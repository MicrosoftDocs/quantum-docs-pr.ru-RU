---
uid: Microsoft.Quantum.MachineLearning.ScheduleLength
title: Функция Счедулеленгс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ScheduleLength
qsharp.summary: Returns the number of elements in a given sampling schedule.
ms.openlocfilehash: dd042b1282d2f5386ee0b67bf57ad4027eefd493
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854914"
---
# <a name="schedulelength-function"></a><span data-ttu-id="bf8f5-102">Функция Счедулеленгс</span><span class="sxs-lookup"><span data-stu-id="bf8f5-102">ScheduleLength function</span></span>

<span data-ttu-id="bf8f5-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="bf8f5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="bf8f5-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="bf8f5-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="bf8f5-105">Возвращает количество элементов в заданном расписании выборки.</span><span class="sxs-lookup"><span data-stu-id="bf8f5-105">Returns the number of elements in a given sampling schedule.</span></span>

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a><span data-ttu-id="bf8f5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bf8f5-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="bf8f5-107">Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="bf8f5-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="bf8f5-108">Расписание выборки, длина которого должна быть возвращена.</span><span class="sxs-lookup"><span data-stu-id="bf8f5-108">A sampling schedule whose length is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="bf8f5-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bf8f5-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bf8f5-110">Количество элементов в заданном расписании выборки.</span><span class="sxs-lookup"><span data-stu-id="bf8f5-110">The number of elements in the given sampling schedule.</span></span>