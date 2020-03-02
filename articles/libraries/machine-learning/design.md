---
title: Разработка собственного классификатора с помощью КДК
description: Изучите основные понятия конструирования моделей цепи для классификатора, ориентированного на такт.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
ms.openlocfilehash: 4899336f437c1b7712a7831b97fd6ec1431b59a2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909727"
---
# <a name="design-your-own-classifier"></a><span data-ttu-id="0a49a-103">Проектирование собственного классификатора</span><span class="sxs-lookup"><span data-stu-id="0a49a-103">Design your own classifier</span></span>

<span data-ttu-id="0a49a-104">В этом разделе вы узнаете основные понятия, лежащие в основе проектирования моделей каналов для классификатора, ориентированного на такт.</span><span class="sxs-lookup"><span data-stu-id="0a49a-104">In this guide you will learn the basic concepts behind the design of circuit models for the quantum circuit centric classifier.</span></span>

<span data-ttu-id="0a49a-105">Как и в случае с классическим глубоким обучением, не существует общего правила выбора конкретной архитектуры.</span><span class="sxs-lookup"><span data-stu-id="0a49a-105">As in classical deep learning, there is no general rule for choosing a specific architecture.</span></span> <span data-ttu-id="0a49a-106">В зависимости от проблемы некоторые архитектуры будут работать лучше, чем другие.</span><span class="sxs-lookup"><span data-stu-id="0a49a-106">Depending on the problem some architectures will perform better than others.</span></span> <span data-ttu-id="0a49a-107">Но есть некоторые концепции, которые могут быть полезны при проектировании канала:</span><span class="sxs-lookup"><span data-stu-id="0a49a-107">But, there are some concepts that might be useful when designing the circuit:</span></span>

- <span data-ttu-id="0a49a-108">Большое количество параметров подразумевает более гибкую модель, которая может быть удобна для нарисовать сложные границы классификации, но это также может быть более уязвимым для перегонки.</span><span class="sxs-lookup"><span data-stu-id="0a49a-108">A large number of parameters implies a more flexible model, which may be suitable to draw complicated classification boundaries but which may also be more susceptible to overfitting.</span></span>

- <span data-ttu-id="0a49a-109">Шлюзы ентанглинг между Кубитс являются обязательными для записи корреляции между функциями такта.</span><span class="sxs-lookup"><span data-stu-id="0a49a-109">Entangling gates between qubits are essential to capture the correlations between the quantum features.</span></span>

## <a name="how-to-build-a-classifier-with-q"></a><span data-ttu-id="0a49a-110">Создание классификатора с помощью Q\#</span><span class="sxs-lookup"><span data-stu-id="0a49a-110">How to build a classifier with Q\#</span></span>

<span data-ttu-id="0a49a-111">Чтобы создать классификатор, мы будем объединять управляемые параметризованнымные вращения в нашей модели канала.</span><span class="sxs-lookup"><span data-stu-id="0a49a-111">To build a classifier we are going to concatenate parametrized controlled rotations in our circuit model.</span></span> <span data-ttu-id="0a49a-112">Для этого можно использовать тип [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) , определенный в библиотеке машинное обучение тактов.</span><span class="sxs-lookup"><span data-stu-id="0a49a-112">To do it we can use the type [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) defined in the Quantum Machine Learning library.</span></span> <span data-ttu-id="0a49a-113">Этот тип принимает четыре аргумента, которые определяют: индекс целевого кубит, массив индексов элемента управления Кубитс, ось вращения и индекс связанного параметра в массиве параметров, определяющих модель.</span><span class="sxs-lookup"><span data-stu-id="0a49a-113">This type accepts four arguments that determine: the index of the target qubit, the array of indices of the control qubits, the axis of rotation, and index of the associated parameter in the array of parameters defining the model.</span></span>

<span data-ttu-id="0a49a-114">Рассмотрим пример классификатора.</span><span class="sxs-lookup"><span data-stu-id="0a49a-114">Let's see an example of a classifier.</span></span> <span data-ttu-id="0a49a-115">В [примере половинной Луны](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons)мы можем найти следующий классификатор, определенный в файле `Training.qs`.</span><span class="sxs-lookup"><span data-stu-id="0a49a-115">In the [half-moons sample](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons), we can find the following classifier defined in the file `Training.qs`.</span></span>

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

<span data-ttu-id="0a49a-116">Здесь мы определяем функцию, которая возвращает массив элементов `ControlledRotation`, которые вместе с массивом параметров и сдвигом определяют нашу [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel).</span><span class="sxs-lookup"><span data-stu-id="0a49a-116">What we are defining here is a function that returns an array of `ControlledRotation` elements, that together with an array of parameters and a bias will define our [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel).</span></span> <span data-ttu-id="0a49a-117">Этот тип является фундаментальным в библиотеке тактов Машинное обучение и определяет классификатор.</span><span class="sxs-lookup"><span data-stu-id="0a49a-117">This type is fundamental in the Quantum Machine Learning library and defines the classifier.</span></span> <span data-ttu-id="0a49a-118">Цепь, определенная в приведенной выше функции, является частью классификатора, в котором каждый пример набора данных содержит две функции.</span><span class="sxs-lookup"><span data-stu-id="0a49a-118">The circuit defined in the function above is part of a classifier in which each sample of the dataset contains two features.</span></span> <span data-ttu-id="0a49a-119">Поэтому нам нужны только два Кубитс.</span><span class="sxs-lookup"><span data-stu-id="0a49a-119">Therefore we only need two qubits.</span></span> <span data-ttu-id="0a49a-120">Графическое представление канала:</span><span class="sxs-lookup"><span data-stu-id="0a49a-120">The graphical representation of the circuit is:</span></span>

 ![Пример модели канала](~/media/circuit_model_1.PNG)

## <a name="use-the-library-functions-to-write-layers-of-gates"></a><span data-ttu-id="0a49a-122">Использование библиотечных функций для записи уровней шлюзов</span><span class="sxs-lookup"><span data-stu-id="0a49a-122">Use the library functions to write layers of gates</span></span>

<span data-ttu-id="0a49a-123">Предположим, что у нас есть набор данных с 784 компонентами на экземпляр, например изображения с 28 × 28 пикселями, такими как набор данных MNIST.</span><span class="sxs-lookup"><span data-stu-id="0a49a-123">Suppose we have a dataset with 784 features per instance, e.g. images of 28×28 pixels like the MNIST dataset.</span></span> <span data-ttu-id="0a49a-124">В этом случае ширина канала станет достаточно большой, чтобы писать вручную каждый отдельный шлюз станет возможной, но непрактичной задачей.</span><span class="sxs-lookup"><span data-stu-id="0a49a-124">In this case, the width of the circuit becomes large enough so that writing by hand each individual gate becomes a possible but impractical task.</span></span> <span data-ttu-id="0a49a-125">Именно поэтому библиотека тактов Машинное обучение предоставляет набор средств для автоматического создания слоев поворотов параметризованным.</span><span class="sxs-lookup"><span data-stu-id="0a49a-125">This is why the Quantum Machine Learning library provides a set of tools to automatically generate layers of parametrized rotations.</span></span> <span data-ttu-id="0a49a-126">Например, функция [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) возвращает массив неуправляемых поворотов кубит вдоль заданной оси с одним поворотом для каждого кубит в регистре, каждый параметризованным с помощью другого параметра модели.</span><span class="sxs-lookup"><span data-stu-id="0a49a-126">For instance, the function [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) returns an array of uncontrolled single-qubit rotations along a given axis, with one rotation for each qubit in the register, each parametrized by a different model parameter.</span></span> <span data-ttu-id="0a49a-127">Например, `LocalRotationsLayer(4, X)` возвращает следующий набор шлюзов:</span><span class="sxs-lookup"><span data-stu-id="0a49a-127">For example, `LocalRotationsLayer(4, X)` returns the following set of gates:</span></span>

 ![Слой локальных поворотов](~/media/local_rotations_layer.PNG)

<span data-ttu-id="0a49a-129">Мы рекомендуем изучить [API-интерфейс референецеа тактовой машинное обучение библиотеки](xref:microsoft.quantum.machinelearning) , чтобы найти все средства, доступные для упрощения проектирования цепи.</span><span class="sxs-lookup"><span data-stu-id="0a49a-129">We recommend you to explore the [API referenece of the Quantum Machine Learning library](xref:microsoft.quantum.machinelearning) to discover all the tools available to streamline the circuit design.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0a49a-130">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="0a49a-130">Next steps</span></span>

 <span data-ttu-id="0a49a-131">Попробуйте использовать различные структуры в примерах, представленных в примерах.</span><span class="sxs-lookup"><span data-stu-id="0a49a-131">Try different structures in the examples provided by the samples.</span></span> <span data-ttu-id="0a49a-132">Отображаются ли изменения в производительности модели?</span><span class="sxs-lookup"><span data-stu-id="0a49a-132">Do you see any changes in the performance of the model?</span></span> <span data-ttu-id="0a49a-133">В следующем руководстве [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), вы узнаете, как загружать наборы данных для попыток и исследовать новые архитектуры классификаторов.</span><span class="sxs-lookup"><span data-stu-id="0a49a-133">In the next tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), you will learn how to load datasets to try and explore new architectures of classifiers.</span></span>