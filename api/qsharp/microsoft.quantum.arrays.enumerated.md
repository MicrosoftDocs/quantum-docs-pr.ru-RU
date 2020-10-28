---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Функция Enumerate
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730305"
---
# <a name="enumerated-function"></a><span data-ttu-id="10d3c-102">Функция Enumerate</span><span class="sxs-lookup"><span data-stu-id="10d3c-102">Enumerated function</span></span>

<span data-ttu-id="10d3c-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="10d3c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="10d3c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10d3c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10d3c-105">При наличии массива возвращает новый массив, содержащий элементы исходного массива вместе с индексами каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="10d3c-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="10d3c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="10d3c-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="10d3c-107">массив: ' TElement []</span><span class="sxs-lookup"><span data-stu-id="10d3c-107">array : 'TElement[]</span></span>

<span data-ttu-id="10d3c-108">Массив, элементы которого необходимо перечислить.</span><span class="sxs-lookup"><span data-stu-id="10d3c-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="10d3c-109">Выходные данные: ([int](xref:microsoft.quantum.lang-ref.int), ' TElement ') []</span><span class="sxs-lookup"><span data-stu-id="10d3c-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="10d3c-110">Новый массив, содержащий элементы исходного массива вместе с их индексами.</span><span class="sxs-lookup"><span data-stu-id="10d3c-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="10d3c-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="10d3c-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="10d3c-112">' TElement</span><span class="sxs-lookup"><span data-stu-id="10d3c-112">'TElement</span></span>

<span data-ttu-id="10d3c-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="10d3c-113">The type of elements of the array.</span></span>