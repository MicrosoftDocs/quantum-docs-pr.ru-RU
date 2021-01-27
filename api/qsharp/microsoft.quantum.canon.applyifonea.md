---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Операция Апплифонеа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 1593f565e950a9410df0ae9de59e6d0e6a7b99b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844926"
---
# <a name="applyifonea-operation"></a>Операция Апплифонеа

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию аджоинтабле с условием для классического значения result.

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a>Описание

При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` . Если значение `Zero` равно, то ничего не происходит с `target` .
Суффикс `A` указывает, что операция, которую необходимо применить, — аджоинтабле.

## <a name="input"></a>Входные данные

### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Результат измерения, определяющий, применяется ли оператор Op.


### <a name="op--t--unit--is-adj"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой

Операция, применяемая к условию.


### <a name="target--t"></a>Целевой объект: 'T

Входные данные, к которым применяется операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна применяться условно.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплифонек](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [Microsoft. тактов. Canon. Апплифонеа](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [Microsoft. тактов. Canon. Апплифонека](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)