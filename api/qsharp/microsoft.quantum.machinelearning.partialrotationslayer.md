---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Функция Партиалротатионслайер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852921"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="6b5c7-102">Функция Партиалротатионслайер</span><span class="sxs-lookup"><span data-stu-id="6b5c7-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="6b5c7-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6b5c7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="6b5c7-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="6b5c7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="6b5c7-105">Возвращает массив однокубитных поворотов вдоль заданной оси, параметризованных разными параметрами модели.</span><span class="sxs-lookup"><span data-stu-id="6b5c7-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="6b5c7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6b5c7-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="6b5c7-107">Идксскубитс: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6b5c7-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6b5c7-108">Индексы для Кубитс, которые будут использоваться в качестве целевых объектов для каждого вращения.</span><span class="sxs-lookup"><span data-stu-id="6b5c7-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="6b5c7-109">ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="6b5c7-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="6b5c7-110">Ось вращения для каждого вращения в заданном слое.</span><span class="sxs-lookup"><span data-stu-id="6b5c7-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="6b5c7-111">Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="6b5c7-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="6b5c7-112">Массив управляемых поворотов относительно заданной оси, по одному на каждый из `nQubits` Кубитс.</span><span class="sxs-lookup"><span data-stu-id="6b5c7-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>