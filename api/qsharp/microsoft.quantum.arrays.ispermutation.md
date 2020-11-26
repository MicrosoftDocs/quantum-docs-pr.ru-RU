---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Функция перестановки
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220932"
---
# <a name="ispermutation-function"></a><span data-ttu-id="3b9f9-102">Функция перестановки</span><span class="sxs-lookup"><span data-stu-id="3b9f9-102">IsPermutation function</span></span>

<span data-ttu-id="3b9f9-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3b9f9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3b9f9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3b9f9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3b9f9-105">Выводит значение true только в том случае, если данный массив представляет перестановку.</span><span class="sxs-lookup"><span data-stu-id="3b9f9-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="3b9f9-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3b9f9-106">Description</span></span>

<span data-ttu-id="3b9f9-107">При наличии массива `array` длины `n` возвращает значение true только в том случае, если каждое целое число из `0` должно `n - 1` встречаться ровно один раз в `array` , например, `array` может интерпретироваться как перестановка `n` элементов.</span><span class="sxs-lookup"><span data-stu-id="3b9f9-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="3b9f9-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3b9f9-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="3b9f9-109">пермуатион: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3b9f9-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3b9f9-110">Массив, который может или не может представлять перестановку.</span><span class="sxs-lookup"><span data-stu-id="3b9f9-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3b9f9-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3b9f9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="3b9f9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b9f9-112">Remarks</span></span>

<span data-ttu-id="3b9f9-113">Массив нулевой длины является тривиальной перестановкой.</span><span class="sxs-lookup"><span data-stu-id="3b9f9-113">An array of length zero is trivially a permutation.</span></span>