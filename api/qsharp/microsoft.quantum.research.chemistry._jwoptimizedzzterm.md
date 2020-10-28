---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZZTerm
title: _JWOptimizedZZTerm операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZZTerm
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 824918e06e54e31834019a396b310bbaa6beeb46
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732520"
---
# <a name="_jwoptimizedzzterm-operation"></a><span data-ttu-id="8d1da-102">_JWOptimizedZZTerm операция</span><span class="sxs-lookup"><span data-stu-id="8d1da-102">_JWOptimizedZZTerm operation</span></span>

<span data-ttu-id="8d1da-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8d1da-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="8d1da-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8d1da-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8d1da-105">Применяет развитие времени по условию ZZ, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="8d1da-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedZZTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="8d1da-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8d1da-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="8d1da-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8d1da-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8d1da-108">`GeneratorIndex` представление Терма ZZ.</span><span class="sxs-lookup"><span data-stu-id="8d1da-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="8d1da-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8d1da-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8d1da-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="8d1da-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="8d1da-111">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8d1da-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8d1da-112">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="8d1da-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="8d1da-113">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8d1da-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8d1da-114">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="8d1da-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8d1da-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8d1da-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

