---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Функция Кумулативефолдед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: a09c2779c8f06d8f6b7b0902366f3cefbbca4525
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730368"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="7fdcf-102">Функция Кумулативефолдед</span><span class="sxs-lookup"><span data-stu-id="7fdcf-102">CumulativeFolded function</span></span>

<span data-ttu-id="7fdcf-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7fdcf-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7fdcf-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7fdcf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7fdcf-105">Объединяет сопоставленные и объединенные в одну функцию</span><span class="sxs-lookup"><span data-stu-id="7fdcf-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="7fdcf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7fdcf-106">Description</span></span>

<span data-ttu-id="7fdcf-107">Эта функция выполняет итерацию `fn` функции через массив, начиная с начального состояния `state` и возвращающего все промежуточные значения, не включая начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="7fdcf-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="7fdcf-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7fdcf-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="7fdcf-109">FN: (' State, t)-> ' State</span><span class="sxs-lookup"><span data-stu-id="7fdcf-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="7fdcf-110">Функция, которая должна быть свернута в массиве</span><span class="sxs-lookup"><span data-stu-id="7fdcf-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="7fdcf-111">состояние: "состояние</span><span class="sxs-lookup"><span data-stu-id="7fdcf-111">state : 'State</span></span>

<span data-ttu-id="7fdcf-112">Начальное состояние, которое должно быть сведено</span><span class="sxs-lookup"><span data-stu-id="7fdcf-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="7fdcf-113">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="7fdcf-113">array : 'T[]</span></span>

<span data-ttu-id="7fdcf-114">Массив значений для свертывания</span><span class="sxs-lookup"><span data-stu-id="7fdcf-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="7fdcf-115">Выходные данные: "State []</span><span class="sxs-lookup"><span data-stu-id="7fdcf-115">Output : 'State[]</span></span>

<span data-ttu-id="7fdcf-116">Все промежуточные состояния, включая конечное состояние, но не начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="7fdcf-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="7fdcf-117">Длина выходного массива равна длине `array` .</span><span class="sxs-lookup"><span data-stu-id="7fdcf-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7fdcf-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="7fdcf-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="7fdcf-119">"State</span><span class="sxs-lookup"><span data-stu-id="7fdcf-119">'State</span></span>

<span data-ttu-id="7fdcf-120">Тип состояний, `fn` в которых работает функция, т. е. принимает в качестве первого входа и возвращает.</span><span class="sxs-lookup"><span data-stu-id="7fdcf-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="7fdcf-121">Е</span><span class="sxs-lookup"><span data-stu-id="7fdcf-121">'T</span></span>

<span data-ttu-id="7fdcf-122">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="7fdcf-122">The type of `array` elements.</span></span>