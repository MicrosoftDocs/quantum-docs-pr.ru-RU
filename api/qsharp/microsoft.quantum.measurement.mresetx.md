---
uid: Microsoft.Quantum.Measurement.MResetX
title: Операция Мресеткс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 04fb0f84ddf79a3d2cfc21fdaabd16c129f6d72f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194208"
---
# <a name="mresetx-operation"></a>Операция Мресеткс

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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