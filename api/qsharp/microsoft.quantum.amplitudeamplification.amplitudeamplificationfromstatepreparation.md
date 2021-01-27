---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: Функция Амплитудеамплификатионфромстатепрепаратион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: e64ad5ad4e975483f20f92c0b070dd6788ef296b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847456"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="9bc91-102">Функция Амплитудеамплификатионфромстатепрепаратион</span><span class="sxs-lookup"><span data-stu-id="9bc91-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="9bc91-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="9bc91-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="9bc91-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9bc91-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9bc91-105">Усиление амплитуды по Oracle для частичных отражений.</span><span class="sxs-lookup"><span data-stu-id="9bc91-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="9bc91-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9bc91-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="9bc91-107">этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="9bc91-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="9bc91-108">Фазы частичной отражения</span><span class="sxs-lookup"><span data-stu-id="9bc91-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="9bc91-109">Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="9bc91-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="9bc91-110">Единая база данных Oracle $A $, подготавливающая начальное состояние</span><span class="sxs-lookup"><span data-stu-id="9bc91-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="9bc91-111">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9bc91-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9bc91-112">Индекс для отметки кубит</span><span class="sxs-lookup"><span data-stu-id="9bc91-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="9bc91-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL</span><span class="sxs-lookup"><span data-stu-id="9bc91-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="9bc91-114">Операция, которая реализует усиление амплитуды с помощью Oracle, которые реализуются частичными отражениями.</span><span class="sxs-lookup"><span data-stu-id="9bc91-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bc91-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="9bc91-115">Remarks</span></span>

<span data-ttu-id="9bc91-116">Это накладывает более четкие условия на формат начального и целевого состояний, чем в `AmpAmpByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="9bc91-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="9bc91-117">Предполагается, что целевое состояние помечено как $ \кет {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="9bc91-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="9bc91-118">Предполагается, что \бегин{алигн} А\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {Target}} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \енд{алигн} в большинстве случаев `flagQubit` и `auxiliaryRegister` инициализируются в состоянии $ \кет {0} \_ {f} \кет {0} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="9bc91-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>