---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Функция Ректангулараррайфакт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220422"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="dd8be-102">Функция Ректангулараррайфакт</span><span class="sxs-lookup"><span data-stu-id="dd8be-102">RectangularArrayFact function</span></span>

<span data-ttu-id="dd8be-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dd8be-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dd8be-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dd8be-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dd8be-105">Представляет условие, в котором двухмерный массив имеет прямоугольную фигуру</span><span class="sxs-lookup"><span data-stu-id="dd8be-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="dd8be-106">Описание</span><span class="sxs-lookup"><span data-stu-id="dd8be-106">Description</span></span>

<span data-ttu-id="dd8be-107">Эта функция утверждает, что каждая строка в массиве имеет одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="dd8be-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="dd8be-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dd8be-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="dd8be-109">массив: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="dd8be-109">array : 'T[][]</span></span>

<span data-ttu-id="dd8be-110">Двухмерный массив элементов</span><span class="sxs-lookup"><span data-stu-id="dd8be-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="dd8be-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="dd8be-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="dd8be-112">Выводимое сообщение, если массив не является прямоугольным массивом</span><span class="sxs-lookup"><span data-stu-id="dd8be-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="dd8be-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dd8be-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dd8be-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="dd8be-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dd8be-115">Е</span><span class="sxs-lookup"><span data-stu-id="dd8be-115">'T</span></span>

<span data-ttu-id="dd8be-116">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="dd8be-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd8be-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="dd8be-117">See Also</span></span>

- [<span data-ttu-id="dd8be-118">Microsoft. тактов. Arrays. Скуареаррайфакт</span><span class="sxs-lookup"><span data-stu-id="dd8be-118">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)