---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Операция Апплисериесофопска
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9dd1343b3ebcc75592441f150eee822cfe83f9a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217889"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="811a1-102">Операция Апплисериесофопска</span><span class="sxs-lookup"><span data-stu-id="811a1-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="811a1-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="811a1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="811a1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="811a1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="811a1-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="811a1-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="811a1-106">(Смежное + управление)</span><span class="sxs-lookup"><span data-stu-id="811a1-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="811a1-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="811a1-107">Input</span></span>

### <a name="listofops--t--unit--is-adj--ctl"></a><span data-ttu-id="811a1-108">Листофопс: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"</span><span class="sxs-lookup"><span data-stu-id="811a1-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="811a1-109">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="811a1-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="811a1-110">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="811a1-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="811a1-111">Каждый из них должен иметь одновременно соседний и контролируемый функтор.</span><span class="sxs-lookup"><span data-stu-id="811a1-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="811a1-112">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="811a1-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="811a1-113">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="811a1-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="811a1-114">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="811a1-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="811a1-115">Register: не []</span><span class="sxs-lookup"><span data-stu-id="811a1-115">register : 'T[]</span></span>

<span data-ttu-id="811a1-116">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="811a1-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="811a1-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="811a1-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="811a1-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="811a1-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="811a1-119">Е</span><span class="sxs-lookup"><span data-stu-id="811a1-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="811a1-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="811a1-120">See Also</span></span>

- [<span data-ttu-id="811a1-121">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="811a1-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)