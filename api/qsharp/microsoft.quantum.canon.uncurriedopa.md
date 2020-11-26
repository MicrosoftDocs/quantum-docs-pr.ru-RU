---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Функция Ункурриедопа
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: e535d017d2665ddb76e5f422e18b8656c73171c6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204629"
---
# <a name="uncurriedopa-function"></a>Функция Ункурриедопа

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.
Модификатор `A` указывает, что операции являются аджоинтабле.

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="curriedop--t---u--unit--is-adj"></a>Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является просуммой

Функция, возвращающая операции.



## <a name="output--tu--unit--is-adj"></a>Выходные данные: ('T, ' U) => [единица](xref:microsoft.quantum.lang-ref.unit)  в сумме

Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого аргумента каррированных функции.
### <a name="u"></a>' U

Тип второго аргумента каррированных функции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Ункурриедоп](xref:Microsoft.Quantum.Canon.UncurriedOp)