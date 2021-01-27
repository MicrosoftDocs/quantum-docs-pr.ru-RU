---
uid: Microsoft.Quantum.Arrays.Zip3
title: Функция zip3
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: b41b0789cdf90db534ee7a50ff25eb3a931ec683
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845356"
---
# <a name="zip3-function"></a><span data-ttu-id="8911d-102">Функция zip3</span><span class="sxs-lookup"><span data-stu-id="8911d-102">Zip3 function</span></span>

<span data-ttu-id="8911d-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8911d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8911d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8911d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="8911d-105">Zip3 является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="8911d-105">Zip3 has been deprecated.</span></span> <span data-ttu-id="8911d-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped3>.</span><span class="sxs-lookup"><span data-stu-id="8911d-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.</span></span>

<span data-ttu-id="8911d-107">При наличии трех массивов возвращает новый массив из трех кортежей, в которых каждый кортеж из трех элементов содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="8911d-107">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="8911d-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8911d-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="8911d-109">Первый: 1 []</span><span class="sxs-lookup"><span data-stu-id="8911d-109">first : 'T1[]</span></span>

<span data-ttu-id="8911d-110">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="8911d-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="8911d-111">секунда: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="8911d-111">second : 'T2[]</span></span>

<span data-ttu-id="8911d-112">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="8911d-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="8911d-113">Третий: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="8911d-113">third : 'T3[]</span></span>

<span data-ttu-id="8911d-114">Массив, содержащий значения для третьего элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="8911d-114">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="8911d-115">Выходные данные: ('T 1, е 2, 'T 3) []</span><span class="sxs-lookup"><span data-stu-id="8911d-115">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="8911d-116">Массив, содержащий три кортежа формы `(first[idx], second[idx], third[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="8911d-116">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="8911d-117">Если массивы имеют неравную длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="8911d-117">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8911d-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8911d-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="8911d-119">Т 1</span><span class="sxs-lookup"><span data-stu-id="8911d-119">'T1</span></span>

<span data-ttu-id="8911d-120">Тип первого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="8911d-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="8911d-121">Е 2</span><span class="sxs-lookup"><span data-stu-id="8911d-121">'T2</span></span>

<span data-ttu-id="8911d-122">Тип второго элемента массива.</span><span class="sxs-lookup"><span data-stu-id="8911d-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="8911d-123">Т 3</span><span class="sxs-lookup"><span data-stu-id="8911d-123">'T3</span></span>

<span data-ttu-id="8911d-124">Тип третьего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="8911d-124">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="8911d-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="8911d-125">See Also</span></span>

- [<span data-ttu-id="8911d-126">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="8911d-126">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="8911d-127">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="8911d-127">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)