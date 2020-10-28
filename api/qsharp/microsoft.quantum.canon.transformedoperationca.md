---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: Функция Трансформедоператионка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 21c9cdfc3b5b266cb3b93e52ee2fa4c655caf795
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715314"
---
# <a name="transformedoperationca-function"></a>Функция Трансформедоператионка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


При наличии функции и операции возвращает новую операцию, входные данные которой преобразуются в заданную функцию.

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="fn--u---t"></a>FN: ' U-> '

Функция, которая преобразует заданные входные данные в форму, ожидаемую операцией.


### <a name="op--t--unit-adj--ctl"></a>Op: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL

Операция для преобразования.



## <a name="output--u--unit-adj--ctl"></a>Выходные данные: "U => [единицы](xref:microsoft.quantum.lang-ref.unit) + CTL

Новая операция `fn` , тбат, вызывает с входными данными, а затем передает полученный результат в `op` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е


### <a name="u"></a>' U



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Трансформедоператион](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [Microsoft. тактов. Canon. Трансформедоператиона](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [Microsoft. тактов. Canon. Трансформедоператионка](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Microsoft. тактов. Canon. Аппливисинпуттрансформатион](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. тактов. Canon. составной](xref:Microsoft.Quantum.Canon.Composed)