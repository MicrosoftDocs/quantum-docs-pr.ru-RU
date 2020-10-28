---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: Функция Ункурриедопка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715202"
---
# <a name="uncurriedopca-function"></a>Функция Ункурриедопка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.
Модификатор `CA` указывает, что операции являются управляемыми и аджоинтабле.

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a>Входные данные

### <a name="curriedop--t---u--unit-ctl--adj"></a>Курриедоп: не> "U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

Функция, возвращающая операции.



## <a name="output--tu--unit-ctl--adj"></a>Выходные данные: ('T, "U" => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого аргумента каррированных функции.
### <a name="u"></a>' U

Тип второго аргумента каррированных функции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Ункурриедоп](xref:Microsoft.Quantum.Canon.UncurriedOp)