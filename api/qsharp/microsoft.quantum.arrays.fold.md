---
uid: Microsoft.Quantum.Arrays.Fold
title: Функция fold
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: 47c23dd657391d80fe473d98f2036d8ddf1dbb0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730241"
---
# <a name="fold-function"></a><span data-ttu-id="564f2-102">Функция fold</span><span class="sxs-lookup"><span data-stu-id="564f2-102">Fold function</span></span>

<span data-ttu-id="564f2-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="564f2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="564f2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="564f2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="564f2-105">Выполняет итерацию функции `f` через массив `array` , возвращая `f(f(f(initialState, array[0]), array[1]), ...)` .</span><span class="sxs-lookup"><span data-stu-id="564f2-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="564f2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="564f2-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="564f2-107">Папка: ("State, t"-> "State</span><span class="sxs-lookup"><span data-stu-id="564f2-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="564f2-108">Функция для свертывания массива.</span><span class="sxs-lookup"><span data-stu-id="564f2-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="564f2-109">состояние: "состояние</span><span class="sxs-lookup"><span data-stu-id="564f2-109">state : 'State</span></span>

<span data-ttu-id="564f2-110">Начальное состояние папки.</span><span class="sxs-lookup"><span data-stu-id="564f2-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="564f2-111">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="564f2-111">array : 'T[]</span></span>

<span data-ttu-id="564f2-112">Массив значений, по которым будет выполняться свертывание.</span><span class="sxs-lookup"><span data-stu-id="564f2-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="564f2-113">Выходные данные: "штат</span><span class="sxs-lookup"><span data-stu-id="564f2-113">Output : 'State</span></span>

<span data-ttu-id="564f2-114">Конечное состояние, возвращенное папкой после прохода по всем элементам `array` .</span><span class="sxs-lookup"><span data-stu-id="564f2-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="564f2-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="564f2-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="564f2-116">"State</span><span class="sxs-lookup"><span data-stu-id="564f2-116">'State</span></span>

<span data-ttu-id="564f2-117">Тип состояний `folder` , в которых функция работает, т. е. принимает в качестве первого аргумента и возвращает.</span><span class="sxs-lookup"><span data-stu-id="564f2-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="564f2-118">Е</span><span class="sxs-lookup"><span data-stu-id="564f2-118">'T</span></span>

<span data-ttu-id="564f2-119">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="564f2-119">The type of `array` elements.</span></span>