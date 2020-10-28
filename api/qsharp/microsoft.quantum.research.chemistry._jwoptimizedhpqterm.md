---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedHpqTerm
title: _JWOptimizedHpqTerm операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedHpqTerm
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: 503de03a379ac0ede3754aa7a31ac2ce84e5c675
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733720"
---
# <a name="_jwoptimizedhpqterm-operation"></a><span data-ttu-id="23120-102">_JWOptimizedHpqTerm операция</span><span class="sxs-lookup"><span data-stu-id="23120-102">_JWOptimizedHpqTerm operation</span></span>

<span data-ttu-id="23120-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="23120-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="23120-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="23120-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="23120-105">Применяет развитие времени по термину PQ, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="23120-105">Applies time-evolution by a PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedHpqTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="23120-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="23120-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="23120-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="23120-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="23120-108">`GeneratorIndex` представляет термин PQ.</span><span class="sxs-lookup"><span data-stu-id="23120-108">`GeneratorIndex` representing a PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="23120-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="23120-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="23120-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="23120-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="23120-111">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="23120-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="23120-112">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="23120-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="23120-113">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="23120-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="23120-114">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="23120-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="23120-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="23120-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

