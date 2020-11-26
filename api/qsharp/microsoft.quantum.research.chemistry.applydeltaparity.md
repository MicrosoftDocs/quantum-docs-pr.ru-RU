---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Операция Апплиделтапарити
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: 40157b6a166b09c6fee63d86e203f92069d008f1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225760"
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



## <a name="remarks"></a>Комментарии

Предполагается, что индексы P < Q < R < S <... для Превпк и Некстпк.