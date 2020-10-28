---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Функция Скуареаррайфакт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: f7f0573db9098feebfd481624e11119c58fd9eed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730008"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="28e5a-102">Функция Скуареаррайфакт</span><span class="sxs-lookup"><span data-stu-id="28e5a-102">SquareArrayFact function</span></span>

<span data-ttu-id="28e5a-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="28e5a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="28e5a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="28e5a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="28e5a-105">Представляет условие, которое двумерный массив имеет квадратную фигуру</span><span class="sxs-lookup"><span data-stu-id="28e5a-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="28e5a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="28e5a-106">Description</span></span>

<span data-ttu-id="28e5a-107">Эта функция утверждает, что каждая строка в массиве содержит столько элементов, сколько строк (элементов) в массиве.</span><span class="sxs-lookup"><span data-stu-id="28e5a-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="28e5a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="28e5a-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="28e5a-109">массив: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="28e5a-109">array : 'T[][]</span></span>

<span data-ttu-id="28e5a-110">Двухмерный массив элементов</span><span class="sxs-lookup"><span data-stu-id="28e5a-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="28e5a-111">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="28e5a-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="28e5a-112">Выводимое сообщение, если массив не является квадратным массивом</span><span class="sxs-lookup"><span data-stu-id="28e5a-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="28e5a-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="28e5a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="28e5a-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="28e5a-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="28e5a-115">Е</span><span class="sxs-lookup"><span data-stu-id="28e5a-115">'T</span></span>

<span data-ttu-id="28e5a-116">Тип каждого элемента `array` .</span><span class="sxs-lookup"><span data-stu-id="28e5a-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="28e5a-117">См. также:</span><span class="sxs-lookup"><span data-stu-id="28e5a-117">See Also</span></span>

- [<span data-ttu-id="28e5a-118">Microsoft. тактов. Arrays. Ректангулараррайфакт</span><span class="sxs-lookup"><span data-stu-id="28e5a-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)