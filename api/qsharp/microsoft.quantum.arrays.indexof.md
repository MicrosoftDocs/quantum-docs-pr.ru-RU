---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730217"
---
# <a name="indexof-function"></a><span data-ttu-id="5a615-102">IndexOf, функция</span><span class="sxs-lookup"><span data-stu-id="5a615-102">IndexOf function</span></span>

<span data-ttu-id="5a615-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5a615-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5a615-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5a615-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5a615-105">Возвращает первый индекс первого элемента в массиве, удовлетворяющего заданному предикату.</span><span class="sxs-lookup"><span data-stu-id="5a615-105">Returns the first index of the first element in an array that satisfies a given predicate.</span></span> <span data-ttu-id="5a615-106">Если такого элемента не существует, возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="5a615-106">If no such element exists, returns -1.</span></span>

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="5a615-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5a615-107">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="5a615-108">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5a615-108">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5a615-109">Функция предиката, действующая на элементы массива.</span><span class="sxs-lookup"><span data-stu-id="5a615-109">A predicate function acting on elements of the array.</span></span>


### <a name="arr--t"></a><span data-ttu-id="5a615-110">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="5a615-110">arr : 'T[]</span></span>

<span data-ttu-id="5a615-111">Массив для поиска с использованием заданного предиката.</span><span class="sxs-lookup"><span data-stu-id="5a615-111">An array to be searched using the given predicate.</span></span>



## <a name="output--int"></a><span data-ttu-id="5a615-112">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5a615-112">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5a615-113">Наименьший индекс, `idx` такой как `predicate(arr[idx])` true, или-1, если такого элемента не существует.</span><span class="sxs-lookup"><span data-stu-id="5a615-113">Either the smallest index `idx` such that `predicate(arr[idx])` is true, or -1 if no such element exists.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5a615-114">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="5a615-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5a615-115">Е</span><span class="sxs-lookup"><span data-stu-id="5a615-115">'T</span></span>

