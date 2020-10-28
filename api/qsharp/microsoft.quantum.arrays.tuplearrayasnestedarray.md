---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Функция Туплеаррайаснестедаррай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729976"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="83b30-102">Функция Туплеаррайаснестедаррай</span><span class="sxs-lookup"><span data-stu-id="83b30-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="83b30-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="83b30-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="83b30-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="83b30-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="83b30-105">Включает список из двух кортежей в вложенный массив.</span><span class="sxs-lookup"><span data-stu-id="83b30-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="83b30-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="83b30-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="83b30-107">Туплелист: ('T) []</span><span class="sxs-lookup"><span data-stu-id="83b30-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="83b30-108">Список кортежей из двух элементов, которые должны быть преобразованы в вложенный массив.</span><span class="sxs-lookup"><span data-stu-id="83b30-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="83b30-109">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="83b30-109">Output : 'T[][]</span></span>

<span data-ttu-id="83b30-110">Вложенный массив с длиной, соответствующей Туплелист.</span><span class="sxs-lookup"><span data-stu-id="83b30-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="83b30-111">Например, .</span><span class="sxs-lookup"><span data-stu-id="83b30-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="83b30-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="83b30-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="83b30-113">Е</span><span class="sxs-lookup"><span data-stu-id="83b30-113">'T</span></span>

