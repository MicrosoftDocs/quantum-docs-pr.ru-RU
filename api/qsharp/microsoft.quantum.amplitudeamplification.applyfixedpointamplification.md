---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Операция Апплификседпоинтамплификатион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: 13e70b1ebd5e3bf0996e6a76f4bffe57ca2d2250
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191539"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="14bfe-102">Операция Апплификседпоинтамплификатион</span><span class="sxs-lookup"><span data-stu-id="14bfe-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="14bfe-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="14bfe-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="14bfe-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14bfe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14bfe-105">Fixed-Point алгоритм усиления амплитуды</span><span class="sxs-lookup"><span data-stu-id="14bfe-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="14bfe-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="14bfe-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="14bfe-107">Статепрепоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="14bfe-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="14bfe-108">Единая база данных Oracle, подготавливающая начальное состояние.</span><span class="sxs-lookup"><span data-stu-id="14bfe-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="14bfe-109">Старткубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="14bfe-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="14bfe-110">Кубит регистр</span><span class="sxs-lookup"><span data-stu-id="14bfe-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="14bfe-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="14bfe-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="14bfe-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14bfe-112">Remarks</span></span>

<span data-ttu-id="14bfe-113">Старткубитс должен находиться в состоянии $ \ket{0 \кдотс 0} $.</span><span class="sxs-lookup"><span data-stu-id="14bfe-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="14bfe-114">Эта операция выполняет перебор нескольких запросов в степени $2 $ до тех пор, пока не будет достигнуто максимальное число запросов или не будет найдено целевое состояние.</span><span class="sxs-lookup"><span data-stu-id="14bfe-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>