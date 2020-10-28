---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: Операция Апплифзероа
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: d324cd970e8df49ceb51b6bf5c9f3c9c3ff142f9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92718057"
---
# <a name="applyifzeroa-operation"></a>Операция Апплифзероа

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию аджоинтабле, определенную для классического результирующего значения, равным нулю.

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `Zero` . Если значение `One` равно, то ничего не происходит с `target` .
Суффикс `A` указывает, что операция, которую необходимо применить, — аджоинтабле.

## <a name="input"></a>Входные данные

### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Результат измерения, определяющий, применяется ли оператор Op.


### <a name="op--t--unit-adj"></a>Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)

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