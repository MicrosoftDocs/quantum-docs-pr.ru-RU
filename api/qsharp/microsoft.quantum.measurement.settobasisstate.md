---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Операция Сеттобасисстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: dfa054360a5e82b7ae6ec5a6d52e7d5fe566f42e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854623"
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



## <a name="remarks"></a>Remarks

В качестве инварианта этой операции вызов `M(q)` сразу после вернет значение `SetToBasisState(result, q)` `result` .