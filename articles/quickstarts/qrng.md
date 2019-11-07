---
title: Создание квантового генератора случайных чисел
description: Создайте проект Q#, который демонстрирует фундаментальные квантовые понятия, например суперпозицию, на примере квантового генератора случайных чисел.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: c3039b92c4b3235a397d5cf31280ac2673706e9d
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462839"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="d5cf5-103">Краткое руководство. Реализация квантового генератора случайных чисел на языке Q#</span><span class="sxs-lookup"><span data-stu-id="d5cf5-103">Quickstart: Implement a Quantum Random Number Generator in Q#</span></span>
<span data-ttu-id="d5cf5-104">Простой пример квантового алгоритма на языке Q#, который моделирует генератор случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="d5cf5-105">Этот алгоритм использует природу квантовой механики для получения случайного числа.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d5cf5-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="d5cf5-106">Prerequisites</span></span>

- <span data-ttu-id="d5cf5-107">[Microsoft Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="d5cf5-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="d5cf5-108">Создание проекта Q#</span><span class="sxs-lookup"><span data-stu-id="d5cf5-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a><span data-ttu-id="d5cf5-109">Создание операции Q#</span><span class="sxs-lookup"><span data-stu-id="d5cf5-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="d5cf5-110">Код операции Q#</span><span class="sxs-lookup"><span data-stu-id="d5cf5-110">Q# operation code</span></span>

1. <span data-ttu-id="d5cf5-111">Замените содержимое файла Operation.cs следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="d5cf5-111">Replace the contents of the Operation.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(q = Qubit())  { // Allocate a qubit.
                H(q);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(q);     // Measure the qubit value.
                Reset(q);
                return r;
            }
        }
    }
    ```

<span data-ttu-id="d5cf5-112">Как упоминалось в статье [Сведения о квантовых вычислениях](xref:microsoft.quantum.overview.what), кубит представляет собой единицу квантовой информации и может находиться в состоянии суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-112">As mentioned in our [What is Quantum Computing?](xref:microsoft.quantum.overview.what) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="d5cf5-113">При измерении он всегда возвращает значение 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="d5cf5-114">Но во время выполнения состояние кубита отражает вероятность получить значение 0 или 1 при измерении.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="d5cf5-115">Такое вероятностное состояние называется суперпозицией.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="d5cf5-116">Эту вероятность мы можем применить для создания случайных чисел.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="d5cf5-117">Мы создадим операцию Q#, в которой используется тип данных `Qubit`,уникальный для языка Q#.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="d5cf5-118">`Qubit` можно выделить инструкцией `using`.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="d5cf5-119">Только что выделенный кубит всегда находится в состоянии `Zero`.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-119">When it gets allocated a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="d5cf5-120">С помощью операции `H` мы можем перевести `Qubit` в состояние суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="d5cf5-121">Чтобы измерить кубит, т. е. определить его значение, используется специальная операция `M`.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="d5cf5-122">Каждый раз, когда мы переводим `Qubit` в состояние суперпозиции и измеряем его, мы получаем разные значения.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span> 

<span data-ttu-id="d5cf5-123">При отмене выделения `Qubit` необходимо явным образом вернуть ему состояние `Zero`. В противном случае симулятор вернет ошибку при выполнении.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="d5cf5-124">Для этого проще всего вызвать `Reset`.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="d5cf5-125">Визуализация кода в формате сферы Блоха</span><span class="sxs-lookup"><span data-stu-id="d5cf5-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="d5cf5-126">В сфере Блоха северный полюс соответствует классическому значению **0**, а южный — классическому значению **1**.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-126">In the Bloch sphere the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="d5cf5-127">Любое состояние суперпозиции обозначается точкой на этой сфере (или стрелкой на схеме).</span><span class="sxs-lookup"><span data-stu-id="d5cf5-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="d5cf5-128">Чем ближе конец этой стрелки к одному из полюсов, тем выше вероятность схлопывания этого кубита при измерении в то классическое состояние, которое соответствует этому полюсу.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-128">When the closer the end of the arrow to a pole, the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="d5cf5-129">В примере ниже красная стрелка обозначает состояние с более высокой вероятностью получить значение **0** при измерении кубита.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="./Bloch.svg" width="175">

<span data-ttu-id="d5cf5-130">Мы можем использовать это представление для визуализации работы нашего кода.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="d5cf5-131">Для начала мы инициализируем кубит в состоянии **0** и применим `H`, чтобы создать состояние суперпозиции с равной вероятностью получить значения **0** и **1**.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-131">First we start with a qubit initalizated in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="./H.svg" width="450">

* <span data-ttu-id="d5cf5-132">Затем мы измерим состояние кубита и сохраним выходное значение:</span><span class="sxs-lookup"><span data-stu-id="d5cf5-132">Then we measure the qubit and save the output:</span></span>

<img src="./Measurement2.svg" width="450">

<span data-ttu-id="d5cf5-133">Так как исход этого измерения является полностью случайным, можно считать, что мы получили случайный бит.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="d5cf5-134">Вызывая эту операцию несколько раз, мы получим большое целое число.</span><span class="sxs-lookup"><span data-stu-id="d5cf5-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="d5cf5-135">Например, три вызова этой операции возвращают три случайных бита, позволяя создать трехбитовое число (т. е. случайное число в диапазоне от 0 до 7).</span><span class="sxs-lookup"><span data-stu-id="d5cf5-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>
