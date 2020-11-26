---
uid: Microsoft.Quantum.Canon.BoundA
title: Функция с ограничением
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `A` indicates that all operations in the array are adjointable.
ms.openlocfilehash: 3132bf198e98dd1a2b433f36b000060e7e721865
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216954"
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

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.Bound)