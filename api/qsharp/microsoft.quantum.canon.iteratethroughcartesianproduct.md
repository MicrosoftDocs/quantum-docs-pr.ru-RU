---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Операция Итератесраугхкартесианпродукт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840281"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="97aa4-102">Операция Итератесраугхкартесианпродукт</span><span class="sxs-lookup"><span data-stu-id="97aa4-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="97aa4-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="97aa4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="97aa4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="97aa4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="97aa4-105">Применяет операцию для каждого индекса в декартово произведение нескольких диапазонов.</span><span class="sxs-lookup"><span data-stu-id="97aa4-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="97aa4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="97aa4-106">Description</span></span>

<span data-ttu-id="97aa4-107">Итеративно применяет операцию для каждого элемента декартово произведения `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,..., `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="97aa4-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="97aa4-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="97aa4-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="97aa4-109">границы: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="97aa4-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="97aa4-110">Массив, указывающий диапазоны для итерации, при этом каждый диапазон задается как целочисленная длина.</span><span class="sxs-lookup"><span data-stu-id="97aa4-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="97aa4-111">Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="97aa4-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="97aa4-112">Операция, вызываемая для каждого элемента данного декартово произведение.</span><span class="sxs-lookup"><span data-stu-id="97aa4-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="97aa4-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="97aa4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="97aa4-114">Пример</span><span class="sxs-lookup"><span data-stu-id="97aa4-114">Example</span></span>

<span data-ttu-id="97aa4-115">При наличии операции `op` следующие два фрагмента эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="97aa4-115">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a><span data-ttu-id="97aa4-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="97aa4-116">See Also</span></span>

- [<span data-ttu-id="97aa4-117">Microsoft. тактов. Canon. Итератесраугхкартесианповер</span><span class="sxs-lookup"><span data-stu-id="97aa4-117">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)