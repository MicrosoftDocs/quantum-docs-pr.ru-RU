---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedPQandPQQRTerm
title: _JWOptimizedPQandPQQRTerm операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedPQandPQQRTerm
qsharp.summary: Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.
ms.openlocfilehash: 9d9f0d17c091ae771702e4047d17e1769d6bb294
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732160"
---
# <a name="_jwoptimizedpqandpqqrterm-operation"></a><span data-ttu-id="cbdf4-102">_JWOptimizedPQandPQQRTerm операция</span><span class="sxs-lookup"><span data-stu-id="cbdf4-102">_JWOptimizedPQandPQQRTerm operation</span></span>

<span data-ttu-id="cbdf4-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="cbdf4-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="cbdf4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cbdf4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cbdf4-105">Применяет развитие времени по термину PQ или ПККР, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="cbdf4-105">Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedPQandPQQRTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="cbdf4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cbdf4-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="cbdf4-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="cbdf4-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="cbdf4-108">`GeneratorIndex` представление термина PQ или ПККР.</span><span class="sxs-lookup"><span data-stu-id="cbdf4-108">`GeneratorIndex` representing a PQ or PQQr term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="cbdf4-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cbdf4-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cbdf4-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="cbdf4-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="cbdf4-111">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="cbdf4-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="cbdf4-112">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="cbdf4-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="cbdf4-113">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cbdf4-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cbdf4-114">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="cbdf4-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cbdf4-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cbdf4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

