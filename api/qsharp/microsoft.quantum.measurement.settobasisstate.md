---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Операция Сеттобасисстате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: bb40ddcf6518a30f5d88eec21cf8e2c2d6e0bbaf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733601"
---
# <a name="settobasisstate-operation"></a>Операция Сеттобасисстате

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакеты [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Remarks

В качестве инварианта этой операции вызов `M(q)` сразу после вернет значение `SetToBasisState(result, q)` `result` .