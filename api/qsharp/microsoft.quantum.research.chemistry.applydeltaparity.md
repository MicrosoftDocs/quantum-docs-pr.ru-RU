---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Операция Апплиделтапарити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: f5f1d74274994f042f1bc3f2e0d5332f504be02c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851107"
---
# <a name="applydeltaparity-operation"></a>Операция Апплиделтапарити

Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)

Пакет: [Microsoft. тактов. Research. Химия](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Вычисление разницы между предыдущим ПКРС... условия и следующие ПКРС... термин. Это различие вычислено на вспомогательной кубит.

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
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