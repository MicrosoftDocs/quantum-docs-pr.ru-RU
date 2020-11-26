---
uid: Microsoft.Quantum.Arrays.ForEach
title: Операция ForEach
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: b362d28e77c8dea2b3daeed4a4d605e1dd42e487
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221153"
---
# <a name="foreach-operation"></a><span data-ttu-id="6684f-102">Операция ForEach</span><span class="sxs-lookup"><span data-stu-id="6684f-102">ForEach operation</span></span>

<span data-ttu-id="6684f-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6684f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6684f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6684f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6684f-105">При наличии массива и операции, определенной для элементов массива, возвращает новый массив, состоящий из изображений исходного массива в операции.</span><span class="sxs-lookup"><span data-stu-id="6684f-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="6684f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6684f-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="6684f-107">действие: 'T => ' U</span><span class="sxs-lookup"><span data-stu-id="6684f-107">action : 'T => 'U</span></span> 

<span data-ttu-id="6684f-108">Операция из `'T` к `'U` , которая применяется к каждому элементу.</span><span class="sxs-lookup"><span data-stu-id="6684f-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="6684f-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="6684f-109">array : 'T[]</span></span>

<span data-ttu-id="6684f-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="6684f-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="6684f-111">Выходные данные: ' U []</span><span class="sxs-lookup"><span data-stu-id="6684f-111">Output : 'U[]</span></span>

<span data-ttu-id="6684f-112">Массив `'U[]` элементов, сопоставленных с `action` операцией.</span><span class="sxs-lookup"><span data-stu-id="6684f-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6684f-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="6684f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6684f-114">Е</span><span class="sxs-lookup"><span data-stu-id="6684f-114">'T</span></span>

<span data-ttu-id="6684f-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="6684f-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="6684f-116">' U</span><span class="sxs-lookup"><span data-stu-id="6684f-116">'U</span></span>

<span data-ttu-id="6684f-117">Тип результата `action` операции.</span><span class="sxs-lookup"><span data-stu-id="6684f-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6684f-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6684f-118">Remarks</span></span>

<span data-ttu-id="6684f-119">Операция определяется для универсальных типов, т. е. Если у нас есть массив `'T[]` и операция, `action : 'T -> 'U` которые мы можем сопоставлять элементы массива и создаем новый массив типа `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="6684f-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>