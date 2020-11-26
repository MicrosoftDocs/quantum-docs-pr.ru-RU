---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Операция Сеттобасисстате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: 2612bfe488c830abd835be89b2f8ea6795abf675
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194157"
---
# <a name="settobasisstate-operation"></a>Операция Сеттобасисстате

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Задает кубит для заданного вычислительного состояния, измеряя кубит и применяя бит отражения при необходимости.

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="desired--__invalidresult__"></a>требуемое __: <Result> недопустимо__

Состояние основания, для которого должно быть установлено значение кубит.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, состояние которого должно быть задано.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

В качестве инварианта этой операции вызов `M(q)` сразу после вернет значение `SetToBasisState(result, q)` `result` .