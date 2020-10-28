---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Операция Мресетз
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 9f084b03504deea9fcf25e4c797c4bde3c97a995
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711057"
---
# <a name="mresetz-operation"></a>Операция Мресетз

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакеты [](https://nuget.org/packages/)


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