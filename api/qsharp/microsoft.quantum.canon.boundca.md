---
uid: Microsoft.Quantum.Canon.BoundCA
title: Функция Баундка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: BoundCA
qsharp.summary: Given an array of operations acting on a single input, produces a new operation that performs each given operation in sequence. The modifier `CA` indicates that all operations in the array are adjointable and controllable.
ms.openlocfilehash: d96d33781def10940479ba2eafdcc6711a0c05a5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716630"
---
# <a name="boundca-function"></a>Функция Баундка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии массива операций, исдействующих один вход, создает новую операцию, которая выполняет каждую заданную операцию последовательно.
Модификатор `CA` указывает, что все операции в массиве являются аджоинтабле и управляемыми.

```qsharp
function BoundCA<'T> (operations : ('T => Unit is Adj + Ctl)[]) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="operations--t--unit-adj--ctl"></a>операции: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL []

Последовательность операций, выполняемых с заданным входом.



## <a name="output--t--unit-adj--ctl"></a>Выходные данные: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) + CTL

Новая операция, которая выполняет каждую заданную операцию последовательно по входным данным.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Целевой объект, на котором выполняется каждая операция в массиве.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Bounds](xref:Microsoft.Quantum.Canon.Bound)