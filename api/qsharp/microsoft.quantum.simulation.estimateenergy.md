---
uid: Microsoft.Quantum.Simulation.EstimateEnergy
title: Операция Естиматинерги
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EstimateEnergy
qsharp.summary: Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.
ms.openlocfilehash: ba4a5372aaf092c3ac3a1302f9715ca643be8436
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732105"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="73912-102">Операция Естиматинерги</span><span class="sxs-lookup"><span data-stu-id="73912-102">EstimateEnergy operation</span></span>

<span data-ttu-id="73912-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="73912-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="73912-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="73912-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="73912-105">Выполняет подготовку состояния, применяя к `statePrepUnitary` выводимой оценке этапа входного состояния по отношению к `qpeUnitary` результирующему состоянию с помощью `phaseEstAlgorithm` .</span><span class="sxs-lookup"><span data-stu-id="73912-105">Performs state preparation by applying a `statePrepUnitary` on an automatically allocated input state phase estimation with respect to `qpeUnitary`on the resulting state using a `phaseEstAlgorithm`.</span></span>

```qsharp
operation EstimateEnergy (nQubits : Int, statePrepUnitary : (Qubit[] => Unit), qpeUnitary : (Qubit[] => Unit is Adj + Ctl), phaseEstAlgorithm : ((Microsoft.Quantum.Oracles.DiscreteOracle, Qubit[]) => Double)) : Double
```


## <a name="input"></a><span data-ttu-id="73912-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="73912-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="73912-107">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="73912-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="73912-108">Число Кубитс, используемых для моделирования.</span><span class="sxs-lookup"><span data-stu-id="73912-108">Number of qubits used to perform simulation.</span></span>


### <a name="stateprepunitary--qubit--unit"></a><span data-ttu-id="73912-109">Статепрепунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="73912-109">statePrepUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="73912-110">Oracle, представляющий подготовку состояния для первоначального динамического генератора.</span><span class="sxs-lookup"><span data-stu-id="73912-110">An oracle representing state preparation for the initial dynamical generator.</span></span>


### <a name="qpeunitary--qubit--unit-adj--ctl"></a><span data-ttu-id="73912-111">Кпеунитари: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="73912-111">qpeUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="73912-112">Oracle, представляющий отдельный оператор $U $ представляющие развитие времени $ \делта t $ в динамическом генераторе с состоянием заземления $ \кет{\фи} $ и состоянием заземления $E = \фи \\ , \делта t $.</span><span class="sxs-lookup"><span data-stu-id="73912-112">An oracle representing a unitary operator $U$ representing evolution for time $\delta t$ under a dynamical generator with ground state $\ket{\phi}$ and ground state energy $E = \phi\\,\delta t$.</span></span>


### <a name="phaseestalgorithm--discreteoraclequbit--double"></a><span data-ttu-id="73912-113">Фасисталгорисм: ([дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) => [double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73912-113">phaseEstAlgorithm : ([DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Double](xref:microsoft.quantum.lang-ref.double)</span></span> 

<span data-ttu-id="73912-114">Операция, выполняющая оценку этапа для данной отдельной операции.</span><span class="sxs-lookup"><span data-stu-id="73912-114">An operation that performs phase estimation on a given unitary operation.</span></span>
<span data-ttu-id="73912-115">Дополнительные сведения см. в статье [Оценка этапа итерации](/quantum/libraries/characterization#iterative-phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="73912-115">See [iterative phase estimation](/quantum/libraries/characterization#iterative-phase-estimation) for more details.</span></span>



## <a name="output--double"></a><span data-ttu-id="73912-116">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="73912-116">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="73912-117">Оценка $ \хат{\фи} $ в энергетическом состоянии Energy $ \фи $ от силы заземления генератора, представленного $U $.</span><span class="sxs-lookup"><span data-stu-id="73912-117">An estimate $\hat{\phi}$ of the ground state energy $\phi$ of the ground state energy of the generator represented by $U$.</span></span>