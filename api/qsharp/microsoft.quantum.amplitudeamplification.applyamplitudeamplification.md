---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: Операция Апплямплитудеамплификатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: be884eab70c7f72f994baf6bd7caf05769e0d5f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732033"
---
# <a name="applyamplitudeamplification-operation"></a><span data-ttu-id="6be9c-102">Операция Апплямплитудеамплификатион</span><span class="sxs-lookup"><span data-stu-id="6be9c-102">ApplyAmplitudeAmplification operation</span></span>

<span data-ttu-id="6be9c-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="6be9c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="6be9c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6be9c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6be9c-105">Применяет усиление амплитуды к заданному регистру, используя заданный набор фаз и Oracle, чтобы отражать начальное и конечное состояния.</span><span class="sxs-lookup"><span data-stu-id="6be9c-105">Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.</span></span>

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="6be9c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6be9c-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="6be9c-107">этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="6be9c-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="6be9c-108">Набор этапов, описывающих частичные отражения на каждом шаге алгоритма усиления амплитуды.</span><span class="sxs-lookup"><span data-stu-id="6be9c-108">A set of phases describing the partial reflections at each step of the amplitude amplification algorithm.</span></span> <span data-ttu-id="6be9c-109">Пример см. в разделе @"microsoft.quantum.amplitudeamplification.standardreflectionphases".</span><span class="sxs-lookup"><span data-stu-id="6be9c-109">See @"microsoft.quantum.amplitudeamplification.standardreflectionphases" for an example.</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="6be9c-110">Стартстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="6be9c-110">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="6be9c-111">Oracle, отражающий начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="6be9c-111">An oracle that reflects about the initial state.</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="6be9c-112">Таржетстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="6be9c-112">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="6be9c-113">Значение Oracle, отражающее требуемое конечное состояние.</span><span class="sxs-lookup"><span data-stu-id="6be9c-113">An oracle that reflects about the desired final state.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="6be9c-114">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6be9c-114">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6be9c-115">Регистр для выполнения усиления амплитуды.</span><span class="sxs-lookup"><span data-stu-id="6be9c-115">A register to perform amplitude amplification on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6be9c-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6be9c-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

