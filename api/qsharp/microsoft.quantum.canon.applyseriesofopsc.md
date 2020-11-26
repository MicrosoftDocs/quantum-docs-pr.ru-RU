---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Операция Апплисериесофопск
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: eaa0ea3e33cce708af5879cfbe875397fbb82a8a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217940"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="ad808-102">Операция Апплисериесофопск</span><span class="sxs-lookup"><span data-stu-id="ad808-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="ad808-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ad808-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ad808-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ad808-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ad808-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="ad808-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="ad808-106">Управляет</span><span class="sxs-lookup"><span data-stu-id="ad808-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="ad808-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad808-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="ad808-108">Листофопс: 'T [] = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL []</span><span class="sxs-lookup"><span data-stu-id="ad808-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="ad808-109">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="ad808-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="ad808-110">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="ad808-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="ad808-111">Каждый из них должен иметь управляемый функтор</span><span class="sxs-lookup"><span data-stu-id="ad808-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="ad808-112">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="ad808-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="ad808-113">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="ad808-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="ad808-114">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="ad808-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="ad808-115">Register: не []</span><span class="sxs-lookup"><span data-stu-id="ad808-115">register : 'T[]</span></span>

<span data-ttu-id="ad808-116">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="ad808-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ad808-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ad808-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ad808-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ad808-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ad808-119">Е</span><span class="sxs-lookup"><span data-stu-id="ad808-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="ad808-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="ad808-120">See Also</span></span>

- [<span data-ttu-id="ad808-121">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="ad808-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)