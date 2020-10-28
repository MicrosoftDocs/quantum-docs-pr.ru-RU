---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Функция Партиалротатионслайер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ab964d2c43a13a5daf64aefdeccd1c26cd371ff4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732321"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="e3570-102">Функция Партиалротатионслайер</span><span class="sxs-lookup"><span data-stu-id="e3570-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="e3570-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e3570-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e3570-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e3570-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e3570-105">Возвращает массив однокубитных поворотов вдоль заданной оси, параметризованных разными параметрами модели.</span><span class="sxs-lookup"><span data-stu-id="e3570-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="e3570-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e3570-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="e3570-107">Идксскубитс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="e3570-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="e3570-108">Индексы для Кубитс, которые будут использоваться в качестве целевых объектов для каждого вращения.</span><span class="sxs-lookup"><span data-stu-id="e3570-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="e3570-109">ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e3570-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e3570-110">Ось вращения для каждого вращения в заданном слое.</span><span class="sxs-lookup"><span data-stu-id="e3570-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="e3570-111">Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="e3570-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="e3570-112">Массив управляемых поворотов относительно заданной оси, по одному на каждый из `nQubits` Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e3570-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>