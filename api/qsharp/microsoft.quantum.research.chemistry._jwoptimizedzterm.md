---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZTerm
title: _JWOptimizedZTerm операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZTerm
qsharp.summary: Applies time-evolution by a Z term described by a `GeneratorIndex`.
ms.openlocfilehash: 0b54bd7916ff8294501716365c11211b4654f5ad
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732528"
---
# <a name="_jwoptimizedzterm-operation"></a><span data-ttu-id="d932d-102">_JWOptimizedZTerm операция</span><span class="sxs-lookup"><span data-stu-id="d932d-102">_JWOptimizedZTerm operation</span></span>

<span data-ttu-id="d932d-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d932d-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="d932d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d932d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d932d-105">Применяет развитие времени по Z-условию, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="d932d-105">Applies time-evolution by a Z term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedZTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d932d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d932d-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="d932d-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d932d-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="d932d-108">`GeneratorIndex` представление термина Z.</span><span class="sxs-lookup"><span data-stu-id="d932d-108">`GeneratorIndex` representing a Z term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="d932d-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d932d-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d932d-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="d932d-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="d932d-111">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d932d-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d932d-112">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="d932d-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="d932d-113">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d932d-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d932d-114">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="d932d-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d932d-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d932d-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

