---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Функция Ректангулараррайфакт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: 8cf6b85da6e8fee7fc255a173753a6468d8134b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845486"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="e5d40-102">Функция Ректангулараррайфакт</span><span class="sxs-lookup"><span data-stu-id="e5d40-102">RectangularArrayFact function</span></span>

<span data-ttu-id="e5d40-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e5d40-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e5d40-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e5d40-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e5d40-105">Представляет условие, в котором двухмерный массив имеет прямоугольную фигуру</span><span class="sxs-lookup"><span data-stu-id="e5d40-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="e5d40-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e5d40-106">Description</span></span>

<span data-ttu-id="e5d40-107">Эта функция утверждает, что каждая строка в массиве имеет одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="e5d40-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="e5d40-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e5d40-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="e5d40-109">массив: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="e5d40-109">array : 'T[][]</span></span>

<span data-ttu-id="e5d40-110">Двухмерный массив элементов</span><span class="sxs-lookup"><span data-stu-id="e5d40-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="e5d40-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e5d40-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e5d40-112">Выводимое сообщение, если массив не является прямоугольным массивом</span><span class="sxs-lookup"><span data-stu-id="e5d40-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="e5d40-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5d40-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e5d40-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e5d40-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e5d40-115">Е</span><span class="sxs-lookup"><span data-stu-id="e5d40-115">'T</span></span>

<span data-ttu-id="e5d40-116">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="e5d40-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="e5d40-117">Пример</span><span class="sxs-lookup"><span data-stu-id="e5d40-117">Example</span></span>

```qsharp
RectangularArrayFact([[1, 2], [3, 4]], "Array is not rectangular");       // okay
RectangularArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not rectangular"); // okay
RectangularArrayFact([[1, 2], [3, 4, 5]], "Array is not rectangular");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="e5d40-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="e5d40-118">See Also</span></span>

- [<span data-ttu-id="e5d40-119">Microsoft. тактов. Arrays. Скуареаррайфакт</span><span class="sxs-lookup"><span data-stu-id="e5d40-119">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)