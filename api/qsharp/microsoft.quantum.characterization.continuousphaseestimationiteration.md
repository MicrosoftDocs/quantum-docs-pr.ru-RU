---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Операция Континуаусфасистиматионитератион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: a3914a4b19e3b898b6de8808699da09d386f487a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715076"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="2e960-102">Операция Континуаусфасистиматионитератион</span><span class="sxs-lookup"><span data-stu-id="2e960-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="2e960-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="2e960-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="2e960-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2e960-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2e960-105">Выполняет одну итерацию итеративного (классического) алгоритма оценки фазы с использованием произвольных реальных степеней единой системы Oracle.</span><span class="sxs-lookup"><span data-stu-id="2e960-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="2e960-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2e960-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="2e960-107">Oracle: [континуаусоракле](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="2e960-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="2e960-108">Операция, работающая с двойным $t $ и регистром, таким, что $U ^ t $ применяется к заданному регистру, где $U $ является единым этапом, который должен быть оценен, а $t $ — целочисленной мощностью, заданной для Oracle</span><span class="sxs-lookup"><span data-stu-id="2e960-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="2e960-109">время: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2e960-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2e960-110">Количество раз, когда применяется заданная Единая база данных Oracle.</span><span class="sxs-lookup"><span data-stu-id="2e960-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="2e960-111">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2e960-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2e960-112">Угол, на который следует обратить фазу на элементе управления кубит до того, как он будет действовать в целевом состоянии.</span><span class="sxs-lookup"><span data-stu-id="2e960-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="2e960-113">Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2e960-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2e960-114">Регистрация состояния в зависимости от заданного единого объекта Oracle.</span><span class="sxs-lookup"><span data-stu-id="2e960-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="2e960-115">Контролкубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2e960-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="2e960-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2e960-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

