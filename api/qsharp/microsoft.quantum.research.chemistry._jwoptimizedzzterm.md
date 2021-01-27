---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZZTerm
title: _JWOptimizedZZTerm операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZZTerm
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: e12d146c0f706e960294580ad4b26ca83711ce33
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844353"
---
# <a name="_jwoptimizedzzterm-operation"></a><span data-ttu-id="2fa1f-102">_JWOptimizedZZTerm операция</span><span class="sxs-lookup"><span data-stu-id="2fa1f-102">_JWOptimizedZZTerm operation</span></span>

<span data-ttu-id="2fa1f-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="2fa1f-104">Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="2fa1f-105">Применяет развитие времени по условию ZZ, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="2fa1f-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedZZTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="2fa1f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2fa1f-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="2fa1f-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="2fa1f-108">`GeneratorIndex` представление Терма ZZ.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="2fa1f-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2fa1f-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="2fa1f-111">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2fa1f-112">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="2fa1f-113">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2fa1f-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2fa1f-114">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="2fa1f-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2fa1f-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2fa1f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

