---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Функция выборки
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732320"
---
# <a name="sampled-function"></a><span data-ttu-id="d0114-102">Функция выборки</span><span class="sxs-lookup"><span data-stu-id="d0114-102">Sampled function</span></span>

<span data-ttu-id="d0114-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d0114-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d0114-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0114-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0114-105">Производит выборку заданного массива с использованием заданного расписания.</span><span class="sxs-lookup"><span data-stu-id="d0114-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d0114-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d0114-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="d0114-107">Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="d0114-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="d0114-108">Расписание, используемое в значениях выборки.</span><span class="sxs-lookup"><span data-stu-id="d0114-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="d0114-109">значения: 'T []</span><span class="sxs-lookup"><span data-stu-id="d0114-109">values : 'T[]</span></span>

<span data-ttu-id="d0114-110">Массив значений для выборки.</span><span class="sxs-lookup"><span data-stu-id="d0114-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="d0114-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="d0114-111">Output : 'T[]</span></span>

<span data-ttu-id="d0114-112">Массив элементов из значений, следующих за заданным расписанием.</span><span class="sxs-lookup"><span data-stu-id="d0114-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d0114-113">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="d0114-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d0114-114">Е</span><span class="sxs-lookup"><span data-stu-id="d0114-114">'T</span></span>

