---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Функция Туплеаррайаснестедаррай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 51a35555080d1d2475fc1aa9e48e84c7c6f92c51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845394"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="d5e8c-102">Функция Туплеаррайаснестедаррай</span><span class="sxs-lookup"><span data-stu-id="d5e8c-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="d5e8c-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d5e8c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d5e8c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d5e8c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d5e8c-105">Включает список из двух кортежей в вложенный массив.</span><span class="sxs-lookup"><span data-stu-id="d5e8c-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="d5e8c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d5e8c-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="d5e8c-107">Туплелист: ('T) []</span><span class="sxs-lookup"><span data-stu-id="d5e8c-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="d5e8c-108">Список кортежей из двух элементов, которые должны быть преобразованы в вложенный массив.</span><span class="sxs-lookup"><span data-stu-id="d5e8c-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="d5e8c-109">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="d5e8c-109">Output : 'T[][]</span></span>

<span data-ttu-id="d5e8c-110">Вложенный массив с длиной, соответствующей Туплелист.</span><span class="sxs-lookup"><span data-stu-id="d5e8c-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="d5e8c-111">Пример</span><span class="sxs-lookup"><span data-stu-id="d5e8c-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="d5e8c-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d5e8c-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d5e8c-113">Е</span><span class="sxs-lookup"><span data-stu-id="d5e8c-113">'T</span></span>

