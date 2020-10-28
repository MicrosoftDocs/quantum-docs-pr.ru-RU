---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Функция Циклицентанглинглайер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 6e0f5057b35baefe2677126ba70ee4fddde7d4db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731112"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="e5c2a-102">Функция Циклицентанглинглайер</span><span class="sxs-lookup"><span data-stu-id="e5c2a-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="e5c2a-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e5c2a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e5c2a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5c2a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5c2a-105">Возвращает массив однонаправленных поворотов вдоль заданной оси, организованных циклически по регистру Кубитс и параметризованных с помощью отдельных параметров модели.</span><span class="sxs-lookup"><span data-stu-id="e5c2a-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="e5c2a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e5c2a-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="e5c2a-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e5c2a-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e5c2a-108">Число Кубитс, обрабатываемых данным слоем.</span><span class="sxs-lookup"><span data-stu-id="e5c2a-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="e5c2a-109">ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e5c2a-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e5c2a-110">Ось вращения для каждого вращения в заданном слое.</span><span class="sxs-lookup"><span data-stu-id="e5c2a-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="e5c2a-111">шаг: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e5c2a-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e5c2a-112">Разделение между целевым индексом и элементами управления для каждого вращения.</span><span class="sxs-lookup"><span data-stu-id="e5c2a-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="e5c2a-113">Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="e5c2a-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="e5c2a-114">Массив кубит управляемых поворотов, которые циклически располагаются в регистре `nQubits` Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e5c2a-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>