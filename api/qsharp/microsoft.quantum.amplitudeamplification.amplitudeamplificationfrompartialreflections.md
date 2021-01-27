---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Функция Амплитудеамплификатионфромпартиалрефлектионс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: e4030aabcab55db35bcb8199e37bee837ead6ad0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845898"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="142f6-102">Функция Амплитудеамплификатионфромпартиалрефлектионс</span><span class="sxs-lookup"><span data-stu-id="142f6-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="142f6-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="142f6-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="142f6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="142f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="142f6-105">Усиление амплитуды путем частичной отражения.</span><span class="sxs-lookup"><span data-stu-id="142f6-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="142f6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="142f6-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="142f6-107">этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="142f6-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="142f6-108">Фазы частичной отражения</span><span class="sxs-lookup"><span data-stu-id="142f6-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="142f6-109">Стартстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="142f6-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="142f6-110">Оператор отражения о начальном состоянии</span><span class="sxs-lookup"><span data-stu-id="142f6-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="142f6-111">Таржетстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="142f6-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="142f6-112">Оператор отражения о целевом состоянии</span><span class="sxs-lookup"><span data-stu-id="142f6-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="142f6-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL</span><span class="sxs-lookup"><span data-stu-id="142f6-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="142f6-114">Операция, реализующая усиление амплитуды путем частичной отражения.</span><span class="sxs-lookup"><span data-stu-id="142f6-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="142f6-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="142f6-115">Remarks</span></span>

<span data-ttu-id="142f6-116">Усиление амплитуды — это особый случай усиления амплитуды очевидным, когда нет Кубитс системы, а очевидным Oracle имеет значение Identity.</span><span class="sxs-lookup"><span data-stu-id="142f6-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="142f6-117">В большинстве случаев `startQubits` инициализируется в состоянии $ \кет{\текст{старт}} \_ $1, которое является $-$1 еиженстате `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="142f6-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>