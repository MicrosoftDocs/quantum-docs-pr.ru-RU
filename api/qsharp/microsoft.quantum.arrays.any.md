---
uid: Microsoft.Quantum.Arrays.Any
title: Любая функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: dd5639f1b0a76cb356c89aca0c0e02d375f30d12
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730417"
---
# <a name="any-function"></a><span data-ttu-id="72490-102">Любая функция</span><span class="sxs-lookup"><span data-stu-id="72490-102">Any function</span></span>

<span data-ttu-id="72490-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="72490-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="72490-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="72490-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="72490-105">При наличии массива и предиката, определенного для элементов массива, проверяет, удовлетворяет ли предикату хотя бы один элемент массива.</span><span class="sxs-lookup"><span data-stu-id="72490-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="72490-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="72490-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="72490-107">предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="72490-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="72490-108">Функция из `'T` в `Bool` , используемая для проверки элементов.</span><span class="sxs-lookup"><span data-stu-id="72490-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="72490-109">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="72490-109">array : 'T[]</span></span>

<span data-ttu-id="72490-110">Массив элементов `'T` .</span><span class="sxs-lookup"><span data-stu-id="72490-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="72490-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="72490-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="72490-112">`Bool`Значение функции или предиката, применяемого ко всем элементам.</span><span class="sxs-lookup"><span data-stu-id="72490-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="72490-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="72490-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="72490-114">Е</span><span class="sxs-lookup"><span data-stu-id="72490-114">'T</span></span>

<span data-ttu-id="72490-115">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="72490-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="72490-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="72490-116">Remarks</span></span>

<span data-ttu-id="72490-117">Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `predicate: 'T -> Bool` мы можем получить `Bool` значение, которое указывает, удовлетворяет ли какой-либо элемент `predicate` .</span><span class="sxs-lookup"><span data-stu-id="72490-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>