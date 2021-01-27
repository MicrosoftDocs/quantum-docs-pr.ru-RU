---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Функция Лексографиккомпарисон
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: de8179ab6e835d08e7f41287f31a876b7ecc91c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814380"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="fe0b2-102">Функция Лексографиккомпарисон</span><span class="sxs-lookup"><span data-stu-id="fe0b2-102">LexographicComparison function</span></span>

<span data-ttu-id="fe0b2-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="fe0b2-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="fe0b2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fe0b2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fe0b2-105">При наличии функции сравнения возвращает новую функцию, лексографикалли сравнение двух массивов.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="fe0b2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fe0b2-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="fe0b2-107">Елементкомпарисон: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fe0b2-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fe0b2-108">Функция, которая сравнивает два элемента `x` и `y` возвращает, если `x` меньше или равно `y` .</span><span class="sxs-lookup"><span data-stu-id="fe0b2-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="fe0b2-109">Выходные данные: ('T [], t [])-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fe0b2-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fe0b2-110">Функция, которая сравнивает два массива `xs` и `ys` и возвращает значение, если `xs` происходит до или равно `ys` в порядке лексографикал.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fe0b2-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fe0b2-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fe0b2-112">Е</span><span class="sxs-lookup"><span data-stu-id="fe0b2-112">'T</span></span>

<span data-ttu-id="fe0b2-113">Тип элементов сравниваемых массивов.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe0b2-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="fe0b2-114">Remarks</span></span>

<span data-ttu-id="fe0b2-115">Сравнение лексографик между двумя массивами `xs` и `ys` определяется следующей процедурой.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="fe0b2-116">Мы говорим, что два элемента `x` и `y` эквивалентны, если `elementComparison(x, y)` и `elementComparison(y, x)` оба имеют значение true.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="fe0b2-117">Оба массива сравниваются по элементу до тех пор, пока первая пара элементов не эквивалентна.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="fe0b2-118">Массив, содержащий элемент, который в первую очередь выполняется в соответствии с `elementComparison` , считается первым в упорядочении лексографикал.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="fe0b2-119">Если неэквивалентные элементы не найдены и один массив длиннее другого, то считается, что первым является более короткий массив.</span><span class="sxs-lookup"><span data-stu-id="fe0b2-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe0b2-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="fe0b2-120">See Also</span></span>

- [<span data-ttu-id="fe0b2-121">Microsoft. тактов. Arrays. Sorted</span><span class="sxs-lookup"><span data-stu-id="fe0b2-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)