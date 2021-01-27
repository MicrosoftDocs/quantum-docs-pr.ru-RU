---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Функция перестановки
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 7e563650f33b0292e1e41f629829a2d3b9e5fd28
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848096"
---
# <a name="ispermutation-function"></a><span data-ttu-id="c2d33-102">Функция перестановки</span><span class="sxs-lookup"><span data-stu-id="c2d33-102">IsPermutation function</span></span>

<span data-ttu-id="c2d33-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c2d33-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c2d33-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2d33-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2d33-105">Выводит значение true только в том случае, если данный массив представляет перестановку.</span><span class="sxs-lookup"><span data-stu-id="c2d33-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="c2d33-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c2d33-106">Description</span></span>

<span data-ttu-id="c2d33-107">При наличии массива `array` длины `n` возвращает значение true только в том случае, если каждое целое число из `0` должно `n - 1` встречаться ровно один раз в `array` , например, `array` может интерпретироваться как перестановка `n` элементов.</span><span class="sxs-lookup"><span data-stu-id="c2d33-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="c2d33-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c2d33-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="c2d33-109">пермуатион: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c2d33-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c2d33-110">Массив, который может или не может представлять перестановку.</span><span class="sxs-lookup"><span data-stu-id="c2d33-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c2d33-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c2d33-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="example"></a><span data-ttu-id="c2d33-112">Пример</span><span class="sxs-lookup"><span data-stu-id="c2d33-112">Example</span></span>

<span data-ttu-id="c2d33-113">Следующий код Q # выводит сообщение "все диагностические сообщения успешно выполнены":</span><span class="sxs-lookup"><span data-stu-id="c2d33-113">The following Q# code prints the message "All diagnostics completed successfully":</span></span>

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a><span data-ttu-id="c2d33-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="c2d33-114">Remarks</span></span>

<span data-ttu-id="c2d33-115">Массив нулевой длины является тривиальной перестановкой.</span><span class="sxs-lookup"><span data-stu-id="c2d33-115">An array of length zero is trivially a permutation.</span></span>