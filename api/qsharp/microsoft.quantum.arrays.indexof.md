---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848528"
---
# <a name="indexof-function"></a><span data-ttu-id="bf0fc-102">IndexOf, функция</span><span class="sxs-lookup"><span data-stu-id="bf0fc-102">IndexOf function</span></span>

<span data-ttu-id="bf0fc-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bf0fc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bf0fc-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bf0fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bf0fc-105">Возвращает первый индекс первого элемента в массиве, удовлетворяющего заданному предикату.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="bf0fc-106">Если такого элемента не существует, возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="bf0fc-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bf0fc-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="bf0fc-108">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bf0fc-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bf0fc-109">Функция предиката, действующая на элементы массива.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="bf0fc-110">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="bf0fc-110">arr : 'T[]</span></span>

<span data-ttu-id="bf0fc-111">Массив для поиска с использованием заданного предиката.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="bf0fc-112">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf0fc-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf0fc-113">Наименьший индекс, `idx` такой как `predicate(arr[idx])` true, или-1, если такого элемента не существует.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bf0fc-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="bf0fc-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bf0fc-115">Е</span><span class="sxs-lookup"><span data-stu-id="bf0fc-115">'T</span></span>



## <a name="example"></a><span data-ttu-id="bf0fc-116">Пример</span><span class="sxs-lookup"><span data-stu-id="bf0fc-116">Example</span></span>

<span data-ttu-id="bf0fc-117">Предположим, что `IsEven : Int -> Bool` это функция, которая возвращает значение, `true` только если входные данные являются четными.</span><span class="sxs-lookup"><span data-stu-id="bf0fc-117">Suppose that `IsEven : Int -> Bool` is a function that returns `true` if and only if its input is even.</span></span> <span data-ttu-id="bf0fc-118">Затем это можно использовать с `IndexOf` для поиска первого четного элемента в массиве:</span><span class="sxs-lookup"><span data-stu-id="bf0fc-118">Then, this can be used with `IndexOf` to find the first even element in an array:</span></span>

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```