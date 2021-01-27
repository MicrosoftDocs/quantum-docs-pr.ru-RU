---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Функция Стандардрефлектионфасес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 703b50d0186cd0f4eddb9a29fa3cffb2b746c8d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843915"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="f26d0-102">Функция Стандардрефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="f26d0-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="f26d0-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="f26d0-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="f26d0-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f26d0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f26d0-105">Вычисление этапов частичного отражения для стандартного усиления амплитуды.</span><span class="sxs-lookup"><span data-stu-id="f26d0-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="f26d0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f26d0-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="f26d0-107">Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f26d0-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f26d0-108">Число итераций усиления амплитуды для создания фаз частичного отражения для.</span><span class="sxs-lookup"><span data-stu-id="f26d0-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="f26d0-109">Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="f26d0-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="f26d0-110">Операция, реализующая этапы, указанные как частичные отражения</span><span class="sxs-lookup"><span data-stu-id="f26d0-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="f26d0-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="f26d0-111">Remarks</span></span>

<span data-ttu-id="f26d0-112">Все фазы являются $ \пи $, за исключением первого отражения о начальном состоянии и последнего отражения состояния целевого объекта, которое равно $0 $.</span><span class="sxs-lookup"><span data-stu-id="f26d0-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>