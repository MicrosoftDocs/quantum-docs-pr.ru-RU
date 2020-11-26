---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Функция Ункурриедоп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: cad508f166d4af805cb98cd21a0260d9babb6a4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204646"
---
# <a name="uncurriedop-function"></a>Функция Ункурриедоп

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции, возвращающей операции, возвращает новую операцию, которая принимает оба входа как кортеж.

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a>Входные данные

### <a name="curriedop--t---u--unit"></a>Курриедоп: не> "U = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Функция, возвращающая операции.



## <a name="output--tu--unit"></a>Выходные данные: ('T, ' U) = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Новая операция `op` , которая `op(t, u)` эквивалентна `(curriedOp(t))(u)` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого входного параметра для перекаррированных операции.
### <a name="u"></a>' U

Тип второго входного параметра для перекаррированных операции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Ункурриедопк](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [Microsoft. тактов. Canon. Ункурриедопа](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [Microsoft. тактов. Canon. Ункурриедопка](xref:Microsoft.Quantum.Canon.UncurriedOpCA)