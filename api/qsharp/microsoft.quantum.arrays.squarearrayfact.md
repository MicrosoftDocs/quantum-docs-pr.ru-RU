---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Функция Скуареаррайфакт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: 3529718f0c903266d21fd593c11c0149dae0fa2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220201"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="7db87-102">Функция Скуареаррайфакт</span><span class="sxs-lookup"><span data-stu-id="7db87-102">SquareArrayFact function</span></span>

<span data-ttu-id="7db87-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7db87-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7db87-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7db87-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7db87-105">Представляет условие, которое двумерный массив имеет квадратную фигуру</span><span class="sxs-lookup"><span data-stu-id="7db87-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="7db87-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7db87-106">Description</span></span>

<span data-ttu-id="7db87-107">Эта функция утверждает, что каждая строка в массиве содержит столько элементов, сколько строк (элементов) в массиве.</span><span class="sxs-lookup"><span data-stu-id="7db87-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="7db87-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7db87-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="7db87-109">массив: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="7db87-109">array : 'T[][]</span></span>

<span data-ttu-id="7db87-110">Двухмерный массив элементов</span><span class="sxs-lookup"><span data-stu-id="7db87-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="7db87-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="7db87-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="7db87-112">Выводимое сообщение, если массив не является квадратным массивом</span><span class="sxs-lookup"><span data-stu-id="7db87-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="7db87-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7db87-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="7db87-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7db87-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7db87-115">Е</span><span class="sxs-lookup"><span data-stu-id="7db87-115">'T</span></span>

<span data-ttu-id="7db87-116">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="7db87-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="7db87-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="7db87-117">See Also</span></span>

- [<span data-ttu-id="7db87-118">Microsoft. тактов. Arrays. Ректангулараррайфакт</span><span class="sxs-lookup"><span data-stu-id="7db87-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)