---
uid: Microsoft.Quantum.Measurement.MResetX
title: Операция Мресеткс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: a16d7405388b560edcdb6c36b6668791f7ba1398
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733792"
---
# <a name="mresetx-operation"></a>Операция Мресеткс

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакеты [](https://nuget.org/packages/)


Измеряет один кубит в базе X и сбрасывает его в фиксированное начальное состояние после измерения.

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a>Описание

Выполняет кубит измерение в $X $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.

## <a name="input"></a>Входные данные

### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Один кубит, который необходимо измерять.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

Результат измерения `target` в паули $X $.