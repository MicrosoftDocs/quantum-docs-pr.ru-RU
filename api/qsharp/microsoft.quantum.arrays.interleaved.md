---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Функция с чередованием
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220966"
---
# <a name="interleaved-function"></a><span data-ttu-id="25d39-102">Функция с чередованием</span><span class="sxs-lookup"><span data-stu-id="25d39-102">Interleaved function</span></span>

<span data-ttu-id="25d39-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="25d39-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="25d39-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25d39-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25d39-105">Покидает два массива (почти) одинакового размера.</span><span class="sxs-lookup"><span data-stu-id="25d39-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="25d39-106">Описание</span><span class="sxs-lookup"><span data-stu-id="25d39-106">Description</span></span>

<span data-ttu-id="25d39-107">Эта функция возвращает два массива, начиная с первого элемента из первого массива, затем первый элемент из второго массива и т. д.</span><span class="sxs-lookup"><span data-stu-id="25d39-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="25d39-108">Первый массив должен иметь длину, равную второму, или может иметь еще один элемент.</span><span class="sxs-lookup"><span data-stu-id="25d39-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="25d39-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="25d39-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="25d39-110">Первый: 'T []</span><span class="sxs-lookup"><span data-stu-id="25d39-110">first : 'T[]</span></span>

<span data-ttu-id="25d39-111">Первый массив для чередования.</span><span class="sxs-lookup"><span data-stu-id="25d39-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="25d39-112">секунда: 'T []</span><span class="sxs-lookup"><span data-stu-id="25d39-112">second : 'T[]</span></span>

<span data-ttu-id="25d39-113">Второй массив для чередования.</span><span class="sxs-lookup"><span data-stu-id="25d39-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="25d39-114">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="25d39-114">Output : 'T[]</span></span>

<span data-ttu-id="25d39-115">Массив с чередованием</span><span class="sxs-lookup"><span data-stu-id="25d39-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="25d39-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="25d39-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="25d39-117">Е</span><span class="sxs-lookup"><span data-stu-id="25d39-117">'T</span></span>

<span data-ttu-id="25d39-118">Тип каждого элемента `first` и `second` .</span><span class="sxs-lookup"><span data-stu-id="25d39-118">The type of each element of `first` and `second`.</span></span>