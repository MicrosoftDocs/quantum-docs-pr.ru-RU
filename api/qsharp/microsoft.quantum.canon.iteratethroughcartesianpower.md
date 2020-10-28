---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Операция Итератесраугхкартесианповер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716027"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="e6e35-102">Операция Итератесраугхкартесианповер</span><span class="sxs-lookup"><span data-stu-id="e6e35-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="e6e35-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e6e35-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e6e35-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e6e35-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e6e35-105">Применяет операцию к каждому индексу в блоке питания целого диапазона.</span><span class="sxs-lookup"><span data-stu-id="e6e35-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="e6e35-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e6e35-106">Description</span></span>

<span data-ttu-id="e6e35-107">Итеративно применяет операцию для каждого элемента декартовой мощности диапазона `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="e6e35-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="e6e35-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e6e35-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="e6e35-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e6e35-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e6e35-110">Постепенная декартка, на которую `0..(bound - 1)` должно быть вызвано значение диапазона.</span><span class="sxs-lookup"><span data-stu-id="e6e35-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="e6e35-111">граница: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e6e35-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e6e35-112">Спецификация диапазона для итерации, заданная как длина диапазона.</span><span class="sxs-lookup"><span data-stu-id="e6e35-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="e6e35-113">Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="e6e35-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e6e35-114">Операция, вызываемая для каждого элемента заданной постепенной Декарт.</span><span class="sxs-lookup"><span data-stu-id="e6e35-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e6e35-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e6e35-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="e6e35-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="e6e35-116">See Also</span></span>

- [<span data-ttu-id="e6e35-117">Microsoft. тактов. Canon. Итератесраугхкартесианпродукт</span><span class="sxs-lookup"><span data-stu-id="e6e35-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)