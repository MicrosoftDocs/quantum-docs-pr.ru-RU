---
uid: Microsoft.Quantum.Arrays.Zip4
title: Функция Zip4
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d42b3b6db059163f6c766d4f133551be293c153d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729904"
---
# <a name="zip4-function"></a><span data-ttu-id="17ec6-102">Функция Zip4</span><span class="sxs-lookup"><span data-stu-id="17ec6-102">Zip4 function</span></span>

<span data-ttu-id="17ec6-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="17ec6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="17ec6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17ec6-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="17ec6-105">Zip4 является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="17ec6-105">Zip4 has been deprecated.</span></span> <span data-ttu-id="17ec6-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped4>.</span><span class="sxs-lookup"><span data-stu-id="17ec6-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.</span></span>

<span data-ttu-id="17ec6-107">При наличии четырех массивов возвращает новый массив из 4 кортежей таким, что каждый 4 кортежа содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="17ec6-107">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="17ec6-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="17ec6-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="17ec6-109">Первый: 1 []</span><span class="sxs-lookup"><span data-stu-id="17ec6-109">first : 'T1[]</span></span>

<span data-ttu-id="17ec6-110">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="17ec6-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="17ec6-111">секунда: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="17ec6-111">second : 'T2[]</span></span>

<span data-ttu-id="17ec6-112">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="17ec6-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="17ec6-113">Третий: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="17ec6-113">third : 'T3[]</span></span>

<span data-ttu-id="17ec6-114">Массив, содержащий значения для третьего элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="17ec6-114">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="17ec6-115">четвертый: 'T 4 []</span><span class="sxs-lookup"><span data-stu-id="17ec6-115">fourth : 'T4[]</span></span>

<span data-ttu-id="17ec6-116">Массив, содержащий значения для четвертого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="17ec6-116">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="17ec6-117">Выходные данные: (т. е. 1, 'T 2, No 3, 'T 4) []</span><span class="sxs-lookup"><span data-stu-id="17ec6-117">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="17ec6-118">Массив, содержащий 4 кортежа формы `(first[idx], second[idx], third[idx], fourth[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="17ec6-118">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="17ec6-119">Если четыре массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="17ec6-119">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="17ec6-120">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="17ec6-120">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="17ec6-121">Т 1</span><span class="sxs-lookup"><span data-stu-id="17ec6-121">'T1</span></span>

<span data-ttu-id="17ec6-122">Тип первого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="17ec6-122">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="17ec6-123">Е 2</span><span class="sxs-lookup"><span data-stu-id="17ec6-123">'T2</span></span>

<span data-ttu-id="17ec6-124">Тип второго элемента массива.</span><span class="sxs-lookup"><span data-stu-id="17ec6-124">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="17ec6-125">Т 3</span><span class="sxs-lookup"><span data-stu-id="17ec6-125">'T3</span></span>

<span data-ttu-id="17ec6-126">Тип третьего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="17ec6-126">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="17ec6-127">No 4</span><span class="sxs-lookup"><span data-stu-id="17ec6-127">'T4</span></span>

<span data-ttu-id="17ec6-128">Тип четвертых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="17ec6-128">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="17ec6-129">См. также:</span><span class="sxs-lookup"><span data-stu-id="17ec6-129">See Also</span></span>

- [<span data-ttu-id="17ec6-130">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="17ec6-130">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="17ec6-131">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="17ec6-131">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)