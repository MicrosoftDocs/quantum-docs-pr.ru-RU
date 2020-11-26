---
uid: Microsoft.Quantum.Arrays.Zipped
title: Функция ZIP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 56ed97d573bf29dddb7cdb1c3f360218bf97889a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219759"
---
# <a name="zipped-function"></a><span data-ttu-id="1cc8f-102">Функция ZIP</span><span class="sxs-lookup"><span data-stu-id="1cc8f-102">Zipped function</span></span>

<span data-ttu-id="1cc8f-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1cc8f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1cc8f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1cc8f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1cc8f-105">При наличии двух массивов возвращает новый массив пар, в котором каждая пара содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="1cc8f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1cc8f-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="1cc8f-107">Left: ' ' []</span><span class="sxs-lookup"><span data-stu-id="1cc8f-107">left : 'T[]</span></span>

<span data-ttu-id="1cc8f-108">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="1cc8f-109">Right: ' U []</span><span class="sxs-lookup"><span data-stu-id="1cc8f-109">right : 'U[]</span></span>

<span data-ttu-id="1cc8f-110">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="1cc8f-111">Выходные данные: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="1cc8f-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="1cc8f-112">Массив, содержащий пары форм `(left[idx], right[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="1cc8f-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="1cc8f-113">Если два массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1cc8f-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="1cc8f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1cc8f-115">Е</span><span class="sxs-lookup"><span data-stu-id="1cc8f-115">'T</span></span>

<span data-ttu-id="1cc8f-116">Тип элементов левого массива.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="1cc8f-117">' U</span><span class="sxs-lookup"><span data-stu-id="1cc8f-117">'U</span></span>

<span data-ttu-id="1cc8f-118">Тип правых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-118">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cc8f-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="1cc8f-119">See Also</span></span>

- [<span data-ttu-id="1cc8f-120">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="1cc8f-120">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="1cc8f-121">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="1cc8f-121">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="1cc8f-122">Microsoft. тактов. Arrays. unzipped</span><span class="sxs-lookup"><span data-stu-id="1cc8f-122">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)