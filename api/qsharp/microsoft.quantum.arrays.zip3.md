---
uid: Microsoft.Quantum.Arrays.Zip3
title: Функция zip3
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: f4b1a769614ee9434b2141b8fcb91f34cd071bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729920"
---
# <a name="zip3-function"></a><span data-ttu-id="29dd5-102">Функция zip3</span><span class="sxs-lookup"><span data-stu-id="29dd5-102">Zip3 function</span></span>

<span data-ttu-id="29dd5-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="29dd5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="29dd5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="29dd5-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="29dd5-105">Zip3 является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="29dd5-105">Zip3 has been deprecated.</span></span> <span data-ttu-id="29dd5-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped3>.</span><span class="sxs-lookup"><span data-stu-id="29dd5-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.</span></span>

<span data-ttu-id="29dd5-107">При наличии трех массивов возвращает новый массив из трех кортежей, в которых каждый кортеж из трех элементов содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="29dd5-107">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="29dd5-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="29dd5-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="29dd5-109">Первый: 1 []</span><span class="sxs-lookup"><span data-stu-id="29dd5-109">first : 'T1[]</span></span>

<span data-ttu-id="29dd5-110">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="29dd5-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="29dd5-111">секунда: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="29dd5-111">second : 'T2[]</span></span>

<span data-ttu-id="29dd5-112">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="29dd5-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="29dd5-113">Третий: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="29dd5-113">third : 'T3[]</span></span>

<span data-ttu-id="29dd5-114">Массив, содержащий значения для третьего элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="29dd5-114">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="29dd5-115">Выходные данные: ('T 1, е 2, 'T 3) []</span><span class="sxs-lookup"><span data-stu-id="29dd5-115">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="29dd5-116">Массив, содержащий три кортежа формы `(first[idx], second[idx], third[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="29dd5-116">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="29dd5-117">Если массивы имеют неравную длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="29dd5-117">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="29dd5-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="29dd5-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="29dd5-119">Т 1</span><span class="sxs-lookup"><span data-stu-id="29dd5-119">'T1</span></span>

<span data-ttu-id="29dd5-120">Тип первого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="29dd5-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="29dd5-121">Е 2</span><span class="sxs-lookup"><span data-stu-id="29dd5-121">'T2</span></span>

<span data-ttu-id="29dd5-122">Тип второго элемента массива.</span><span class="sxs-lookup"><span data-stu-id="29dd5-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="29dd5-123">Т 3</span><span class="sxs-lookup"><span data-stu-id="29dd5-123">'T3</span></span>

<span data-ttu-id="29dd5-124">Тип третьего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="29dd5-124">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="29dd5-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="29dd5-125">See Also</span></span>

- [<span data-ttu-id="29dd5-126">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="29dd5-126">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="29dd5-127">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="29dd5-127">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)