---
uid: Microsoft.Quantum.Arrays.Reversed
title: Обратная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 99244195e581dc00db24b938f5aa1c541cd4433a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730041"
---
# <a name="reversed-function"></a><span data-ttu-id="c48fe-102">Обратная функция</span><span class="sxs-lookup"><span data-stu-id="c48fe-102">Reversed function</span></span>

<span data-ttu-id="c48fe-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c48fe-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c48fe-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c48fe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c48fe-105">Создайте массив, содержащий те же элементы, что и входной массив, но в обратный порядок.</span><span class="sxs-lookup"><span data-stu-id="c48fe-105">Create an array that contains the same elements as an input array but in Reversed order.</span></span>

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="c48fe-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c48fe-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="c48fe-107">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="c48fe-107">array : 'T[]</span></span>

<span data-ttu-id="c48fe-108">Массив, элементы которого должны быть скопированы в обратный порядок.</span><span class="sxs-lookup"><span data-stu-id="c48fe-108">An array whose elements are to be copied in Reversed order.</span></span>



## <a name="output--t"></a><span data-ttu-id="c48fe-109">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="c48fe-109">Output : 'T[]</span></span>

<span data-ttu-id="c48fe-110">Массив, содержащий элементы `array[Length(array) - 1]` ..</span><span class="sxs-lookup"><span data-stu-id="c48fe-110">An array containing the elements `array[Length(array) - 1]` ..</span></span> <span data-ttu-id="c48fe-111">`array[0]`.</span><span class="sxs-lookup"><span data-stu-id="c48fe-111">`array[0]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c48fe-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c48fe-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c48fe-113">Е</span><span class="sxs-lookup"><span data-stu-id="c48fe-113">'T</span></span>

<span data-ttu-id="c48fe-114">Тип элементов массива.</span><span class="sxs-lookup"><span data-stu-id="c48fe-114">The type of the array elements.</span></span>