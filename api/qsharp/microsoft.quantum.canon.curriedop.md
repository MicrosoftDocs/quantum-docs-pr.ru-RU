---
uid: Microsoft.Quantum.Canon.CurriedOp
title: Функция Курриедоп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: f811347d65a6460690163e9df631979c906bd89f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840771"
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

## <a name="remarks"></a>Remarks

Следующие эквивалентны:

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```