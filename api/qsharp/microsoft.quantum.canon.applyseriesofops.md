---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Операция Апплисериесофопс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b8810e7d31689046e72905195a3a25ef80fc8d67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218008"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="4de4c-102">Операция Апплисериесофопс</span><span class="sxs-lookup"><span data-stu-id="4de4c-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="4de4c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4de4c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4de4c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4de4c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4de4c-105">Применяет список Ops и их целевых объектов последовательно в массиве.</span><span class="sxs-lookup"><span data-stu-id="4de4c-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4de4c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4de4c-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="4de4c-107">Листофопс: 'T [] = [модуль](xref:microsoft.quantum.lang-ref.unit)> []</span><span class="sxs-lookup"><span data-stu-id="4de4c-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="4de4c-108">Список операций, каждый из которых принимает массив «t» для применения.</span><span class="sxs-lookup"><span data-stu-id="4de4c-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="4de4c-109">Они применяются последовательно, сначала по нижнему индексу.</span><span class="sxs-lookup"><span data-stu-id="4de4c-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="4de4c-110">целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="4de4c-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="4de4c-111">Вложенные массивы, описывающие целевые объекты Op.</span><span class="sxs-lookup"><span data-stu-id="4de4c-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="4de4c-112">Каждый массив должен содержать список ints, описывающих индексы для использования.</span><span class="sxs-lookup"><span data-stu-id="4de4c-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="4de4c-113">Register: не []</span><span class="sxs-lookup"><span data-stu-id="4de4c-113">register : 'T[]</span></span>

<span data-ttu-id="4de4c-114">Регистр кубит, по которому будет выполняться операция.</span><span class="sxs-lookup"><span data-stu-id="4de4c-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4de4c-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4de4c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="4de4c-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="4de4c-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4de4c-117">Е</span><span class="sxs-lookup"><span data-stu-id="4de4c-117">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="4de4c-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="4de4c-118">See Also</span></span>

- [<span data-ttu-id="4de4c-119">Microsoft. тактов. Canon. Апплйопрепеатедлйовер</span><span class="sxs-lookup"><span data-stu-id="4de4c-119">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)