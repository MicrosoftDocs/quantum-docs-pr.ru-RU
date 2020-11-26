---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Функция Фикседпоинтрефлектионфасес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191454"
---
# <a name="fixedpointreflectionphases-function"></a><span data-ttu-id="6b74e-102">Функция Фикседпоинтрефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="6b74e-102">FixedPointReflectionPhases function</span></span>

<span data-ttu-id="6b74e-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="6b74e-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="6b74e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b74e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b74e-105">Вычисление этапов частичного отражения для усиления амплитуды с фиксированной точкой.</span><span class="sxs-lookup"><span data-stu-id="6b74e-105">Computes partial reflection phases for fixed-point amplitude amplification.</span></span>

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="6b74e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6b74e-106">Input</span></span>

### <a name="nqueries--int"></a><span data-ttu-id="6b74e-107">Нкуериес: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b74e-107">nQueries : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6b74e-108">Число запросов к состоянию Oracle для подготовки.</span><span class="sxs-lookup"><span data-stu-id="6b74e-108">Number of queries to the state preparation oracle.</span></span> <span data-ttu-id="6b74e-109">Должно быть нечетным целым числом.</span><span class="sxs-lookup"><span data-stu-id="6b74e-109">Must be an odd integer.</span></span>


### <a name="successmin--double"></a><span data-ttu-id="6b74e-110">Сукцессмин: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6b74e-110">successMin : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6b74e-111">Минимальная вероятность успеха для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6b74e-111">Target minimum success probability.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="6b74e-112">Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="6b74e-112">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="6b74e-113">Массив фаз, который может использоваться в реализации алгоритма для усиления амплитуды с фиксированной точкой.</span><span class="sxs-lookup"><span data-stu-id="6b74e-113">Array of phases that can be used in fixed-point amplitude amplification quantum algorithm implementation.</span></span>

## <a name="references"></a><span data-ttu-id="6b74e-114">Ссылки</span><span class="sxs-lookup"><span data-stu-id="6b74e-114">References</span></span>

<span data-ttu-id="6b74e-115">Мы используем этапы в «усилении амплитуды с фиксированной точкой с оптимальным количеством запросов».</span><span class="sxs-lookup"><span data-stu-id="6b74e-115">We use the phases in "Fixed-Point Amplitude Amplification with an Optimal Number of Queries"</span></span>

- <span data-ttu-id="6b74e-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) См. также «методология составного тактового шлюза»</span><span class="sxs-lookup"><span data-stu-id="6b74e-116">[YoderLowChuang2014](https://arxiv.org/abs/1409.3305) See also "Methodology of composite quantum gates"</span></span>
- <span data-ttu-id="6b74e-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) для этапов в `RotationPhases` формате.</span><span class="sxs-lookup"><span data-stu-id="6b74e-117">[LowYoderChuang2016](https://arxiv.org/abs/1603.03996) for phases in the `RotationPhases` format.</span></span>