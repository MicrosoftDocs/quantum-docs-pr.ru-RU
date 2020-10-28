---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Операция Апплификседпоинтамплификатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732024"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="4dc3a-102">Операция Апплификседпоинтамплификатион</span><span class="sxs-lookup"><span data-stu-id="4dc3a-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="4dc3a-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="4dc3a-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="4dc3a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4dc3a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4dc3a-105">Fixed-Point алгоритм усиления амплитуды</span><span class="sxs-lookup"><span data-stu-id="4dc3a-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="4dc3a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4dc3a-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="4dc3a-107">Статепрепоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="4dc3a-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="4dc3a-108">Единая база данных Oracle, подготавливающая начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="4dc3a-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="4dc3a-109">Старткубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="4dc3a-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="4dc3a-110">Кубит регистр</span><span class="sxs-lookup"><span data-stu-id="4dc3a-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="4dc3a-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4dc3a-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4dc3a-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="4dc3a-112">Remarks</span></span>

<span data-ttu-id="4dc3a-113">Старткубитс должен находиться в состоянии $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="4dc3a-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="4dc3a-114">Эта операция выполняет перебор нескольких запросов в степени $2 $ до тех пор, пока не будет достигнуто максимальное число запросов или не будет найдено целевое состояние.</span><span class="sxs-lookup"><span data-stu-id="4dc3a-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>