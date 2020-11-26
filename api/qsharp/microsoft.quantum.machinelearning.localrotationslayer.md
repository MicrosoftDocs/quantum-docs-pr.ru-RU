---
uid: Microsoft.Quantum.MachineLearning.LocalRotationsLayer
title: Функция Локалротатионслайер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LocalRotationsLayer
qsharp.summary: Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.
ms.openlocfilehash: 1549f24427f19bacbadf72e00c1c0181b64bcb73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211735"
---
# <a name="localrotationslayer-function"></a><span data-ttu-id="3d6c7-102">Функция Локалротатионслайер</span><span class="sxs-lookup"><span data-stu-id="3d6c7-102">LocalRotationsLayer function</span></span>

<span data-ttu-id="3d6c7-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="3d6c7-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="3d6c7-105">Возвращает массив неуправляемых (одинарных кубит) поворотов вдоль заданной оси с одним поворотом для каждого кубит в регистре, параметризованным разными параметрами модели.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-105">Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.</span></span>

```qsharp
function LocalRotationsLayer (nQubits : Int, axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="3d6c7-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3d6c7-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="3d6c7-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3d6c7-108">Число Кубитс, обрабатываемых данным слоем.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="3d6c7-109">ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="3d6c7-110">Ось вращения для каждого вращения в заданном слое.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="3d6c7-111">Выходные данные: [контролледротатион](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="3d6c7-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="3d6c7-112">Массив управляемых поворотов относительно заданной оси, по одному на каждый из `nQubits` Кубитс.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>