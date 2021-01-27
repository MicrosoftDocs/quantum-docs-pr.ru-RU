---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Операция Апплификседпоинтамплификатион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: fa19c3bb06ae91a2fa18acb6f853020830e749f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847234"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="63414-102">Операция Апплификседпоинтамплификатион</span><span class="sxs-lookup"><span data-stu-id="63414-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="63414-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="63414-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="63414-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="63414-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="63414-105">Fixed-Point алгоритм усиления амплитуды</span><span class="sxs-lookup"><span data-stu-id="63414-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="63414-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="63414-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="63414-107">Статепрепоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="63414-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="63414-108">Единая база данных Oracle, подготавливающая начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="63414-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="63414-109">Старткубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="63414-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="63414-110">Кубит регистр</span><span class="sxs-lookup"><span data-stu-id="63414-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="63414-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="63414-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="63414-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="63414-112">Remarks</span></span>

<span data-ttu-id="63414-113">Старткубитс должен находиться в состоянии $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="63414-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="63414-114">Эта операция выполняет перебор нескольких запросов в степени $2 $ до тех пор, пока не будет достигнуто максимальное число запросов или не будет найдено целевое состояние.</span><span class="sxs-lookup"><span data-stu-id="63414-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>