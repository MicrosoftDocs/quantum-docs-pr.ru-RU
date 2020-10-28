---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: Функция Трансформедоператиона
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 349424a102dba7354bbaa65fffdc2b5d506a3b91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715328"
---
# <a name="transformedoperationa-function"></a>Функция Трансформедоператиона

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a>Входные данные

### <a name="fn--u---t"></a>FN: ' U-> '

Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.


### <a name="op--t--unit-adj"></a>Op: 'T => [единица измерения](xref:microsoft.quantum.lang-ref.unit)

Операция для преобразования.



## <a name="output--u--unit-adj"></a>Выходные данные: "U = [>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Трансформедоператион](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [Microsoft. тактов. Canon. Трансформедоператионк](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [Microsoft. тактов. Canon. Трансформедоператионка](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатион](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. тактов. Canon. составной](xref:Microsoft.Quantum.Canon.Composed)