---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: Операция Апплифонека
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 8b27a192c66a127fe5a8acfbba7b78314988bf2e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844915"
---
# <a name="applyifoneca-operation"></a>Операция Апплифонека

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет единую операцию с условием для классического результирующего значения One.

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

При наличии операции `op` и результирующего значения `result` применяется `op` к, `target` Если имеет `result` значение `One` . Если значение `Zero` равно, то ничего не происходит с `target` .
Суффикс `CA` указывает, что применяемая операция является единой (управляемой и аджоинтабле).

## <a name="input"></a>Входные данные

### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Результат измерения, определяющий, применяется ли оператор Op.


### <a name="op--t--unit--is-adj--ctl"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

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