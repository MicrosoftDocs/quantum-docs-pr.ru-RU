---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: Операция Аппликнотчаин
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: c98fe24ca352952162acb7a9c4fc93d5da4285b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729688"
---
# <a name="applycnotchain-operation"></a>Операция Аппликнотчаин

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Вычисление четности регистра Кубитс на месте.

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit
```


## <a name="description"></a>Описание

Эта операция преобразует состояние входа как $ $ \бегин{алигн} \кет{q_0} \кет{q_1} \кдотс \кет{q_ {n-1}} & \мапсто \кет{q_0} \кет{q_0 \оплус q_1} \кет{q_0 \оплус q_1 \оплус q_2} \кдотс \ket{q_0 \oplus \cdots \oplus q_ {n-1}}.
\енд{алигн} $ $

## <a name="input"></a>Входные данные

### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив Кубитс, для которого необходимо вычислить и сохранить контрольные суммы.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

