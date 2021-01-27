---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZTerm_
title: Операция _апплижорданвигнерзтерм_
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZTerm_
qsharp.summary: Applies time-evolution by a Z term described by a `GeneratorIndex`.
ms.openlocfilehash: c27255409061a28668270d69133fbccb6b01b493
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839539"
---
# <a name="_applyjordanwignerzterm_-operation"></a><span data-ttu-id="288d3-102">Операция _апплижорданвигнерзтерм_</span><span class="sxs-lookup"><span data-stu-id="288d3-102">_ApplyJordanWignerZTerm_ operation</span></span>

<span data-ttu-id="288d3-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="288d3-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="288d3-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="288d3-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="288d3-105">Применяет развитие времени по Z-условию, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="288d3-105">Applies time-evolution by a Z term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="288d3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="288d3-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="288d3-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="288d3-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="288d3-108">`GeneratorIndex` представление термина Z.</span><span class="sxs-lookup"><span data-stu-id="288d3-108">`GeneratorIndex` representing a Z term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="288d3-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="288d3-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="288d3-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="288d3-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="288d3-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="288d3-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="288d3-112">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="288d3-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="288d3-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="288d3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

