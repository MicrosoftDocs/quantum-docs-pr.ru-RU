---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: Операция Аппликнотчаин
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: b5a74eb66529095233c89a4ec7ea37c996458cb4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841964"
---
# <a name="applycnotchain-operation"></a>Операция Аппликнотчаин

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вычисление четности регистра Кубитс на месте.

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

Эта операция преобразует состояние входа как $ $ \бегин{алигн} \кет{q_0} \кет{q_1} \кдотс \кет{q_ {n-1}} & \мапсто \кет{q_0} \кет{q_0 \оплус q_1} \кет{q_0 \оплус q_1 \оплус q_2} \кдотс \ket{q_0 \oplus \cdots \oplus q_ {n-1}}.
\енд{алигн} $ $

## <a name="input"></a>Входные данные

### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Массив Кубитс, для которого необходимо вычислить и сохранить контрольные суммы.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

