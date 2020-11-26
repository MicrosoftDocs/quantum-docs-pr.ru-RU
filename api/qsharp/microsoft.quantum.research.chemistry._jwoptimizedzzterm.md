---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZZTerm
title: _JWOptimizedZZTerm операция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZZTerm
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 7fdda06b88ce03e0d76b7b589e50b460f0a5ff48
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225811"
---
# <a name="_jwoptimizedzzterm-operation"></a>_JWOptimizedZZTerm операция

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Применяет развитие времени по условию ZZ, описанному в `GeneratorIndex` .

```qsharp
operation _JWOptimizedZZTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="term--generatorindex"></a>термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` представление Терма ZZ.


### <a name="stepsize--double"></a>Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)

Длительность времени — развитие.


### <a name="parityqubit--qubit"></a>Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, определяющий знак времени — развитие.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс Хамилтониан.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

