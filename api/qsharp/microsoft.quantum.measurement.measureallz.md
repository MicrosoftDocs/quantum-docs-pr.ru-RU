---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Операция Меасуреаллз
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711072"
---
# <a name="measureallz-operation"></a>Операция Меасуреаллз

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакеты [](https://nuget.org/packages/)


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