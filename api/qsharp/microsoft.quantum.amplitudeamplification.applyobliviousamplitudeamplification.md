---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Операция Апплйобливиаусамплитудеамплификатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: a1bda344b1097c7ab3240bc6d9cd0d8df80b9662
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732008"
---
# <a name="applyobliviousamplitudeamplification-operation"></a><span data-ttu-id="c773b-102">Операция Апплйобливиаусамплитудеамплификатион</span><span class="sxs-lookup"><span data-stu-id="c773b-102">ApplyObliviousAmplitudeAmplification operation</span></span>

<span data-ttu-id="c773b-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="c773b-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="c773b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c773b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c773b-105">Усиление амплитуды очевидным путем указания частичных отражений.</span><span class="sxs-lookup"><span data-stu-id="c773b-105">Oblivious amplitude amplification by specifying partial reflections.</span></span>

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c773b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c773b-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="c773b-107">этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="c773b-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="c773b-108">Фазы частичной отражения</span><span class="sxs-lookup"><span data-stu-id="c773b-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="c773b-109">Стартстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="c773b-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="c773b-110">Оператор Reflection о начальном состоянии дополнительного регистра</span><span class="sxs-lookup"><span data-stu-id="c773b-110">Reflection operator about start state of auxiliary register</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="c773b-111">Таржетстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="c773b-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="c773b-112">Оператор отражения о целевом состоянии дополнительного регистра</span><span class="sxs-lookup"><span data-stu-id="c773b-112">Reflection operator about target state of auxiliary register</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="c773b-113">Сигналоракле: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="c773b-113">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="c773b-114">Единая база данных Oracle $O $ типа `ObliviousOracle` , которая взаимодействует с вспомогательными и системными регистрами.</span><span class="sxs-lookup"><span data-stu-id="c773b-114">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system registers.</span></span>


### <a name="auxiliaryregister--qubit"></a><span data-ttu-id="c773b-115">Ауксилиарирегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c773b-115">auxiliaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c773b-116">Дополнительный регистр</span><span class="sxs-lookup"><span data-stu-id="c773b-116">Auxiliary register</span></span>


### <a name="systemregister--qubit"></a><span data-ttu-id="c773b-117">Системрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c773b-117">systemRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c773b-118">Системный регистр</span><span class="sxs-lookup"><span data-stu-id="c773b-118">System register</span></span>



## <a name="output--unit"></a><span data-ttu-id="c773b-119">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c773b-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c773b-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="c773b-120">Remarks</span></span>

<span data-ttu-id="c773b-121">Учитывая определенное вспомогательное состояние запуска $ \кет{\текст{старт}} \_ $, определенное вспомогательное состояние $ \кет{\текст{таржет}} \_ a $ и любое состояние системы $ \кет{\пси} \_ s $, предположим, что \бегин{алигн} о\кет {\ Text {Start}} \_ а\кет {\ PSI} \_ s = \ламбда\кет{\текст{таржет}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\Text{Target} ^ \perp} \_ a\cdots \end{align} для $U $.</span><span class="sxs-lookup"><span data-stu-id="c773b-121">Given a particular auxiliary start state $\ket{\text{start}}\_a$, a particular auxiliary target state $\ket{\text{target}}\_a$, and any system state $\ket{\psi}\_s$, suppose that \begin{align} O\ket{\text{start}}\_a\ket{\psi}\_s= \lambda\ket{\text{target}}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{\text{target}^\perp}\_a\cdots \end{align} for some unitary $U$.</span></span>
<span data-ttu-id="c773b-122">По последовательности отражений состояний запуска и целевого объекта вспомогательной ККМ, которая загружается приложениями `signalOracle` и соседними, вероятность успешного применения U может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="c773b-122">By a sequence of reflections about the start and target states on the auxiliary register interleaved by applications of `signalOracle` and its adjoint, the success probability of applying U may be altered.</span></span>

<span data-ttu-id="c773b-123">В большинстве случаев `auxiliaryRegister` инициализируется в состоянии $ \кет{\текст{старт}} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="c773b-123">In most cases, `auxiliaryRegister` is initialized in the state $\ket{\text{start}}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="c773b-124">Ссылки</span><span class="sxs-lookup"><span data-stu-id="c773b-124">References</span></span>

<span data-ttu-id="c773b-125">См.</span><span class="sxs-lookup"><span data-stu-id="c773b-125">See</span></span>

- <span data-ttu-id="c773b-126">[ *Д.в. Берри, дочерние, r. Cleve, r. Котари, р.д. Сомма*](https://arxiv.org/abs/1312.1414) для стандартной версии.</span><span class="sxs-lookup"><span data-stu-id="c773b-126">[ *D.W. Berry, A.M. Childs, R. Cleve, R. Kothari, R.D. Somma* ](https://arxiv.org/abs/1312.1414) for the standard version.</span></span>
  <span data-ttu-id="c773b-127">См.</span><span class="sxs-lookup"><span data-stu-id="c773b-127">See</span></span>
- <span data-ttu-id="c773b-128">[ *Г.х. Low, и.л. Чжуанский*](https://arxiv.org/abs/1610.06546) для обобщения с частичными отражениями.</span><span class="sxs-lookup"><span data-stu-id="c773b-128">[ *G.H. Low, I.L. Chuang* ](https://arxiv.org/abs/1610.06546) for a generalization to partial reflections.</span></span>