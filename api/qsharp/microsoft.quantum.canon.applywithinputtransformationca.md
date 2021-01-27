---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationCA
title: Операция Аппливисинпуттрансформатионка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationCA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: b31ed1b3da0d5467588f4cb2e4368e68f0dbe9d5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841114"
---
# <a name="applywithinputtransformationca-operation"></a>Операция Аппливисинпуттрансформатионка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии операции, принимающей некоторые входные данные, функция, которая возвращает выходные данные, совместимые с этой операцией, и входные данные для этой функции, применяет операцию с помощью функции для преобразования входных данных в форму, ожидаемую операцией.

```qsharp
operation ApplyWithInputTransformationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl), input : 'U) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="fn--u---t"></a>FN: ' U-> '

Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.


### <a name="op--t--unit--is-adj--ctl"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, которая будет применена.


### <a name="input--u"></a>входные данные: ' U

Входные данные для функции.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U



## <a name="example"></a>Пример

Следующий вызов использует @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" для применения операции, предназначенной для @"Microsoft.Quantum.Arithmetic.BigEndian" входных данных входного типа @"Microsoft.Quantum.Arithmetic.LittleEndian" :

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Аппливисинпуттрансформатион](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатиона](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатионк](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [Microsoft. тактов. Canon. Трансформедоператион](xref:Microsoft.Quantum.Canon.TransformedOperation)