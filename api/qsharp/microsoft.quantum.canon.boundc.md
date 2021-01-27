---
uid: Microsoft.Quantum.Canon.BoundC
title: Функция Баундк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundC
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `C` indicates that all operations in the array are controllable.
ms.openlocfilehash: 6b640c0dab14778336f42098e699e7e68cc726df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841050"
---
# <a name="boundc-function"></a>Функция Баундк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.
Модификатор `C` указывает, что все операции в массиве являются управляемыми.

```qsharp
function BoundC<'T> (operations : ('T => Unit is Ctl)[]) : ('T => Unit is Ctl)
```


## <a name="input"></a>Входные данные

### <a name="operations--t--unit--is-ctl"></a>операции: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL []

Последовательность операций, выполняемых с заданным входом.



## <a name="output--t--unit--is-ctl"></a>Выходные данные: 'T => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL

Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором выполняется каждая операция в массиве.

## <a name="example"></a>Пример

Следующие эквивалентны:

```qsharp
let bound = BoundC([U, V]);
bound(x);
```

и

```qsharp
U(x); V(x);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.Bound)