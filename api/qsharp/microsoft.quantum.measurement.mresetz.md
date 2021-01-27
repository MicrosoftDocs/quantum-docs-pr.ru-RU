---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Операция Мресетз
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: fc9ba6576b56d7df1a57334e1da46b9c48376ecb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853740"
---
# <a name="mresetz-operation"></a>Операция Мресетз

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Измеряет один кубит в Z-координате и сбрасывает его в фиксированное начальное состояние после измерения.

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a>Описание

Выполняет кубит измерение в $Z $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.

## <a name="input"></a>Входные данные

### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Один кубит, который необходимо измерять.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

Результат измерения `target` в паули $Z $.