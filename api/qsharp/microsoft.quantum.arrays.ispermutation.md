---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Функция перестановки
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 361bb21bedc725c25a1f3dfc811e9cfda4cb45ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730176"
---
# <a name="ispermutation-function"></a><span data-ttu-id="c6710-102">Функция перестановки</span><span class="sxs-lookup"><span data-stu-id="c6710-102">IsPermutation function</span></span>

<span data-ttu-id="c6710-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c6710-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c6710-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6710-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6710-105">Выводит значение true только в том случае, если данный массив представляет перестановку.</span><span class="sxs-lookup"><span data-stu-id="c6710-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="c6710-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c6710-106">Description</span></span>

<span data-ttu-id="c6710-107">При наличии массива `array` длины `n` возвращает значение true только в том случае, если каждое целое число из `0` должно `n - 1` встречаться ровно один раз в `array` , например, `array` может интерпретироваться как перестановка `n` элементов.</span><span class="sxs-lookup"><span data-stu-id="c6710-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="c6710-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c6710-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="c6710-109">пермуатион: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c6710-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c6710-110">Массив, который может или не может представлять перестановку.</span><span class="sxs-lookup"><span data-stu-id="c6710-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c6710-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c6710-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="c6710-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="c6710-112">Remarks</span></span>

<span data-ttu-id="c6710-113">Массив нулевой длины является тривиальной перестановкой.</span><span class="sxs-lookup"><span data-stu-id="c6710-113">An array of length zero is trivially a permutation.</span></span>