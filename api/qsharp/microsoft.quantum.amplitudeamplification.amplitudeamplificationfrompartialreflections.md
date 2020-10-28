---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Функция Амплитудеамплификатионфромпартиалрефлектионс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: fc7c2c0d05ea626f7f7e5d8ebf3ce5ecea61390b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732048"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="912a0-102">Функция Амплитудеамплификатионфромпартиалрефлектионс</span><span class="sxs-lookup"><span data-stu-id="912a0-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="912a0-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="912a0-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="912a0-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="912a0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="912a0-105">Усиление амплитуды путем частичной отражения.</span><span class="sxs-lookup"><span data-stu-id="912a0-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="912a0-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="912a0-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="912a0-107">этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="912a0-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="912a0-108">Фазы частичной отражения</span><span class="sxs-lookup"><span data-stu-id="912a0-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="912a0-109">Стартстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="912a0-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="912a0-110">Оператор отражения о начальном состоянии</span><span class="sxs-lookup"><span data-stu-id="912a0-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="912a0-111">Таржетстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="912a0-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="912a0-112">Оператор отражения о целевом состоянии</span><span class="sxs-lookup"><span data-stu-id="912a0-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="912a0-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="912a0-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="912a0-114">Операция, реализующая усиление амплитуды путем частичной отражения.</span><span class="sxs-lookup"><span data-stu-id="912a0-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="912a0-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="912a0-115">Remarks</span></span>

<span data-ttu-id="912a0-116">Усиление амплитуды — это особый случай усиления амплитуды очевидным, когда нет Кубитс системы, а очевидным Oracle имеет значение Identity.</span><span class="sxs-lookup"><span data-stu-id="912a0-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="912a0-117">В большинстве случаев `startQubits` инициализируется в состоянии $ \кет{\текст{старт}} \_ $1, которое является $-$1 еиженстате `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="912a0-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>