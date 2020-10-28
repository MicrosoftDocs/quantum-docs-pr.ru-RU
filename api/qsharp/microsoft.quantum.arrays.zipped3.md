---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Функция Zipped3
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: c0535ca4d6e0de13bf809a21e69d100dcb798d1f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729897"
---
# <a name="zipped3-function"></a><span data-ttu-id="eda21-102">Функция Zipped3</span><span class="sxs-lookup"><span data-stu-id="eda21-102">Zipped3 function</span></span>

<span data-ttu-id="eda21-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="eda21-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="eda21-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eda21-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eda21-105">При наличии трех массивов возвращает новый массив из трех кортежей, в которых каждый кортеж из трех элементов содержит элемент из каждого исходного массива.</span><span class="sxs-lookup"><span data-stu-id="eda21-105">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="eda21-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="eda21-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="eda21-107">Первый: 1 []</span><span class="sxs-lookup"><span data-stu-id="eda21-107">first : 'T1[]</span></span>

<span data-ttu-id="eda21-108">Массив, содержащий значения для первого элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="eda21-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="eda21-109">секунда: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="eda21-109">second : 'T2[]</span></span>

<span data-ttu-id="eda21-110">Массив, содержащий значения для второго элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="eda21-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="eda21-111">Третий: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="eda21-111">third : 'T3[]</span></span>

<span data-ttu-id="eda21-112">Массив, содержащий значения для третьего элемента каждого кортежа.</span><span class="sxs-lookup"><span data-stu-id="eda21-112">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="eda21-113">Выходные данные: ('T 1, е 2, 'T 3) []</span><span class="sxs-lookup"><span data-stu-id="eda21-113">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="eda21-114">Массив, содержащий три кортежа формы `(first[idx], second[idx], third[idx])` для каждого из них `idx` .</span><span class="sxs-lookup"><span data-stu-id="eda21-114">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="eda21-115">Если массивы имеют неравную длину, выходные данные будут иметь длину до более короткой из входных значений.</span><span class="sxs-lookup"><span data-stu-id="eda21-115">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="eda21-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="eda21-116">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="eda21-117">Т 1</span><span class="sxs-lookup"><span data-stu-id="eda21-117">'T1</span></span>

<span data-ttu-id="eda21-118">Тип первого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="eda21-118">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="eda21-119">Е 2</span><span class="sxs-lookup"><span data-stu-id="eda21-119">'T2</span></span>

<span data-ttu-id="eda21-120">Тип второго элемента массива.</span><span class="sxs-lookup"><span data-stu-id="eda21-120">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="eda21-121">Т 3</span><span class="sxs-lookup"><span data-stu-id="eda21-121">'T3</span></span>

<span data-ttu-id="eda21-122">Тип третьего элемента массива.</span><span class="sxs-lookup"><span data-stu-id="eda21-122">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="eda21-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="eda21-123">See Also</span></span>

- [<span data-ttu-id="eda21-124">Microsoft.Quantum.Arrays.Zipпед</span><span class="sxs-lookup"><span data-stu-id="eda21-124">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="eda21-125">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="eda21-125">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)