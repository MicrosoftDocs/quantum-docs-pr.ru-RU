---
uid: Microsoft.Quantum.Arrays.Zipped4
title: Функция Zipped4
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: e932cd4c266b39a3a88da48e649448d0028f61e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845332"
---
# <a name="zipped4-function"></a><span data-ttu-id="9b340-102">Функция Zipped4</span><span class="sxs-lookup"><span data-stu-id="9b340-102">Zipped4 function</span></span>

<span data-ttu-id="9b340-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9b340-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9b340-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b340-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b340-105">При наличии четырех массивов возвращает новый массив из 4 кортежей таким, что каждый 4 кортежа содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="9b340-105">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="9b340-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9b340-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="9b340-107">Первый: 1 []</span><span class="sxs-lookup"><span data-stu-id="9b340-107">first : 'T1[]</span></span>

<span data-ttu-id="9b340-108">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="9b340-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="9b340-109">секунда: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="9b340-109">second : 'T2[]</span></span>

<span data-ttu-id="9b340-110">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="9b340-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="9b340-111">Третий: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="9b340-111">third : 'T3[]</span></span>

<span data-ttu-id="9b340-112">Массив, содержащий значения для третьего элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="9b340-112">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="9b340-113">четвертый: 'T 4 []</span><span class="sxs-lookup"><span data-stu-id="9b340-113">fourth : 'T4[]</span></span>

<span data-ttu-id="9b340-114">Массив, содержащий значения для четвертого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="9b340-114">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="9b340-115">Выходные данные: (т. е. 1, 'T 2, No 3, 'T 4) []</span><span class="sxs-lookup"><span data-stu-id="9b340-115">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="9b340-116">Массив, содержащий 4 кортежа формы `(first[idx], second[idx], third[idx], fourth[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="9b340-116">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="9b340-117">Если четыре массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="9b340-117">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9b340-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="9b340-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="9b340-119">Т 1</span><span class="sxs-lookup"><span data-stu-id="9b340-119">'T1</span></span>

<span data-ttu-id="9b340-120">Тип первого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="9b340-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="9b340-121">Е 2</span><span class="sxs-lookup"><span data-stu-id="9b340-121">'T2</span></span>

<span data-ttu-id="9b340-122">Тип второго элемента массива.</span><span class="sxs-lookup"><span data-stu-id="9b340-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="9b340-123">Т 3</span><span class="sxs-lookup"><span data-stu-id="9b340-123">'T3</span></span>

<span data-ttu-id="9b340-124">Тип третьего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="9b340-124">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="9b340-125">No 4</span><span class="sxs-lookup"><span data-stu-id="9b340-125">'T4</span></span>

<span data-ttu-id="9b340-126">Тип четвертых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="9b340-126">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b340-127">См. также:</span><span class="sxs-lookup"><span data-stu-id="9b340-127">See Also</span></span>

- [<span data-ttu-id="9b340-128">Microsoft.Quantum.Arrays.Zipпед</span><span class="sxs-lookup"><span data-stu-id="9b340-128">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="9b340-129">Microsoft.Quantum.Arrays.Zipped3</span><span class="sxs-lookup"><span data-stu-id="9b340-129">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)