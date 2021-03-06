---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: Функция Трансформедоператионк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 9475c5a1cc3b7e14c56c301749311a72e15f71e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852043"
---
# <a name="transformedoperationc-function"></a>Функция Трансформедоператионк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a>Входные данные

### <a name="fn--u---t"></a>FN: ' U-> '

Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.


### <a name="op--t--unit--is-ctl"></a>Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL

Операция для преобразования.



## <a name="output--u--unit--is-ctl"></a>Выходные данные: "U = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL

Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U



## <a name="example"></a>Пример

Следующий вызов использует @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" для преобразования операции, предназначенной для @"Microsoft.Quantum.Arithmetic.BigEndian" входных данных, в операцию, которая принимает входные данные типа @"Microsoft.Quantum.Arithmetic.LittleEndian" :

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Трансформедоператион](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [Microsoft. тактов. Canon. Трансформедоператиона](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [Microsoft. тактов. Canon. Трансформедоператионка](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатион](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. тактов. Canon. составной](xref:Microsoft.Quantum.Canon.Composed)