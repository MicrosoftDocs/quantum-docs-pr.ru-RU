---
uid: Microsoft.Quantum.Arrays.Fold
title: Функция fold
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: a42f9a832c18bd612c1ae416187f3f2513eed54d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221170"
---
# <a name="fold-function"></a><span data-ttu-id="8c7ab-102">Функция fold</span><span class="sxs-lookup"><span data-stu-id="8c7ab-102">Fold function</span></span>

<span data-ttu-id="8c7ab-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8c7ab-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8c7ab-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8c7ab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8c7ab-105">Выполняет итерацию функции `f` через массив `array` , возвращая `f(f(f(initialState, array[0]), array[1]), ...)` .</span><span class="sxs-lookup"><span data-stu-id="8c7ab-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="8c7ab-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8c7ab-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="8c7ab-107">Папка: ("State, t"-> "State</span><span class="sxs-lookup"><span data-stu-id="8c7ab-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="8c7ab-108">Функция для свертывания массива.</span><span class="sxs-lookup"><span data-stu-id="8c7ab-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="8c7ab-109">состояние: "состояние</span><span class="sxs-lookup"><span data-stu-id="8c7ab-109">state : 'State</span></span>

<span data-ttu-id="8c7ab-110">Начальное состояние папки.</span><span class="sxs-lookup"><span data-stu-id="8c7ab-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="8c7ab-111">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="8c7ab-111">array : 'T[]</span></span>

<span data-ttu-id="8c7ab-112">Массив значений, по которым будет выполняться свертывание.</span><span class="sxs-lookup"><span data-stu-id="8c7ab-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="8c7ab-113">Выходные данные: "штат</span><span class="sxs-lookup"><span data-stu-id="8c7ab-113">Output : 'State</span></span>

<span data-ttu-id="8c7ab-114">Конечное состояние, возвращенное папкой после прохода по всем элементам `array` .</span><span class="sxs-lookup"><span data-stu-id="8c7ab-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8c7ab-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8c7ab-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="8c7ab-116">"State</span><span class="sxs-lookup"><span data-stu-id="8c7ab-116">'State</span></span>

<span data-ttu-id="8c7ab-117">Тип состояний `folder` , в которых функция работает, т. е. принимает в качестве первого аргумента и возвращает.</span><span class="sxs-lookup"><span data-stu-id="8c7ab-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="8c7ab-118">Е</span><span class="sxs-lookup"><span data-stu-id="8c7ab-118">'T</span></span>

<span data-ttu-id="8c7ab-119">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="8c7ab-119">The type of `array` elements.</span></span>