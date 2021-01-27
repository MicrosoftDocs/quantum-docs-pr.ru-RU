---
uid: Microsoft.Quantum.Canon.BoundCA
title: Функция Баундка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: 391183829a3cc8b7aa8051767dcfc6bec9638223
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844528"
---
# <a name="boundca-function"></a>Функция Баундка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.
Модификатор `CA` указывает, что все операции в массиве являются аджоинтабле и управляемыми.

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="operations--t--unit--is-adj--ctl"></a>Operations: t => [Unit](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"

Последовательность операций, выполняемых с заданным входом.



## <a name="output--t--unit--is-adj--ctl"></a>Выходные данные: 'T => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  и CTL

Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором выполняется каждая операция в массиве.

## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
let bound = BoundCA([U, V]);
bound(x);
```

и

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.Bound)