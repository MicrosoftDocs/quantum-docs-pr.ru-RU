---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Операция Апплифзерок
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: cfc2a659f4da011baadff1a0d6a20a2a36d0a285
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718015"
---
# <a name="applyifzeroc-operation"></a>Операция Апплифзерок

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет управляемую операцию, заданную для классического результирующего значения, равного нулю.

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `Zero` . Если значение `One` равно, то ничего не происходит с `target` .
Суффикс `C` указывает, что операция, которая должна быть применена, является управляемой.

## <a name="input"></a>Входные данные

### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Результат измерения, определяющий, применяется ли оператор Op.


### <a name="op--t--unit-ctl"></a>Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL

Операция, применяемая к условию.


### <a name="target--t"></a>Целевой объект: 'T

Входные данные, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифзерок](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [Microsoft. тактов. Canon. Апплифзероа](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [Microsoft. тактов. Canon. Апплифзерока](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)