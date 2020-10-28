---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Операция Апплисериесофопса
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: e2b928fa4c9446e16d2bf5e7b68a32d4bba3a528
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717652"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="92c1f-102">Операция Апплисериесофопса</span><span class="sxs-lookup"><span data-stu-id="92c1f-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="92c1f-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="92c1f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="92c1f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="92c1f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="92c1f-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="92c1f-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="92c1f-106">(Прилегающий)</span><span class="sxs-lookup"><span data-stu-id="92c1f-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="92c1f-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="92c1f-107">Input</span></span>

### <a name="listofops--t--unit-adj"></a><span data-ttu-id="92c1f-108">Листофопс: 'T [] => [единица измерения](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="92c1f-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj[]</span></span>

<span data-ttu-id="92c1f-109">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="92c1f-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="92c1f-110">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="92c1f-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="92c1f-111">Каждый должен иметь смежный функтор</span><span class="sxs-lookup"><span data-stu-id="92c1f-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="92c1f-112">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="92c1f-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="92c1f-113">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="92c1f-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="92c1f-114">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="92c1f-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="92c1f-115">Register: не []</span><span class="sxs-lookup"><span data-stu-id="92c1f-115">register : 'T[]</span></span>

<span data-ttu-id="92c1f-116">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="92c1f-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="92c1f-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="92c1f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="92c1f-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="92c1f-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="92c1f-119">Е</span><span class="sxs-lookup"><span data-stu-id="92c1f-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="92c1f-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="92c1f-120">See Also</span></span>

- [<span data-ttu-id="92c1f-121">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="92c1f-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)