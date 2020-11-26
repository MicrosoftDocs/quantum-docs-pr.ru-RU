---
uid: Microsoft.Quantum.Canon.RAll1
title: Операция RAll1
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll1
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.
ms.openlocfilehash: 36e460f93b4349bc2e3da9bfb22cb0aa82ef1795
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205540"
---
# <a name="rall1-operation"></a>Операция RAll1

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет операцию сдвига этапа.

$R = \болдоне-(1-e ^ {i \фи}) \ket{1\cdots 1} \bra{1\cdots 1} $.

```qsharp
operation RAll1 (phase : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="phase--double"></a>этап: [двойной](xref:microsoft.quantum.lang-ref.double)

Этап $ \фи $ применен к состоянию $ \ket{1\cdots 1} \bra{1\cdots 1} $.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр, состояние которого необходимо поворачивать $R $.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

