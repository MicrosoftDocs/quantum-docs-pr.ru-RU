---
uid: Microsoft.Quantum.Arrays.Most
title: Большинство функций
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 2b212b38ec55f3798eb9397f03b842573173eb88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845581"
---
# <a name="most-function"></a><span data-ttu-id="2552f-102">Большинство функций</span><span class="sxs-lookup"><span data-stu-id="2552f-102">Most function</span></span>

<span data-ttu-id="2552f-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2552f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2552f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2552f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2552f-105">Создает массив, равный входному массиву, за исключением того, что последний элемент массива удален.</span><span class="sxs-lookup"><span data-stu-id="2552f-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="2552f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2552f-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="2552f-107">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="2552f-107">array : 'T[]</span></span>

<span data-ttu-id="2552f-108">Массив, к элементам которого сначала приотносятся элементы, которые образуют выходной массив.</span><span class="sxs-lookup"><span data-stu-id="2552f-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="2552f-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="2552f-109">Output : 'T[]</span></span>

<span data-ttu-id="2552f-110">Массив, содержащий элементы `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="2552f-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="2552f-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="2552f-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2552f-112">Е</span><span class="sxs-lookup"><span data-stu-id="2552f-112">'T</span></span>

<span data-ttu-id="2552f-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="2552f-113">The type of the array elements.</span></span>