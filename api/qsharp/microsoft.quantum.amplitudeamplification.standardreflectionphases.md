---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Функция Стандардрефлектионфасес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: c189b34b641989ab458986fb3f2872759b949be5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731921"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="0f37f-102">Функция Стандардрефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="0f37f-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="0f37f-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="0f37f-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="0f37f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0f37f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0f37f-105">Вычисление этапов частичного отражения для стандартного усиления амплитуды.</span><span class="sxs-lookup"><span data-stu-id="0f37f-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="0f37f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0f37f-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="0f37f-107">Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0f37f-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0f37f-108">Число итераций усиления амплитуды для создания фаз частичного отражения для.</span><span class="sxs-lookup"><span data-stu-id="0f37f-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="0f37f-109">Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="0f37f-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="0f37f-110">Операция, реализующая этапы, указанные как частичные отражения</span><span class="sxs-lookup"><span data-stu-id="0f37f-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="0f37f-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="0f37f-111">Remarks</span></span>

<span data-ttu-id="0f37f-112">Все фазы являются $ \пи $, за исключением первого отражения о начальном состоянии и последнего отражения состояния целевого объекта, которое равно $0 $.</span><span class="sxs-lookup"><span data-stu-id="0f37f-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>