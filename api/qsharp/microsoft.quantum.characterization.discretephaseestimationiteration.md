---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Операция Дискретефасистиматионитератион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 167b53d7108c64d11a4f258d17e90ba78d7dd8d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715075"
---
# <a name="discretephaseestimationiteration-operation"></a><span data-ttu-id="a28a3-102">Операция Дискретефасистиматионитератион</span><span class="sxs-lookup"><span data-stu-id="a28a3-102">DiscretePhaseEstimationIteration operation</span></span>

<span data-ttu-id="a28a3-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="a28a3-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="a28a3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a28a3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a28a3-105">Выполняет одну итерацию итеративного (классического) алгоритма оценки фазы с помощью целочисленных степеней единой Oracle.</span><span class="sxs-lookup"><span data-stu-id="a28a3-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.</span></span>

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="a28a3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a28a3-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="a28a3-107">Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="a28a3-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="a28a3-108">Операция, выполняемая над целым числом и регистром, например $U ^ m $ применяется к заданному регистру, где $U $ — это единое целое, этап которого должен быть оценен, а $m $ — целочисленная мощность, заданная Oracle</span><span class="sxs-lookup"><span data-stu-id="a28a3-108">Operation acting on an integer and a register, such that $U^m$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $m$ is the integer power given to the oracle</span></span>


### <a name="power--int"></a><span data-ttu-id="a28a3-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a28a3-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a28a3-110">Количество раз, когда применяется заданная Единая база данных Oracle.</span><span class="sxs-lookup"><span data-stu-id="a28a3-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="a28a3-111">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a28a3-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a28a3-112">Угол, на который следует обратить фазу на элементе управления кубит до того, как он будет действовать в целевом состоянии.</span><span class="sxs-lookup"><span data-stu-id="a28a3-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="a28a3-113">Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a28a3-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a28a3-114">Регистрация состояния в зависимости от заданного единого объекта Oracle.</span><span class="sxs-lookup"><span data-stu-id="a28a3-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="a28a3-115">Контролкубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a28a3-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a28a3-116">Вспомогательная кубит, используемая для управления приложением данного Oracle.</span><span class="sxs-lookup"><span data-stu-id="a28a3-116">An auxiliary qubit used to control the application of the given oracle.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a28a3-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a28a3-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

