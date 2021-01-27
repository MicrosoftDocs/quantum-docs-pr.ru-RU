---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Функция выборки
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 5dd599246847718f4f0411715585cb416595db9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854947"
---
# <a name="sampled-function"></a><span data-ttu-id="3dd5b-102">Функция выборки</span><span class="sxs-lookup"><span data-stu-id="3dd5b-102">Sampled function</span></span>

<span data-ttu-id="3dd5b-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3dd5b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="3dd5b-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3dd5b-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="3dd5b-105">Производит выборку заданного массива с использованием заданного расписания.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="3dd5b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3dd5b-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="3dd5b-107">Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="3dd5b-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="3dd5b-108">Расписание, используемое в значениях выборки.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="3dd5b-109">значения: 'T []</span><span class="sxs-lookup"><span data-stu-id="3dd5b-109">values : 'T[]</span></span>

<span data-ttu-id="3dd5b-110">Массив значений для выборки.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="3dd5b-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="3dd5b-111">Output : 'T[]</span></span>

<span data-ttu-id="3dd5b-112">Массив элементов из значений, следующих за заданным расписанием.</span><span class="sxs-lookup"><span data-stu-id="3dd5b-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3dd5b-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="3dd5b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3dd5b-114">Е</span><span class="sxs-lookup"><span data-stu-id="3dd5b-114">'T</span></span>

