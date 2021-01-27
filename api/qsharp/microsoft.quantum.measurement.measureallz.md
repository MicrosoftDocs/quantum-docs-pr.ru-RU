---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Операция Меасуреаллз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854670"
---
# <a name="measureallz-operation"></a>Операция Меасуреаллз

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Совместно измеряет регистр Кубитс на основе Паули Z.

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a>Описание

Измеряет регистр Кубитс в $Z \отимес Z \отимес \кдотс \отимес Z $, представляющий четность всего регистра.

## <a name="input"></a>Входные данные

### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр для измерения.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

Результат измерения $Z \отимес Z \отимес \кдотс \отимес Z $.