---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: Функция Ункурриедопк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 05df99dce8b167f32078ce256748647ceb94d0fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851988"
---
# <a name="uncurriedopc-function"></a>Функция Ункурриедопк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.
Модификатор `C` указывает, что операции являются управляемыми.

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a>Входные данные

### <a name="curriedop--t---u--unit--is-ctl"></a>Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL

Функция, возвращающая операции.



## <a name="output--tu--unit--is-ctl"></a>Выходные данные: ('T, ' U) => [единица](xref:microsoft.quantum.lang-ref.unit)  является CTL

Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого аргумента каррированных функции.
### <a name="u"></a>' U

Тип второго аргумента каррированных функции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Ункурриедоп](xref:Microsoft.Quantum.Canon.UncurriedOp)