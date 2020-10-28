---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformation
title: Операция Аппливисинпуттрансформатион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformation
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 2b7863337ef724d9c3ba10201a9a01d0b2226ea8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716867"
---
# <a name="applywithinputtransformation-operation"></a>Операция Аппливисинпуттрансформатион

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии операции, принимающей некоторые входные данные, функция, которая возвращает выходные данные, совместимые с этой операцией, и входные данные для этой функции, применяет операцию с помощью функции для преобразования входных данных в форму, ожидаемую операцией.

```qsharp
operation ApplyWithInputTransformation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit), input : 'U) : Unit
```


## <a name="input"></a>Входные данные

### <a name="fn--u---t"></a>FN: ' U-> '

Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.


### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, которая будет применена.


### <a name="input--u"></a>входные данные: ' U

Входные данные для функции.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппливисинпуттрансформатиона](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатионк](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатионка](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [Microsoft. тактов. Canon. Трансформедоператион](xref:Microsoft.Quantum.Canon.TransformedOperation)