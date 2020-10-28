---
uid: Microsoft.Quantum.Simulation.AdiabaticStateEnergyUnitary
title: Операция Адиабатикстатинергюнитари
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: AdiabaticStateEnergyUnitary
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on the input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: 642f6a0af76b3b2d0703f0377c379abf33ecee71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732513"
---
# <a name="adiabaticstateenergyunitary-operation"></a><span data-ttu-id="90c8a-102">Операция Адиабатикстатинергюнитари</span><span class="sxs-lookup"><span data-stu-id="90c8a-102">AdiabaticStateEnergyUnitary operation</span></span>

<span data-ttu-id="90c8a-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="90c8a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="90c8a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="90c8a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="90c8a-105">Выполняет подготовку состояния, применяя к `statePrepUnitary` входному состоянию, за которым следует подготовка состояния адиабатик с помощью `adiabaticUnitary` , и, наконец, Оценка этапа с учетом `qpeUnitary` состояния с помощью `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="90c8a-105">Performs state preparation by applying a `statePrepUnitary` on the input state, followed by adiabatic state preparation using a `adiabaticUnitary`, and finally phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation AdiabaticStateEnergyUnitary (statePrepUnitary : (Qubit[] => Unit), adiabaticUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double), qubits : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="90c8a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="90c8a-106">Input</span></span>

### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="90c8a-107">Статепрепунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="90c8a-107">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="90c8a-108">Oracle, представляющий подготовку состояния для первоначального динамического генератора.</span><span class="sxs-lookup"><span data-stu-id="90c8a-108">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="adiabaticunitary--qubit--unit"></a><span data-ttu-id="90c8a-109">Адиабатикунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="90c8a-109">adiabaticUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="90c8a-110">Oracle, представляющий алгоритм эволюции адиабатик, который используется для реализации очистки до окончательного состояния алгоритма.</span><span class="sxs-lookup"><span data-stu-id="90c8a-110">An oracle representing the adiabatic evolution algorithm to be used to implement the sweeps to the final state of the algorithm.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="90c8a-111">Кпеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="90c8a-111">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="90c8a-112">Oracle, представляющий отдельный оператор $U $ представляющие развитие времени $ \делта t $ в динамическом генераторе с состоянием заземления $ \кет{\фи} $ и состоянием заземления $E = \фи \\ , \делта t $.</span><span class="sxs-lookup"><span data-stu-id="90c8a-112">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="90c8a-113">Фасисталгорисм: ([дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="90c8a-113">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="90c8a-114">Операция, выполняющая оценку этапа для данной отдельной операции.</span><span class="sxs-lookup"><span data-stu-id="90c8a-114">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="90c8a-115">Дополнительные сведения см. в статье [Оценка этапа итерации](/quantum/libraries/characterization#iterative-phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="90c8a-115">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="90c8a-116">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="90c8a-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="90c8a-117">Регистр Кубитс, который будет использоваться для моделирования.</span><span class="sxs-lookup"><span data-stu-id="90c8a-117">A register of qubits to be used to perform the simulation.</span></span>



## <a name="output--double"></a><span data-ttu-id="90c8a-118">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="90c8a-118">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="90c8a-119">Оценочное значение $ \хат{\фи} $ от земли $ \фи $ генератора, представленного $U $.</span><span class="sxs-lookup"><span data-stu-id="90c8a-119">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the generator represented by $U$.</span></span>