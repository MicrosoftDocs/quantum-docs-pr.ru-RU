---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Функция Кумулативефолдед
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: ffb934d06f6be06cbc35a523c90d2c54e0a51353
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210035"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="d6a0b-102">Функция Кумулативефолдед</span><span class="sxs-lookup"><span data-stu-id="d6a0b-102">CumulativeFolded function</span></span>

<span data-ttu-id="d6a0b-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d6a0b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d6a0b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6a0b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6a0b-105">Объединяет сопоставленные и объединенные в одну функцию</span><span class="sxs-lookup"><span data-stu-id="d6a0b-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="d6a0b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d6a0b-106">Description</span></span>

<span data-ttu-id="d6a0b-107">Эта функция выполняет итерацию `fn` функции через массив, начиная с начального состояния `state` и возвращающего все промежуточные значения, не включая начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="d6a0b-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="d6a0b-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d6a0b-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="d6a0b-109">FN: (' State, t)-> ' State</span><span class="sxs-lookup"><span data-stu-id="d6a0b-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="d6a0b-110">Функция, которая должна быть свернута в массиве</span><span class="sxs-lookup"><span data-stu-id="d6a0b-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="d6a0b-111">состояние: "состояние</span><span class="sxs-lookup"><span data-stu-id="d6a0b-111">state : 'State</span></span>

<span data-ttu-id="d6a0b-112">Начальное состояние, которое должно быть сведено</span><span class="sxs-lookup"><span data-stu-id="d6a0b-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="d6a0b-113">массив: 'T []</span><span class="sxs-lookup"><span data-stu-id="d6a0b-113">array : 'T[]</span></span>

<span data-ttu-id="d6a0b-114">Массив значений для свертывания</span><span class="sxs-lookup"><span data-stu-id="d6a0b-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="d6a0b-115">Выходные данные: "State []</span><span class="sxs-lookup"><span data-stu-id="d6a0b-115">Output : 'State[]</span></span>

<span data-ttu-id="d6a0b-116">Все промежуточные состояния, включая конечное состояние, но не начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="d6a0b-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="d6a0b-117">Длина выходного массива равна длине `array` .</span><span class="sxs-lookup"><span data-stu-id="d6a0b-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d6a0b-118">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d6a0b-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="d6a0b-119">"State</span><span class="sxs-lookup"><span data-stu-id="d6a0b-119">'State</span></span>

<span data-ttu-id="d6a0b-120">Тип состояний, `fn` в которых работает функция, т. е. принимает в качестве первого входа и возвращает.</span><span class="sxs-lookup"><span data-stu-id="d6a0b-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="d6a0b-121">Е</span><span class="sxs-lookup"><span data-stu-id="d6a0b-121">'T</span></span>

<span data-ttu-id="d6a0b-122">Тип `array` элементов.</span><span class="sxs-lookup"><span data-stu-id="d6a0b-122">The type of `array` elements.</span></span>