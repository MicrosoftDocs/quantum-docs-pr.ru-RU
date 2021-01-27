---
uid: Microsoft.Quantum.Measurement.MResetY
title: Операция Мресети
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 2e41e76a46b68178a8a22b39131d6ca2a8c50b64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854634"
---
# <a name="mresety-operation"></a>Операция Мресети

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Измеряет один кубит в базе Y и сбрасывает его в фиксированное начальное состояние после измерения.

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a>Описание

Выполняет кубит измерение в $Y $-of и гарантирует, что кубит возвращается в $ \кет {0} $ после измерения.

## <a name="input"></a>Входные данные

### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Один кубит, который необходимо измерять.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

Результат измерения `target` в паули $Y $.