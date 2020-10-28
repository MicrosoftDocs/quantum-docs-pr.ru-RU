---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Функция с чередованием
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730200"
---
# <a name="interleaved-function"></a><span data-ttu-id="3d4a3-102">Функция с чередованием</span><span class="sxs-lookup"><span data-stu-id="3d4a3-102">Interleaved function</span></span>

<span data-ttu-id="3d4a3-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3d4a3-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3d4a3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3d4a3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3d4a3-105">Покидает два массива (почти) одинакового размера.</span><span class="sxs-lookup"><span data-stu-id="3d4a3-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="3d4a3-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3d4a3-106">Description</span></span>

<span data-ttu-id="3d4a3-107">Эта функция возвращает два массива, начиная с первого элемента из первого массива, затем первый элемент из второго массива и т. д.</span><span class="sxs-lookup"><span data-stu-id="3d4a3-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="3d4a3-108">Первый массив должен иметь длину, равную второму, или может иметь еще один элемент.</span><span class="sxs-lookup"><span data-stu-id="3d4a3-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="3d4a3-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3d4a3-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="3d4a3-110">Первый: 'T []</span><span class="sxs-lookup"><span data-stu-id="3d4a3-110">first : 'T[]</span></span>

<span data-ttu-id="3d4a3-111">Первый массив для чередования.</span><span class="sxs-lookup"><span data-stu-id="3d4a3-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="3d4a3-112">секунда: 'T []</span><span class="sxs-lookup"><span data-stu-id="3d4a3-112">second : 'T[]</span></span>

<span data-ttu-id="3d4a3-113">Второй массив для чередования.</span><span class="sxs-lookup"><span data-stu-id="3d4a3-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="3d4a3-114">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="3d4a3-114">Output : 'T[]</span></span>

<span data-ttu-id="3d4a3-115">Массив с чередованием</span><span class="sxs-lookup"><span data-stu-id="3d4a3-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3d4a3-116">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3d4a3-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3d4a3-117">Е</span><span class="sxs-lookup"><span data-stu-id="3d4a3-117">'T</span></span>

<span data-ttu-id="3d4a3-118">Тип каждого элемента `first` и `second` .</span><span class="sxs-lookup"><span data-stu-id="3d4a3-118">The type of each element of `first` and `second`.</span></span>