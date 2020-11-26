---
uid: Microsoft.Quantum.MachineLearning.ScheduleLength
title: Функция Счедулеленгс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ScheduleLength
qsharp.summary: Returns the number of elements in a given sampling schedule.
ms.openlocfilehash: 008bdcdc0a7c0ad2775dea65ebba46556092beed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211599"
---
# <a name="schedulelength-function"></a><span data-ttu-id="1cc8a-102">Функция Счедулеленгс</span><span class="sxs-lookup"><span data-stu-id="1cc8a-102">ScheduleLength function</span></span>

<span data-ttu-id="1cc8a-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="1cc8a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="1cc8a-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="1cc8a-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="1cc8a-105">Возвращает количество элементов в заданном расписании выборки.</span><span class="sxs-lookup"><span data-stu-id="1cc8a-105">Returns the number of elements in a given sampling schedule.</span></span>

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a><span data-ttu-id="1cc8a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1cc8a-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="1cc8a-107">Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="1cc8a-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="1cc8a-108">Расписание выборки, длина которого должна быть возвращена.</span><span class="sxs-lookup"><span data-stu-id="1cc8a-108">A sampling schedule whose length is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="1cc8a-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1cc8a-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1cc8a-110">Количество элементов в заданном расписании выборки.</span><span class="sxs-lookup"><span data-stu-id="1cc8a-110">The number of elements in the given sampling schedule.</span></span>