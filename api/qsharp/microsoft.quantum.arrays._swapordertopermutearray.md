---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Функция _SwapOrderToPermuteArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 965f2f3d4f8b366abb27287ce0d27a3b7d7b8fb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730432"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="aed25-102">Функция _SwapOrderToPermuteArray</span><span class="sxs-lookup"><span data-stu-id="aed25-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="aed25-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aed25-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aed25-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aed25-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aed25-105">Возвращает порядок элементов в массиве, который должен быть переключен для создания упорядоченного массива.</span><span class="sxs-lookup"><span data-stu-id="aed25-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="aed25-106">Предполагается, что происходит переключение на месте.</span><span class="sxs-lookup"><span data-stu-id="aed25-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="aed25-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aed25-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="aed25-108">newOrder: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="aed25-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="aed25-109">Массив с перестановкой индексов нового массива.</span><span class="sxs-lookup"><span data-stu-id="aed25-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="aed25-110">Должно быть $n $ Elements, каждое из которых является уникальным целым числом от $0 $ до $n-$1.</span><span class="sxs-lookup"><span data-stu-id="aed25-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="aed25-111">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="aed25-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="aed25-112">Кортеж представляет два индекса, которые нужно поменять местами.</span><span class="sxs-lookup"><span data-stu-id="aed25-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="aed25-113">Перестановки начинаются с самого низкого индекса.</span><span class="sxs-lookup"><span data-stu-id="aed25-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="aed25-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="aed25-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="aed25-115">псуедокоде</span><span class="sxs-lookup"><span data-stu-id="aed25-115">Psuedocode</span></span>

<span data-ttu-id="aed25-116">для (индекс в 0.. Length (newOrder) – 1) {while newOrder [Индекс]! = Индекс {Switch newOrder [Индекс] с newOrder [newOrder [index]]}}</span><span class="sxs-lookup"><span data-stu-id="aed25-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>