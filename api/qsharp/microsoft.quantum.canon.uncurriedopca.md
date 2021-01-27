---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Функция Ункурриедопка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 910d8a3006a2f217888b791e479e10f9f1a6965e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840041"
---
# <a name="uncurriedopca-function"></a>Функция Ункурриедопка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.
Модификатор `CA` указывает, что операции являются управляемыми и аджоинтабле.

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a>Входные данные

### <a name="curriedop--t---u--unit--is-adj--ctl"></a>Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является" суммой + CTL "

Функция, возвращающая операции.



## <a name="output--tu--unit--is-adj--ctl"></a>Выходные данные: ('T, ' U) => [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого аргумента каррированных функции.
### <a name="u"></a>' U

Тип второго аргумента каррированных функции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Ункурриедоп](xref:Microsoft.Quantum.Canon.UncurriedOp)