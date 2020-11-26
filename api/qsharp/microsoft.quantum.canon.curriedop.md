---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Функция Курриедоп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 6c1917d6f1ee69cb29fed1ab173106af1e206533
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216631"
---
# <a name="curriedop-function"></a>Функция Курриедоп

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает перекаррированных версию операции с двумя входными данными.

Это значит, что при выполнении операции с двумя входными данными эта функция применяет карри исоморфисм $f (x, y) \екуив f (x) (y) $ для возврата операции одного входа, которая возвращает операцию одного входа.

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a>Входные данные

### <a name="op--tu--unit"></a>Op: (t, ' U) = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, входные данные которой являются парой.



## <a name="output--t---u--unit"></a>Выходные данные: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, которая принимает первый элемент пары и возвращает операцию, которая принимает в качестве входных данных второй элемент входных данных исходной операции.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого компонента функции, определенной в парах.
### <a name="u"></a>' U

Тип второго компонента функции, определенной в парах.

## <a name="remarks"></a>Комментарии

Следующие эквивалентны:

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```