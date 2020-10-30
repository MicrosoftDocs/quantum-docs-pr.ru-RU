---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: Функция Обливиаусамплитудеамплификатионфромстатепрепаратион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 9975d26af8f9beb2b91e409ad78159d6f04936e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731977"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="fab4d-102">Функция Обливиаусамплитудеамплификатионфромстатепрепаратион</span><span class="sxs-lookup"><span data-stu-id="fab4d-102">ObliviousAmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="fab4d-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="fab4d-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="fab4d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fab4d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fab4d-105">Усиление амплитуды очевидным по Oracle для частичных отражений.</span><span class="sxs-lookup"><span data-stu-id="fab4d-105">Oblivious amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="fab4d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fab4d-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="fab4d-107">этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="fab4d-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="fab4d-108">Фазы частичной отражения</span><span class="sxs-lookup"><span data-stu-id="fab4d-108">Phases of partial reflections</span></span>


### <a name="startstateoracle--deterministicstateoracle"></a><span data-ttu-id="fab4d-109">Стартстатеоракле: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="fab4d-109">startStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="fab4d-110">Единая база данных Oracle $A $, подготавливающая дополнительное состояние запуска</span><span class="sxs-lookup"><span data-stu-id="fab4d-110">Unitary oracle $A$ that prepares auxiliary start state</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="fab4d-111">Сигналоракле: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="fab4d-111">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="fab4d-112">Единая база данных Oracle $O $ типа `ObliviousOracle` , которая взаимодействует с дополнительным и системным регистром</span><span class="sxs-lookup"><span data-stu-id="fab4d-112">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system register</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="fab4d-113">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fab4d-113">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fab4d-114">Регистр индекса для однокубитного флага</span><span class="sxs-lookup"><span data-stu-id="fab4d-114">Index to single-qubit flag register</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="fab4d-115">Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [>ная](xref:microsoft.quantum.lang-ref.unit) расгода и список доверия</span><span class="sxs-lookup"><span data-stu-id="fab4d-115">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="fab4d-116">Операция, реализующая усиление амплитуды очевидным на основе частичных отражений.</span><span class="sxs-lookup"><span data-stu-id="fab4d-116">An operation that implements oblivious amplitude amplification based on partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="fab4d-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="fab4d-117">Remarks</span></span>

<span data-ttu-id="fab4d-118">Это накладывает более четкие условия на формат начального и целевого состояний, чем в `AmpAmpObliviousByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="fab4d-118">This imposes stricter conditions on form of the auxiliary start and target states than in `AmpAmpObliviousByReflectionPhases`.</span></span>
<span data-ttu-id="fab4d-119">Предполагается, что $A \кет {0} \_ ф\кет {0} \_ A = \кет{\текст{старт}} \_ {FA} $ подготавливает вспомогательное состояние запуска $ \кет{\текст{старт}} \_ {FA} $ от вычислительной базы $ \кет {0} \_ ф\кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="fab4d-119">It is assumed that $A\ket{0}\_f\ket{0}\_a= \ket{\text{start}}\_{fa}$ prepares the auxiliary start state $\ket{\text{start}}\_{fa}$ from the computational basis $\ket{0}\_f\ket{0}$.</span></span>
<span data-ttu-id="fab4d-120">Предполагается, что целевое состояние помечено как $ \кет {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="fab4d-120">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="fab4d-121">Предполагается, что \бегин{алигн} О\кет {\ Text {Start}} \_ {FA} \кет{\пси} \_ s = \ламбда\кет {1} \_ ф\кет {\ Text {ничего}} \_ а\кет {\ Text {Target}} \_ s U \кет{\пси} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, \end{align} для некоторых $U $.</span><span class="sxs-lookup"><span data-stu-id="fab4d-121">It is assumed that \begin{align} O\ket{\text{start}}\_{fa}\ket{\psi}\_s= \lambda\ket{1}\_f\ket{\text{anything}}\_a\ket{\text{target}}\_s U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} for some unitary $U$.</span></span>