---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Функция Стандардрефлектионфасес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 316c8f22a16859ebb439824eda9a5aa02c750b5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191131"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="3f85e-102">Функция Стандардрефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="3f85e-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="3f85e-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="3f85e-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="3f85e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f85e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f85e-105">Вычисление этапов частичного отражения для стандартного усиления амплитуды.</span><span class="sxs-lookup"><span data-stu-id="3f85e-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="3f85e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3f85e-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="3f85e-107">Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3f85e-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3f85e-108">Число итераций усиления амплитуды для создания фаз частичного отражения для.</span><span class="sxs-lookup"><span data-stu-id="3f85e-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="3f85e-109">Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="3f85e-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="3f85e-110">Операция, реализующая этапы, указанные как частичные отражения</span><span class="sxs-lookup"><span data-stu-id="3f85e-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="3f85e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f85e-111">Remarks</span></span>

<span data-ttu-id="3f85e-112">Все фазы являются $ \пи $, за исключением первого отражения о начальном состоянии и последнего отражения состояния целевого объекта, которое равно $0 $.</span><span class="sxs-lookup"><span data-stu-id="3f85e-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>