---
uid: Microsoft.Quantum.Arrays.Rest
title: Функция RESTful
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: 4dd10b6e8839fd906ca9c2e36c89c626d5772149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220402"
---
# <a name="rest-function"></a><span data-ttu-id="aa523-102">Функция RESTful</span><span class="sxs-lookup"><span data-stu-id="aa523-102">Rest function</span></span>

<span data-ttu-id="aa523-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aa523-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aa523-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa523-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa523-105">Создает массив, равный входному массиву, за исключением того, что первый элемент массива удаляется.</span><span class="sxs-lookup"><span data-stu-id="aa523-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="aa523-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aa523-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="aa523-107">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="aa523-107">array : 'T[]</span></span>

<span data-ttu-id="aa523-108">Массив, второй с последними элементами которого образуют выходной массив.</span><span class="sxs-lookup"><span data-stu-id="aa523-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="aa523-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="aa523-109">Output : 'T[]</span></span>

<span data-ttu-id="aa523-110">Массив, содержащий элементы `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="aa523-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="aa523-111">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="aa523-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aa523-112">Е</span><span class="sxs-lookup"><span data-stu-id="aa523-112">'T</span></span>

<span data-ttu-id="aa523-113">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="aa523-113">The type of the array elements.</span></span>