---
uid: Microsoft.Quantum.Arrays.Most
title: Большинство функций
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730104"
---
# <a name="most-function"></a><span data-ttu-id="7783c-102">Большинство функций</span><span class="sxs-lookup"><span data-stu-id="7783c-102">Most function</span></span>

<span data-ttu-id="7783c-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7783c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7783c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7783c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7783c-105">Создает массив, равный входному массиву, за исключением того, что последний элемент массива удален.</span><span class="sxs-lookup"><span data-stu-id="7783c-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="7783c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7783c-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="7783c-107">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="7783c-107">array : 'T[]</span></span>

<span data-ttu-id="7783c-108">Массив, к элементам которого сначала приотносятся элементы, которые образуют выходной массив.</span><span class="sxs-lookup"><span data-stu-id="7783c-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="7783c-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="7783c-109">Output : 'T[]</span></span>

<span data-ttu-id="7783c-110">Массив, содержащий элементы `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="7783c-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7783c-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7783c-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7783c-112">Е</span><span class="sxs-lookup"><span data-stu-id="7783c-112">'T</span></span>

<span data-ttu-id="7783c-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="7783c-113">The type of the array elements.</span></span>