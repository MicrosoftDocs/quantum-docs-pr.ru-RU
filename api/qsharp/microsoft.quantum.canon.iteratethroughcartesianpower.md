---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Операция Итератесраугхкартесианповер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840302"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="2b6b2-102">Операция Итератесраугхкартесианповер</span><span class="sxs-lookup"><span data-stu-id="2b6b2-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="2b6b2-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2b6b2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2b6b2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b6b2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2b6b2-105">Применяет операцию к каждому индексу в блоке питания целого диапазона.</span><span class="sxs-lookup"><span data-stu-id="2b6b2-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="2b6b2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="2b6b2-106">Description</span></span>

<span data-ttu-id="2b6b2-107">Итеративно применяет операцию для каждого элемента декартовой мощности диапазона `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="2b6b2-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="2b6b2-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2b6b2-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="2b6b2-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2b6b2-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2b6b2-110">Постепенная декартка, на которую `0..(bound - 1)` должно быть вызвано значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="2b6b2-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="2b6b2-111">граница: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2b6b2-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2b6b2-112">Спецификация диапазона для итерации, заданная как длина диапазона.</span><span class="sxs-lookup"><span data-stu-id="2b6b2-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="2b6b2-113">Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="2b6b2-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="2b6b2-114">Операция, вызываемая для каждого элемента заданной постепенной Декарт.</span><span class="sxs-lookup"><span data-stu-id="2b6b2-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2b6b2-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2b6b2-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="2b6b2-116">Пример</span><span class="sxs-lookup"><span data-stu-id="2b6b2-116">Example</span></span>

<span data-ttu-id="2b6b2-117">При наличии операции `op` следующие два фрагмента эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="2b6b2-117">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a><span data-ttu-id="2b6b2-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="2b6b2-118">See Also</span></span>

- [<span data-ttu-id="2b6b2-119">Microsoft. тактов. Canon. Итератесраугхкартесианпродукт</span><span class="sxs-lookup"><span data-stu-id="2b6b2-119">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)