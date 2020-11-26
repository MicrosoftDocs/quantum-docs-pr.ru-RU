---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZZTerm_
title: Операция _апплижорданвигнерззтерм_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZZTerm_
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 346dc18d3d70899eab0800a3087703aa42055a04
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215866"
---
# <a name="_applyjordanwignerzzterm_-operation"></a><span data-ttu-id="3e8ac-102">Операция _апплижорданвигнерззтерм_</span><span class="sxs-lookup"><span data-stu-id="3e8ac-102">_ApplyJordanWignerZZTerm_ operation</span></span>

<span data-ttu-id="3e8ac-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="3e8ac-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="3e8ac-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3e8ac-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="3e8ac-105">Применяет развитие времени по условию ZZ, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="3e8ac-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3e8ac-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3e8ac-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="3e8ac-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3e8ac-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3e8ac-108">`GeneratorIndex` представление Терма ZZ.</span><span class="sxs-lookup"><span data-stu-id="3e8ac-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="3e8ac-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3e8ac-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3e8ac-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="3e8ac-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="3e8ac-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3e8ac-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3e8ac-112">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="3e8ac-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3e8ac-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3e8ac-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

