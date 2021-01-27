---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Функция с чередованием
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 3605c0d0bc43cdb1097d025861c3ec2424763c86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848111"
---
# <a name="interleaved-function"></a><span data-ttu-id="a0ff7-102">Функция с чередованием</span><span class="sxs-lookup"><span data-stu-id="a0ff7-102">Interleaved function</span></span>

<span data-ttu-id="a0ff7-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a0ff7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0ff7-105">Покидает два массива (почти) одинакового размера.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="a0ff7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a0ff7-106">Description</span></span>

<span data-ttu-id="a0ff7-107">Эта функция возвращает два массива, начиная с первого элемента из первого массива, затем первый элемент из второго массива и т. д.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="a0ff7-108">Первый массив должен иметь длину, равную второму, или может иметь еще один элемент.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="a0ff7-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a0ff7-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="a0ff7-110">Первый: 'T []</span><span class="sxs-lookup"><span data-stu-id="a0ff7-110">first : 'T[]</span></span>

<span data-ttu-id="a0ff7-111">Первый массив для чередования.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="a0ff7-112">секунда: 'T []</span><span class="sxs-lookup"><span data-stu-id="a0ff7-112">second : 'T[]</span></span>

<span data-ttu-id="a0ff7-113">Второй массив для чередования.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="a0ff7-114">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="a0ff7-114">Output : 'T[]</span></span>

<span data-ttu-id="a0ff7-115">Массив с чередованием</span><span class="sxs-lookup"><span data-stu-id="a0ff7-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a0ff7-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="a0ff7-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a0ff7-117">Е</span><span class="sxs-lookup"><span data-stu-id="a0ff7-117">'T</span></span>

<span data-ttu-id="a0ff7-118">Тип каждого элемента `first` и `second` .</span><span class="sxs-lookup"><span data-stu-id="a0ff7-118">The type of each element of `first` and `second`.</span></span>

## <a name="example"></a><span data-ttu-id="a0ff7-119">Пример</span><span class="sxs-lookup"><span data-stu-id="a0ff7-119">Example</span></span>

```qsharp
// same as int1 = [1, -1, 2, -2, 3, -3]
let int1 = Interleaved([1, 2, 3], [-1, -2, -3])

// same as int2 = [false, true, false, true, false]
let int2 = Interleaved(ConstantArray(3, false), ConstantArray(2, true));
```