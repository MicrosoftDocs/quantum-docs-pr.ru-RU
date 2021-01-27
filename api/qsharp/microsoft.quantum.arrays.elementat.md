---
uid: Microsoft.Quantum.Arrays.ElementAt
title: Функция ElementAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementAt
qsharp.summary: Returns the at the given index of an array.
ms.openlocfilehash: 2d31c62a4a5ba3b273e7440b5dfe4482b47e3a8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842803"
---
# <a name="elementat-function"></a>Функция ElementAt

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает объект по указанному индексу массива.

```qsharp
function ElementAt<'T> (index : Int, array : 'T[]) : 'T
```


## <a name="input"></a>Входные данные

### <a name="index--int"></a>Индекс: [int](xref:microsoft.quantum.lang-ref.int)

Индекс элемента


### <a name="array--t"></a>массив: 'T []

Индексируемый массив.



## <a name="output--t"></a>Выходные данные: 'T



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `array` .

## <a name="example"></a>Пример

Получение третьего числа в четырех известных целочисленных последовательностях. (Обратите внимание, что индекс 0 соответствует _первому_ значению последовательности.)

```qsharp
let lucas = [2, 1, 3, 4, 7, 11, 18, 29, 47, 76];
let prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34];
let catalan = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
let famous2 = Mapped(ElementAt<Int>(2, _), [lucas, prime, fibonacci, catalan]);
// same as: famous2 = [3, 5, 1, 2]
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Лукупфунктион](xref:Microsoft.Quantum.Arrays.LookupFunction)
- [Microsoft. тактов. Arrays. Елементсат](xref:Microsoft.Quantum.Arrays.ElementsAt)