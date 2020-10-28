---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Определяемый пользователем тип Контролледротатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: afc425c16ab550fd414e656484c9ff6f0f8f3ef4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711365"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="dc45e-102">Определяемый пользователем тип Контролледротатион</span><span class="sxs-lookup"><span data-stu-id="dc45e-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="dc45e-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dc45e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="dc45e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc45e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc45e-105">Описывает управляемый поворот в терминах целевого объекта и индексов управления, ось вращения и индекс в векторе параметров модели.</span><span class="sxs-lookup"><span data-stu-id="dc45e-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="dc45e-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="dc45e-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="dc45e-107">Таржетиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc45e-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc45e-108">Индекс целевого кубит для этого управляемого вращения.</span><span class="sxs-lookup"><span data-stu-id="dc45e-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="dc45e-109">Контролиндицес: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dc45e-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dc45e-110">Массив элементов управления, кубит индексы для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="dc45e-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="dc45e-111">Ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="dc45e-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="dc45e-112">Ось для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="dc45e-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="dc45e-113">ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc45e-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc45e-114">Индекс в векторе параметра модели, описывающий угол для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="dc45e-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc45e-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="dc45e-115">Remarks</span></span>

<span data-ttu-id="dc45e-116">Неуправляемый поворот можно представить, задав `ControlIndices` для него пустой массив индексов, `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="dc45e-116">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>