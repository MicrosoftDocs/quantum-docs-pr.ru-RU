---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: Функция Трансформедоператионка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840124"
---
# <a name="transformedoperationca-function"></a>Функция Трансформедоператионка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="fn--u---t"></a>FN: ' U-> '

Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.


### <a name="op--t--unit--is-adj--ctl"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция для преобразования.



## <a name="output--u--unit--is-adj--ctl"></a>Выходные данные: "U => [единица](xref:microsoft.quantum.lang-ref.unit)  —" года + CTL "

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