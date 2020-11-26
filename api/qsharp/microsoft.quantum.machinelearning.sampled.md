---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Функция выборки
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: ddff72bbed6f20e8e0ceb3bfe3fc50a3da0bd2a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211633"
---
# <a name="sampled-function"></a><span data-ttu-id="fb194-102">Функция выборки</span><span class="sxs-lookup"><span data-stu-id="fb194-102">Sampled function</span></span>

<span data-ttu-id="fb194-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fb194-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="fb194-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="fb194-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="fb194-105">Производит выборку заданного массива с использованием заданного расписания.</span><span class="sxs-lookup"><span data-stu-id="fb194-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="fb194-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fb194-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="fb194-107">Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="fb194-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="fb194-108">Расписание, используемое в значениях выборки.</span><span class="sxs-lookup"><span data-stu-id="fb194-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="fb194-109">значения: 'T []</span><span class="sxs-lookup"><span data-stu-id="fb194-109">values : 'T[]</span></span>

<span data-ttu-id="fb194-110">Массив значений для выборки.</span><span class="sxs-lookup"><span data-stu-id="fb194-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="fb194-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="fb194-111">Output : 'T[]</span></span>

<span data-ttu-id="fb194-112">Массив элементов из значений, следующих за заданным расписанием.</span><span class="sxs-lookup"><span data-stu-id="fb194-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fb194-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="fb194-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fb194-114">Е</span><span class="sxs-lookup"><span data-stu-id="fb194-114">'T</span></span>

