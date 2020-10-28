---
uid: Microsoft.Quantum.Simulation.EstimateEnergyWithAdiabaticEvolution
title: Операция Естиматинергивисадиабатицеволутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergyWithAdiabaticEvolution
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 3fdbdd83b784cdc560e3160151fdf4ba4e7115e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732112"
---
# <a name="estimateenergywithadiabaticevolution-operation"></a><span data-ttu-id="97ea2-102">Операция Естиматинергивисадиабатицеволутион</span><span class="sxs-lookup"><span data-stu-id="97ea2-102">EstimateEnergyWithAdiabaticEvolution operation</span></span>

<span data-ttu-id="97ea2-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="97ea2-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="97ea2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="97ea2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="97ea2-105">Выполняет подготовку состояния, применяя к `statePrepUnitary` автоматически выделенному входному состоянию, за которым следует подготовка состояния адиабатик с помощью `adiabaticUnitary` , и, наконец, Оценка этапа по отношению к `qpeUnitary` результирующему состоянию с помощью `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="97ea2-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergyWithAdiabaticEvolution (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="97ea2-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="97ea2-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="97ea2-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="97ea2-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="97ea2-108">Число Кубитс, используемых для моделирования.</span><span class="sxs-lookup"><span data-stu-id="97ea2-108">Number of qubits used for the simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="97ea2-109">Статепрепунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="97ea2-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="97ea2-110">Oracle, представляющий подготовку состояния для первоначального динамического генератора.</span><span class="sxs-lookup"><span data-stu-id="97ea2-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="adiabaticunitary--qubit--unit"></a><span data-ttu-id="97ea2-111">Адиабатикунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="97ea2-111">adiabaticUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="97ea2-112">Oracle, представляющий алгоритм эволюции адиабатик, который используется для реализации очистки до окончательного состояния алгоритма.</span><span class="sxs-lookup"><span data-stu-id="97ea2-112">An oracle representing the adiabatic evolution algorithm to be used to implement the sweeps to the final state of the algorithm.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="97ea2-113">Кпеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="97ea2-113">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="97ea2-114">Oracle, представляющий отдельный оператор $U $ представляющие развитие времени $ \делта t $ в динамическом генераторе с состоянием заземления $ \кет{\фи} $ и состоянием заземления $E = \фи \\ , \делта t $.</span><span class="sxs-lookup"><span data-stu-id="97ea2-114">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="97ea2-115">Фасисталгорисм: ([дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="97ea2-115">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="97ea2-116">Операция, выполняющая оценку этапа для данной отдельной операции.</span><span class="sxs-lookup"><span data-stu-id="97ea2-116">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="97ea2-117">Дополнительные сведения см. в статье [Оценка этапа итерации](/quantum/libraries/characterization#iterative-phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="97ea2-117">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="97ea2-118">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="97ea2-118">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="97ea2-119">Оценочное значение $ \хат{\фи} $ от земли $ \фи $ генератора, представленного $U $.</span><span class="sxs-lookup"><span data-stu-id="97ea2-119">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the generator represented by $U$.</span></span>