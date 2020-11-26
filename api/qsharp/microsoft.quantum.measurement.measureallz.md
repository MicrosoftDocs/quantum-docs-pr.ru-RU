---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: Операция Меасуреаллз
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 6c44ab6a7983697644071f0e3cf106e9825661ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227086"
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