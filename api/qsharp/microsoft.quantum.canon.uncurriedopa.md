---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: Функция Ункурриедопа
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: feb5da771ee6cb6a750fa76f9ffd8f5a3e0b5734
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840054"
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