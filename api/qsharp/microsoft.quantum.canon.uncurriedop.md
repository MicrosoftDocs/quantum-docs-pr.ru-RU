---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: Функция Ункурриедоп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: d707b52bb17f4dea795fa4ff824c785e506b8b20
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852013"
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