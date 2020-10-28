---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Операция Апплисериесофопска
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 2327a693e528cf46f95eae5ee052e9dd9b6ee187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717637"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="f3a97-102">Операция Апплисериесофопска</span><span class="sxs-lookup"><span data-stu-id="f3a97-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="f3a97-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f3a97-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f3a97-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f3a97-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f3a97-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="f3a97-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="f3a97-106">(Смежное + управление)</span><span class="sxs-lookup"><span data-stu-id="f3a97-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="f3a97-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f3a97-107">Input</span></span>

### <a name="listofops--t--unit-adj--ctl"></a><span data-ttu-id="f3a97-108">Листофопс: 'T [] => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL []</span><span class="sxs-lookup"><span data-stu-id="f3a97-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="f3a97-109">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="f3a97-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="f3a97-110">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="f3a97-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="f3a97-111">Каждый из них должен иметь одновременно соседний и контролируемый функтор.</span><span class="sxs-lookup"><span data-stu-id="f3a97-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="f3a97-112">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="f3a97-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="f3a97-113">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="f3a97-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="f3a97-114">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="f3a97-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="f3a97-115">Register: не []</span><span class="sxs-lookup"><span data-stu-id="f3a97-115">register : 'T[]</span></span>

<span data-ttu-id="f3a97-116">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="f3a97-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f3a97-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f3a97-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f3a97-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f3a97-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f3a97-119">Е</span><span class="sxs-lookup"><span data-stu-id="f3a97-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="f3a97-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="f3a97-120">See Also</span></span>

- [<span data-ttu-id="f3a97-121">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="f3a97-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)