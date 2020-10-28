---
uid: Microsoft.Quantum.Arrays.Rest
title: Функция RESTful
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: c14e4b2902741d7ea70c895aa715cbcaa849af3e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730048"
---
# <a name="rest-function"></a><span data-ttu-id="e04de-102">Функция RESTful</span><span class="sxs-lookup"><span data-stu-id="e04de-102">Rest function</span></span>

<span data-ttu-id="e04de-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e04de-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e04de-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e04de-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e04de-105">Создает массив, равный входному массиву, за исключением того, что первый элемент массива удаляется.</span><span class="sxs-lookup"><span data-stu-id="e04de-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="e04de-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e04de-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="e04de-107">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="e04de-107">array : 'T[]</span></span>

<span data-ttu-id="e04de-108">Массив, второй с последними элементами которого образуют выходной массив.</span><span class="sxs-lookup"><span data-stu-id="e04de-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="e04de-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="e04de-109">Output : 'T[]</span></span>

<span data-ttu-id="e04de-110">Массив, содержащий элементы `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="e04de-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e04de-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e04de-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e04de-112">Е</span><span class="sxs-lookup"><span data-stu-id="e04de-112">'T</span></span>

<span data-ttu-id="e04de-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="e04de-113">The type of the array elements.</span></span>