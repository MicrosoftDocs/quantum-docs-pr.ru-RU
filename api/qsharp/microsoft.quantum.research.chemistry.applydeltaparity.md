---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Операция Апплиделтапарити
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: bb01eb684ff1820be08a573c0ca6cfc12efeb889
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733208"
---
# <a name="applydeltaparity-operation"></a>Операция Апплиделтапарити

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакеты [](https://nuget.org/packages/)


Вычисление разницы между предыдущим ПКРС... условия и следующие ПКРС... термин. Это различие вычислено на вспомогательной кубит.

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="prevfermionicterm--int"></a>Превфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]

Список индексов для предыдущего ПКРС... черт.


### <a name="nextfermionicterm--int"></a>Некстфермиониктерм: [int](xref:microsoft.quantum.lang-ref.int)[]

Список индексов для следующего ПКРС... черт.


### <a name="aux--qubit"></a>AUX: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Вспомогательная кубит, на которой сохраняются результаты вычисления четности.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубит, обрабатываемый всеми ПКРС... черт.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Предполагается, что индексы P < Q < R < S <... для Превпк и Некстпк.