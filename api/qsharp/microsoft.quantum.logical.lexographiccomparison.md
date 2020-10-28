---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Функция Лексографиккомпарисон
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: f0b68974a0ea26907b58971e4fa4b1f06f5714d2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709909"
---
# <a name="lexographiccomparison-function"></a><span data-ttu-id="8def4-102">Функция Лексографиккомпарисон</span><span class="sxs-lookup"><span data-stu-id="8def4-102">LexographicComparison function</span></span>

<span data-ttu-id="8def4-103">Пространство имен: [Microsoft. тактов. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8def4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8def4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8def4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8def4-105">При наличии функции сравнения возвращает новую функцию, лексографикалли сравнение двух массивов.</span><span class="sxs-lookup"><span data-stu-id="8def4-105">Given a comparison function, returns a new function that lexographically compares two arrays.</span></span>

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a><span data-ttu-id="8def4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8def4-106">Input</span></span>

### <a name="elementcomparison--tt---bool"></a><span data-ttu-id="8def4-107">Елементкомпарисон: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8def4-107">elementComparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8def4-108">Функция, которая сравнивает два элемента `x` и `y` возвращает, если `x` меньше или равно `y` .</span><span class="sxs-lookup"><span data-stu-id="8def4-108">A function that compares two elements `x` and `y` and returns if `x` is less than or equal to `y`.</span></span>



## <a name="output--tt---bool"></a><span data-ttu-id="8def4-109">Выходные данные: ('T [], t [])-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8def4-109">Output : ('T[],'T[]) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8def4-110">Функция, которая сравнивает два массива `xs` и `ys` и возвращает значение, если `xs` происходит до или равно `ys` в порядке лексографикал.</span><span class="sxs-lookup"><span data-stu-id="8def4-110">A function that compares two arrays `xs` and `ys` and returns if `xs` occurs before or equal to `ys` in lexographical ordering.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8def4-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8def4-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8def4-112">Е</span><span class="sxs-lookup"><span data-stu-id="8def4-112">'T</span></span>

<span data-ttu-id="8def4-113">Тип элементов сравниваемых массивов.</span><span class="sxs-lookup"><span data-stu-id="8def4-113">The type of the elements of the arrays being compared.</span></span>

## <a name="remarks"></a><span data-ttu-id="8def4-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="8def4-114">Remarks</span></span>

<span data-ttu-id="8def4-115">Сравнение лексографик между двумя массивами `xs` и `ys` определяется следующей процедурой.</span><span class="sxs-lookup"><span data-stu-id="8def4-115">The lexographic comparison between two arrays `xs` and `ys` is defined by the following procedure.</span></span> <span data-ttu-id="8def4-116">Мы говорим, что два элемента `x` и `y` эквивалентны, если `elementComparison(x, y)` и `elementComparison(y, x)` оба имеют значение true.</span><span class="sxs-lookup"><span data-stu-id="8def4-116">We say that two elements `x` and `y` are equivalent if `elementComparison(x, y)` and `elementComparison(y, x)` are both true.</span></span>

- <span data-ttu-id="8def4-117">Оба массива сравниваются по элементу до тех пор, пока первая пара элементов не эквивалентна.</span><span class="sxs-lookup"><span data-stu-id="8def4-117">Both arrays are compared element-by-element until the first pair of elements that are not equivalent.</span></span> <span data-ttu-id="8def4-118">Массив, содержащий элемент, который в первую очередь выполняется в соответствии с `elementComparison` , считается первым в упорядочении лексографикал.</span><span class="sxs-lookup"><span data-stu-id="8def4-118">The array containing the element that occurs first according to `elementComparison` is said to occur first in lexographical ordering.</span></span>
- <span data-ttu-id="8def4-119">Если неэквивалентные элементы не найдены и один массив длиннее другого, то считается, что первым является более короткий массив.</span><span class="sxs-lookup"><span data-stu-id="8def4-119">If no inequivalent elements are found, and one array is longer than the other, the shorter array is said to occur first.</span></span>

## <a name="see-also"></a><span data-ttu-id="8def4-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="8def4-120">See Also</span></span>

- [<span data-ttu-id="8def4-121">Microsoft. тактов. Arrays. Sorted</span><span class="sxs-lookup"><span data-stu-id="8def4-121">Microsoft.Quantum.Arrays.Sorted</span></span>](xref:Microsoft.Quantum.Arrays.Sorted)