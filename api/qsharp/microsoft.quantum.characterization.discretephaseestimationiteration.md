---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Операция Дискретефасистиматионитератион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 03e2300dcc2d2cb42992e074833c8cd2530e898b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839976"
---
# <a name="discretephaseestimationiteration-operation"></a><span data-ttu-id="39b54-102">Операция Дискретефасистиматионитератион</span><span class="sxs-lookup"><span data-stu-id="39b54-102">DiscretePhaseEstimationIteration operation</span></span>

<span data-ttu-id="39b54-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="39b54-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="39b54-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39b54-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39b54-105">Выполняет одну итерацию итеративного (классического) алгоритма оценки фазы с помощью целочисленных степеней единой Oracle.</span><span class="sxs-lookup"><span data-stu-id="39b54-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.</span></span>

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="39b54-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="39b54-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="39b54-107">Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="39b54-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="39b54-108">Операция, выполняемая над целым числом и регистром, например $U ^ m $ применяется к заданному регистру, где $U $ — это единое целое, этап которого должен быть оценен, а $m $ — целочисленная мощность, заданная Oracle</span><span class="sxs-lookup"><span data-stu-id="39b54-108">Operation acting on an integer and a register, such that $U^m$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $m$ is the integer power given to the oracle</span></span>


### <a name="power--int"></a><span data-ttu-id="39b54-109">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39b54-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39b54-110">Количество раз, когда применяется заданная Единая база данных Oracle.</span><span class="sxs-lookup"><span data-stu-id="39b54-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="39b54-111">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="39b54-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="39b54-112">Угол, на который следует обратить фазу на элементе управления кубит до того, как он будет действовать в целевом состоянии.</span><span class="sxs-lookup"><span data-stu-id="39b54-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="39b54-113">Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="39b54-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="39b54-114">Регистрация состояния в зависимости от заданного единого объекта Oracle.</span><span class="sxs-lookup"><span data-stu-id="39b54-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="39b54-115">Контролкубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="39b54-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="39b54-116">Вспомогательная кубит, используемая для управления приложением данного Oracle.</span><span class="sxs-lookup"><span data-stu-id="39b54-116">An auxiliary qubit used to control the application of the given oracle.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39b54-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39b54-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

