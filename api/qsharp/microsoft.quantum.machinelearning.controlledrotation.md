---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Определяемый пользователем тип Контролледротатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847399"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="128f7-102">Определяемый пользователем тип Контролледротатион</span><span class="sxs-lookup"><span data-stu-id="128f7-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="128f7-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="128f7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="128f7-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="128f7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="128f7-105">Описывает управляемый поворот в терминах целевого объекта и индексов управления, ось вращения и индекс в векторе параметров модели.</span><span class="sxs-lookup"><span data-stu-id="128f7-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="128f7-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="128f7-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="128f7-107">Таржетиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="128f7-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="128f7-108">Индекс целевого кубит для этого управляемого вращения.</span><span class="sxs-lookup"><span data-stu-id="128f7-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="128f7-109">Контролиндицес: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="128f7-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="128f7-110">Массив элементов управления, кубит индексы для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="128f7-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="128f7-111">Ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="128f7-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="128f7-112">Ось для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="128f7-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="128f7-113">ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="128f7-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="128f7-114">Индекс в векторе параметра модели, описывающий угол для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="128f7-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="example"></a><span data-ttu-id="128f7-115">Пример</span><span class="sxs-lookup"><span data-stu-id="128f7-115">Example</span></span>

<span data-ttu-id="128f7-116">Ниже представлен поворот $X $-AXIS первого кубит в регистре, управление вторым кубит, а также угол, заданный Четвертым параметром в последовательной модели.</span><span class="sxs-lookup"><span data-stu-id="128f7-116">The following represents a rotation about the $X$-axis of the first qubit in a register, controlled on the second qubit, and with an angle given by the fourth parameter in a sequential model:</span></span>

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a><span data-ttu-id="128f7-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="128f7-117">Remarks</span></span>

<span data-ttu-id="128f7-118">Неуправляемый поворот можно представить, задав `ControlIndices` для него пустой массив индексов, `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="128f7-118">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>