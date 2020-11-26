---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: Функция Амплитудеамплификатионфромстатепрепаратион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 30e1cf6e353b8a4491e13a9e2f588ec9cc103cb4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191607"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="99c60-102">Функция Амплитудеамплификатионфромстатепрепаратион</span><span class="sxs-lookup"><span data-stu-id="99c60-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="99c60-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="99c60-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="99c60-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="99c60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="99c60-105">Усиление амплитуды по Oracle для частичных отражений.</span><span class="sxs-lookup"><span data-stu-id="99c60-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="99c60-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="99c60-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="99c60-107">этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="99c60-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="99c60-108">Фазы частичной отражения</span><span class="sxs-lookup"><span data-stu-id="99c60-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="99c60-109">Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="99c60-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="99c60-110">Единая база данных Oracle $A $, подготавливающая начальное состояние</span><span class="sxs-lookup"><span data-stu-id="99c60-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="99c60-111">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="99c60-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="99c60-112">Индекс для отметки кубит</span><span class="sxs-lookup"><span data-stu-id="99c60-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="99c60-113">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL</span><span class="sxs-lookup"><span data-stu-id="99c60-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="99c60-114">Операция, которая реализует усиление амплитуды с помощью Oracle, которые реализуются частичными отражениями.</span><span class="sxs-lookup"><span data-stu-id="99c60-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="99c60-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99c60-115">Remarks</span></span>

<span data-ttu-id="99c60-116">Это накладывает более четкие условия на формат начального и целевого состояний, чем в `AmpAmpByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="99c60-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="99c60-117">Предполагается, что целевое состояние помечено как $ \кет {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="99c60-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="99c60-118">Предполагается, что \бегин{алигн} А\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {Target}} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \енд{алигн} в большинстве случаев `flagQubit` и `auxiliaryRegister` инициализируются в состоянии $ \кет {0} \_ {f} \кет {0} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="99c60-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>