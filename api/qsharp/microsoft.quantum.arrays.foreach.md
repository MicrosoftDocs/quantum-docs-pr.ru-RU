---
uid: Microsoft.Quantum.Arrays.ForEach
title: Операция ForEach
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: 90dd6f94408d37d2b32d82e772a482b0e69c523f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848581"
---
# <a name="foreach-operation"></a><span data-ttu-id="b7a21-102">Операция ForEach</span><span class="sxs-lookup"><span data-stu-id="b7a21-102">ForEach operation</span></span>

<span data-ttu-id="b7a21-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b7a21-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b7a21-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b7a21-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b7a21-105">При наличии массива и операции, определенной для элементов массива, возвращает новый массив, состоящий из изображений исходного массива в операции.</span><span class="sxs-lookup"><span data-stu-id="b7a21-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="b7a21-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b7a21-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="b7a21-107">действие: 'T => ' U</span><span class="sxs-lookup"><span data-stu-id="b7a21-107">action : 'T => 'U</span></span> 

<span data-ttu-id="b7a21-108">Операция из `'T` к `'U` , которая применяется к каждому элементу.</span><span class="sxs-lookup"><span data-stu-id="b7a21-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="b7a21-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="b7a21-109">array : 'T[]</span></span>

<span data-ttu-id="b7a21-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="b7a21-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="b7a21-111">Выходные данные: ' U []</span><span class="sxs-lookup"><span data-stu-id="b7a21-111">Output : 'U[]</span></span>

<span data-ttu-id="b7a21-112">Массив `'U[]` элементов, сопоставленных с `action` операцией.</span><span class="sxs-lookup"><span data-stu-id="b7a21-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b7a21-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="b7a21-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b7a21-114">Е</span><span class="sxs-lookup"><span data-stu-id="b7a21-114">'T</span></span>

<span data-ttu-id="b7a21-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="b7a21-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="b7a21-116">' U</span><span class="sxs-lookup"><span data-stu-id="b7a21-116">'U</span></span>

<span data-ttu-id="b7a21-117">Тип результата `action` операции.</span><span class="sxs-lookup"><span data-stu-id="b7a21-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7a21-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="b7a21-118">Remarks</span></span>

<span data-ttu-id="b7a21-119">Операция определяется для универсальных типов, т. е. Если у нас есть массив `'T[]` и операция, `action : 'T -> 'U` которые мы можем сопоставлять элементы массива и создаем новый массив типа `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="b7a21-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>