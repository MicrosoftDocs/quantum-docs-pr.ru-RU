---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Функция Ректангулараррайфакт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: 8cf6b85da6e8fee7fc255a173753a6468d8134b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845486"
---
# <a name="rectangulararrayfact-function"></a>Функция Ректангулараррайфакт

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет условие, в котором двухмерный массив имеет прямоугольную фигуру

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>Описание

Эта функция утверждает, что каждая строка в массиве имеет одинаковую длину.

## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T [] []

Двухмерный массив элементов


### <a name="message--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Выводимое сообщение, если массив не является прямоугольным массивом



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `array` .

## <a name="example"></a>Пример

```qsharp
RectangularArrayFact([[1, 2], [3, 4]], "Array is not rectangular");       // okay
RectangularArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not rectangular"); // okay
RectangularArrayFact([[1, 2], [3, 4, 5]], "Array is not rectangular");    // will fail
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Скуареаррайфакт](xref:Microsoft.Quantum.Arrays.SquareArrayFact)