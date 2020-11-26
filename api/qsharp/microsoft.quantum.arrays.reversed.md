---
uid: Microsoft.Quantum.Arrays.Reversed
title: Обратная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 270f15c1d10b4397e258c750876095efc2b8e951
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220439"
---
# <a name="reversed-function"></a><span data-ttu-id="c9c10-102">Обратная функция</span><span class="sxs-lookup"><span data-stu-id="c9c10-102">Reversed function</span></span>

<span data-ttu-id="c9c10-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c9c10-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c9c10-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c9c10-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c9c10-105">Создайте массив, содержащий те же элементы, что и входной массив, но в обратный порядок.</span><span class="sxs-lookup"><span data-stu-id="c9c10-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="c9c10-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c9c10-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="c9c10-107">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="c9c10-107">array : 'T[]</span></span>

<span data-ttu-id="c9c10-108">Массив, элементы которого должны быть скопированы в обратный порядок.</span><span class="sxs-lookup"><span data-stu-id="c9c10-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="c9c10-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="c9c10-109">Output : 'T[]</span></span>

<span data-ttu-id="c9c10-110">Массив, содержащий элементы `array[Length(array) - 1]` ..</span><span class="sxs-lookup"><span data-stu-id="c9c10-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="c9c10-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="c9c10-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c9c10-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c9c10-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c9c10-113">Е</span><span class="sxs-lookup"><span data-stu-id="c9c10-113">'T</span></span>

<span data-ttu-id="c9c10-114">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="c9c10-114">The type of the array elements.</span></span>