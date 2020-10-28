---
uid: Microsoft.Quantum.Arrays.IsSorted
title: Функция IsSorted
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: 330c1f789585f64cf255bc74f8a9c1ccf81b009e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730169"
---
# <a name="issorted-function"></a><span data-ttu-id="b23ee-102">Функция IsSorted</span><span class="sxs-lookup"><span data-stu-id="b23ee-102">IsSorted function</span></span>

<span data-ttu-id="b23ee-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b23ee-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b23ee-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b23ee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b23ee-105">При наличии массива возвращает значение, указывающее, сортируется ли этот массив как определенный данной функцией сравнения.</span><span class="sxs-lookup"><span data-stu-id="b23ee-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="b23ee-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b23ee-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="b23ee-107">Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b23ee-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b23ee-108">Функция, которая сравнивает два элемента, которые `a` считаются меньше или равными, `b` Если `comparison(a, b)` имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="b23ee-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="b23ee-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="b23ee-109">array : 'T[]</span></span>

<span data-ttu-id="b23ee-110">Проверяемый массив.</span><span class="sxs-lookup"><span data-stu-id="b23ee-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b23ee-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b23ee-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b23ee-112">`true` Если и только для каждой пары элементов `a` и `b` `array` в этом порядке, `comparison(a, b)` то имеет значение `true` .</span><span class="sxs-lookup"><span data-stu-id="b23ee-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b23ee-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b23ee-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b23ee-114">Е</span><span class="sxs-lookup"><span data-stu-id="b23ee-114">'T</span></span>

<span data-ttu-id="b23ee-115">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="b23ee-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b23ee-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="b23ee-116">Remarks</span></span>

<span data-ttu-id="b23ee-117">`comparison`Предполагается, что функция является транзитивным, например, если `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` предполагается и.</span><span class="sxs-lookup"><span data-stu-id="b23ee-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="b23ee-118">Если это свойство не удерживает, выходные данные этой функции могут быть неправильными.</span><span class="sxs-lookup"><span data-stu-id="b23ee-118">If this property does not hold, then the output of this function may be incorrect.</span></span>