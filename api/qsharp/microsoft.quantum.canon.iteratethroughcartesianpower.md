---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Операция Итератесраугхкартесианповер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 2883e7cb30633afe51d380befe806665207c5abd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206482"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="79523-102">Операция Итератесраугхкартесианповер</span><span class="sxs-lookup"><span data-stu-id="79523-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="79523-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="79523-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="79523-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="79523-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="79523-105">Применяет операцию к каждому индексу в блоке питания целого диапазона.</span><span class="sxs-lookup"><span data-stu-id="79523-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="79523-106">Описание</span><span class="sxs-lookup"><span data-stu-id="79523-106">Description</span></span>

<span data-ttu-id="79523-107">Итеративно применяет операцию для каждого элемента декартовой мощности диапазона `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="79523-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="79523-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="79523-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="79523-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="79523-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="79523-110">Постепенная декартка, на которую `0..(bound - 1)` должно быть вызвано значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="79523-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="79523-111">граница: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="79523-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="79523-112">Спецификация диапазона для итерации, заданная как длина диапазона.</span><span class="sxs-lookup"><span data-stu-id="79523-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="79523-113">Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="79523-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="79523-114">Операция, вызываемая для каждого элемента заданной постепенной Декарт.</span><span class="sxs-lookup"><span data-stu-id="79523-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79523-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79523-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="79523-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="79523-116">See Also</span></span>

- [<span data-ttu-id="79523-117">Microsoft. тактов. Canon. Итератесраугхкартесианпродукт</span><span class="sxs-lookup"><span data-stu-id="79523-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)