---
uid: Microsoft.Quantum.Arrays.IsSorted
title: Функция IsSorted
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: a5916b5cbf36e1b6c421a81e04016a333e2b5be7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845736"
---
# <a name="issorted-function"></a><span data-ttu-id="f2319-102">Функция IsSorted</span><span class="sxs-lookup"><span data-stu-id="f2319-102">IsSorted function</span></span>

<span data-ttu-id="f2319-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f2319-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f2319-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f2319-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f2319-105">При наличии массива возвращает значение, указывающее, сортируется ли этот массив как определенный данной функцией сравнения.</span><span class="sxs-lookup"><span data-stu-id="f2319-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="f2319-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f2319-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="f2319-107">Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f2319-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f2319-108">Функция, которая сравнивает два элемента, которые `a` считаются меньше или равными, `b` Если `comparison(a, b)` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="f2319-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="f2319-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="f2319-109">array : 'T[]</span></span>

<span data-ttu-id="f2319-110">Проверяемый массив.</span><span class="sxs-lookup"><span data-stu-id="f2319-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f2319-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f2319-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f2319-112">`true` Если и только для каждой пары элементов `a` и `b` `array` в этом порядке, `comparison(a, b)` то имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="f2319-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2319-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f2319-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f2319-114">Е</span><span class="sxs-lookup"><span data-stu-id="f2319-114">'T</span></span>

<span data-ttu-id="f2319-115">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="f2319-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2319-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2319-116">Remarks</span></span>

<span data-ttu-id="f2319-117">`comparison`Предполагается, что функция является транзитивным, например, если `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` предполагается и.</span><span class="sxs-lookup"><span data-stu-id="f2319-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="f2319-118">Если это свойство не удерживает, выходные данные этой функции могут быть неправильными.</span><span class="sxs-lookup"><span data-stu-id="f2319-118">If this property does not hold, then the output of this function may be incorrect.</span></span>