---
uid: Microsoft.Quantum.Arrays.ForEach
title: Операция ForEach
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730240"
---
# <a name="foreach-operation"></a><span data-ttu-id="9cc58-102">Операция ForEach</span><span class="sxs-lookup"><span data-stu-id="9cc58-102">ForEach operation</span></span>

<span data-ttu-id="9cc58-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9cc58-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9cc58-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9cc58-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9cc58-105">При наличии массива и операции, определенной для элементов массива, возвращает новый массив, состоящий из изображений исходного массива в операции.</span><span class="sxs-lookup"><span data-stu-id="9cc58-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="9cc58-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9cc58-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="9cc58-107">действие: 'T => ' U</span><span class="sxs-lookup"><span data-stu-id="9cc58-107">action : 'T => 'U</span></span> 

<span data-ttu-id="9cc58-108">Операция из `'T` к `'U` , которая применяется к каждому элементу.</span><span class="sxs-lookup"><span data-stu-id="9cc58-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="9cc58-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="9cc58-109">array : 'T[]</span></span>

<span data-ttu-id="9cc58-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="9cc58-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="9cc58-111">Выходные данные: ' U []</span><span class="sxs-lookup"><span data-stu-id="9cc58-111">Output : 'U[]</span></span>

<span data-ttu-id="9cc58-112">Массив `'U[]` элементов, сопоставленных с `action` операцией.</span><span class="sxs-lookup"><span data-stu-id="9cc58-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9cc58-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="9cc58-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9cc58-114">Е</span><span class="sxs-lookup"><span data-stu-id="9cc58-114">'T</span></span>

<span data-ttu-id="9cc58-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="9cc58-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="9cc58-116">' U</span><span class="sxs-lookup"><span data-stu-id="9cc58-116">'U</span></span>

<span data-ttu-id="9cc58-117">Тип результата `action` операции.</span><span class="sxs-lookup"><span data-stu-id="9cc58-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc58-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="9cc58-118">Remarks</span></span>

<span data-ttu-id="9cc58-119">Операция определяется для универсальных типов, т. е. Если у нас есть массив `'T[]` и операция, `action : 'T -> 'U` которые мы можем сопоставлять элементы массива и создаем новый массив типа `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="9cc58-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>