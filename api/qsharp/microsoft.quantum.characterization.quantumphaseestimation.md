---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: Операция Куантумфасистиматион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 14ba3e012f6561e7089f9fe59b2a13516b211d51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204221"
---
# <a name="quantumphaseestimation-operation"></a><span data-ttu-id="a2565-102">Операция Куантумфасистиматион</span><span class="sxs-lookup"><span data-stu-id="a2565-102">QuantumPhaseEstimation operation</span></span>

<span data-ttu-id="a2565-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="a2565-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="a2565-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a2565-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a2565-105">Выполняет алгоритм оценки тактовой фазы для заданного Oracle `U` и `targetState` считывает его в реестр такта с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="a2565-105">Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.</span></span>

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a2565-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a2565-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="a2565-107">Oracle: [дискретеоракле](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="a2565-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="a2565-108">Операция, реализующая $U ^ m $ для данного целого числа степеней m.</span><span class="sxs-lookup"><span data-stu-id="a2565-108">An operation implementing $U^m$ for given integer powers m.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="a2565-109">Таржетстате: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a2565-109">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a2565-110">Регистр такта, представляющий состояние $ \кет{\фи} $ в соответствии с $U $.</span><span class="sxs-lookup"><span data-stu-id="a2565-110">A quantum register representing the state $\ket{\phi}$ acted on by $U$.</span></span> <span data-ttu-id="a2565-111">Если $ \кет{\фи} $ является еиженстате $U $, $U \кет{\фи} = e ^ {и\фи} \кет{\фи} $ for $ \фи \ин [0, 2 \ PI) $ Неизвестный этап.</span><span class="sxs-lookup"><span data-stu-id="a2565-111">If $\ket{\phi}$ is an eigenstate of $U$, $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi \in [0, 2\pi)$ an unknown phase.</span></span>


### <a name="controlregister--bigendian"></a><span data-ttu-id="a2565-112">Контролрегистер: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="a2565-112">controlRegister : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="a2565-113">Регистр целых чисел с обратным порядком байтов, который может использоваться для управления предоставленной базой данных Oracle и будет содержать представление $ \фи $ после применения этой операции.</span><span class="sxs-lookup"><span data-stu-id="a2565-113">A big-endian representation integer register that can be used to control the provided oracle, and that will contain the a representation of $\phi$ following the application of this operation.</span></span> <span data-ttu-id="a2565-114">Предполагается, что Контролрегистер начинается в начальном состоянии $ \ket{00\cdots 0} $, где длина регистра указывает требуемую точность.</span><span class="sxs-lookup"><span data-stu-id="a2565-114">The controlRegister is assumed to start in the initial state $\ket{00\cdots 0}$, where the length of the register indicates the desired precision.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a2565-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a2565-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

