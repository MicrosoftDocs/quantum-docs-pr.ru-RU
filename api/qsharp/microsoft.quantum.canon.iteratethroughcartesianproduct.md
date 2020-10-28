---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Операция Итератесраугхкартесианпродукт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: e4fc71f6f707639f6f89eece8546ec2fb434a15a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716041"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="746e7-102">Операция Итератесраугхкартесианпродукт</span><span class="sxs-lookup"><span data-stu-id="746e7-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="746e7-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="746e7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="746e7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="746e7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="746e7-105">Применяет операцию для каждого индекса в декартово произведение нескольких диапазонов.</span><span class="sxs-lookup"><span data-stu-id="746e7-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="746e7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="746e7-106">Description</span></span>

<span data-ttu-id="746e7-107">Итеративно применяет операцию для каждого элемента декартово произведения `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,..., `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="746e7-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="746e7-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="746e7-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="746e7-109">границы: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="746e7-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="746e7-110">Массив, указывающий диапазоны для итерации, при этом каждый диапазон задается как целочисленная длина.</span><span class="sxs-lookup"><span data-stu-id="746e7-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="746e7-111">Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="746e7-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="746e7-112">Операция, вызываемая для каждого элемента данного декартово произведение.</span><span class="sxs-lookup"><span data-stu-id="746e7-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="746e7-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="746e7-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="746e7-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="746e7-114">See Also</span></span>

- [<span data-ttu-id="746e7-115">Microsoft. тактов. Canon. Итератесраугхкартесианповер</span><span class="sxs-lookup"><span data-stu-id="746e7-115">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)