---
uid: Microsoft.Quantum.Canon.TransformedOperation
title: Функция Трансформедоператион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperation
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 9f564fee38fb22283da4807f829ddc5ec156bf3d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852060"
---
# <a name="transformedoperation-function"></a>Функция Трансформедоператион

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.

```qsharp
function TransformedOperation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit)) : ('U => Unit)
```


## <a name="input"></a>Входные данные

### <a name="fn--u---t"></a>FN: ' U-> '

Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.


### <a name="op--t--unit"></a>Op: t = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция для преобразования.



## <a name="output--u--unit"></a>Выходные данные: "U =>ная [единица](xref:microsoft.quantum.lang-ref.unit) 

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

- [Microsoft. тактов. Canon. Трансформедоператиона](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [Microsoft. тактов. Canon. Трансформедоператионк](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [Microsoft. тактов. Canon. Трансформедоператионка](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатион](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. тактов. Canon. составной](xref:Microsoft.Quantum.Canon.Composed)