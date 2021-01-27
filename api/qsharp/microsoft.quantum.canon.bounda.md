---
uid: Microsoft.Quantum.Canon.BoundA
title: Функция с ограничением
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3d0a5ba5d3d9c76289ed29e59a9c226358b83797
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844547"
---
# <a name="bounda-function"></a>Функция с ограничением

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.
Модификатор `A` указывает, что все операции в массиве являются аджоинтабле.

```qsharp
function BoundA<'T> (operations : ('T => Unit is Adj)[]) : ('T => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="operations--t--unit--is-adj"></a>операции: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является суммой []

Последовательность операций, выполняемых с заданным входом.



## <a name="output--t--unit--is-adj"></a>Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является прогода

Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором выполняется каждая операция в массиве.

## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
let bound = BoundA([U, V]);
bound(x);
```

и

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.Bound)