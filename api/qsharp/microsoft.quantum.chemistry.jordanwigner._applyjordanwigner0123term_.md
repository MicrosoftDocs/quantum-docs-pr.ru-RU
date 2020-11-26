---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWigner0123Term_
title: Операция _ApplyJordanWigner0123Term_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWigner0123Term_
qsharp.summary: Applies time-evolution by a PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: bdc0b693a653761a89fa975325150de80440d18c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215985"
---
# <a name="_applyjordanwigner0123term_-operation"></a><span data-ttu-id="d6a59-102">Операция _ApplyJordanWigner0123Term_</span><span class="sxs-lookup"><span data-stu-id="d6a59-102">_ApplyJordanWigner0123Term_ operation</span></span>

<span data-ttu-id="d6a59-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="d6a59-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="d6a59-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d6a59-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d6a59-105">Применяет развитие времени по термину ПКРС, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="d6a59-105">Applies time-evolution by a PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWigner0123Term_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d6a59-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d6a59-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="d6a59-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d6a59-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="d6a59-108">`GeneratorIndex` представляет термин ПКРС.</span><span class="sxs-lookup"><span data-stu-id="d6a59-108">`GeneratorIndex` representing a PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="d6a59-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d6a59-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d6a59-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="d6a59-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="d6a59-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d6a59-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d6a59-112">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="d6a59-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d6a59-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d6a59-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

