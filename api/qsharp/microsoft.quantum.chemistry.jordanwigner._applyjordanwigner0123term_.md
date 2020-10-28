---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWigner0123Term_
title: Операция _ApplyJordanWigner0123Term_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWigner0123Term_
qsharp.summary: Applies time-evolution by a PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: 36590b2ee9f6f6c2b5e076f8e334dfe7b0144e5e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714823"
---
# <a name="_applyjordanwigner0123term_-operation"></a><span data-ttu-id="78fb3-102">Операция _ApplyJordanWigner0123Term_</span><span class="sxs-lookup"><span data-stu-id="78fb3-102">_ApplyJordanWigner0123Term_ operation</span></span>

<span data-ttu-id="78fb3-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="78fb3-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="78fb3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="78fb3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="78fb3-105">Применяет развитие времени по термину ПКРС, описанному в `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="78fb3-105">Applies time-evolution by a PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWigner0123Term_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="78fb3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="78fb3-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="78fb3-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="78fb3-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="78fb3-108">`GeneratorIndex` представляет термин ПКРС.</span><span class="sxs-lookup"><span data-stu-id="78fb3-108">`GeneratorIndex` representing a PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="78fb3-109">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="78fb3-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="78fb3-110">Длительность времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="78fb3-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="78fb3-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="78fb3-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="78fb3-112">Кубитс Хамилтониан.</span><span class="sxs-lookup"><span data-stu-id="78fb3-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="78fb3-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="78fb3-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

