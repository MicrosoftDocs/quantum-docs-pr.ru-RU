---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Определяемый пользователем тип Контролледротатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 1e664b470caeba656ea4a73f70bbc0ef5fe76f7e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196571"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="99d0b-102">Определяемый пользователем тип Контролледротатион</span><span class="sxs-lookup"><span data-stu-id="99d0b-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="99d0b-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="99d0b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="99d0b-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="99d0b-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="99d0b-105">Описывает управляемый поворот в терминах целевого объекта и индексов управления, ось вращения и индекс в векторе параметров модели.</span><span class="sxs-lookup"><span data-stu-id="99d0b-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="99d0b-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="99d0b-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="99d0b-107">Таржетиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="99d0b-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="99d0b-108">Индекс целевого кубит для этого управляемого вращения.</span><span class="sxs-lookup"><span data-stu-id="99d0b-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="99d0b-109">Контролиндицес: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="99d0b-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="99d0b-110">Массив элементов управления, кубит индексы для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="99d0b-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="99d0b-111">Ось: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="99d0b-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="99d0b-112">Ось для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="99d0b-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="99d0b-113">ParameterIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="99d0b-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="99d0b-114">Индекс в векторе параметра модели, описывающий угол для этого вращения.</span><span class="sxs-lookup"><span data-stu-id="99d0b-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="remarks"></a><span data-ttu-id="99d0b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99d0b-115">Remarks</span></span>

<span data-ttu-id="99d0b-116">Неуправляемый поворот можно представить, задав `ControlIndices` для него пустой массив индексов, `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="99d0b-116">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>