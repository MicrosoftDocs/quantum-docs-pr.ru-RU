---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Функция Курриедоп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 13bc3e195d8a4ba26b726f96e4dc6b83da43c3e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716364"
---
# <a name="curriedop-function"></a>Функция Курриедоп

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```