---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Функция Скуареаррайфакт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: a154e5becba4dae762596a3fc1b268855520fa1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850969"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="ba114-102">Функция Скуареаррайфакт</span><span class="sxs-lookup"><span data-stu-id="ba114-102">SquareArrayFact function</span></span>

<span data-ttu-id="ba114-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ba114-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ba114-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ba114-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ba114-105">Представляет условие, которое двумерный массив имеет квадратную фигуру</span><span class="sxs-lookup"><span data-stu-id="ba114-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="ba114-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ba114-106">Description</span></span>

<span data-ttu-id="ba114-107">Эта функция утверждает, что каждая строка в массиве содержит столько элементов, сколько строк (элементов) в массиве.</span><span class="sxs-lookup"><span data-stu-id="ba114-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="ba114-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ba114-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="ba114-109">массив: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="ba114-109">array : 'T[][]</span></span>

<span data-ttu-id="ba114-110">Двухмерный массив элементов</span><span class="sxs-lookup"><span data-stu-id="ba114-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="ba114-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="ba114-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="ba114-112">Выводимое сообщение, если массив не является квадратным массивом</span><span class="sxs-lookup"><span data-stu-id="ba114-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="ba114-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ba114-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ba114-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ba114-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ba114-115">Е</span><span class="sxs-lookup"><span data-stu-id="ba114-115">'T</span></span>

<span data-ttu-id="ba114-116">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="ba114-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="ba114-117">Пример</span><span class="sxs-lookup"><span data-stu-id="ba114-117">Example</span></span>

```qsharp
SquareArrayFact([[1, 2], [3, 4]], "Array is not a square");       // okay
SquareArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not a square"); // will fail
SquareArrayFact([[1, 2], [3, 4, 5]], "Array is not a square");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="ba114-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="ba114-118">See Also</span></span>

- [<span data-ttu-id="ba114-119">Microsoft. тактов. Arrays. Ректангулараррайфакт</span><span class="sxs-lookup"><span data-stu-id="ba114-119">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)