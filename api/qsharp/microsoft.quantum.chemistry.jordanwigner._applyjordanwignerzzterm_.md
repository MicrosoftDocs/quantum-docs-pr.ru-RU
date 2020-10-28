---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZZTerm_
title: Операция _апплижорданвигнерззтерм_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZZTerm_
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 9f03255d53f7ed7f3e79689ea53c8b95133f6cde
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714725"
---
# <a name="_applyjordanwignerzzterm_-operation"></a><span data-ttu-id="30a35-102">Операция _апплижорданвигнерззтерм_</span><span class="sxs-lookup"><span data-stu-id="30a35-102">_ApplyJordanWignerZZTerm_ operation</span></span>

<span data-ttu-id="30a35-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="30a35-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="30a35-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="30a35-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="30a35-105">Применяет развитие времени по условию ZZ, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="30a35-105">Applies time-evolution by a ZZ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="30a35-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="30a35-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="30a35-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="30a35-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="30a35-108">`GeneratorIndex` представление Терма ZZ.</span><span class="sxs-lookup"><span data-stu-id="30a35-108">`GeneratorIndex` representing a ZZ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="30a35-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="30a35-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="30a35-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="30a35-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="30a35-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="30a35-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="30a35-112">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="30a35-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="30a35-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="30a35-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

