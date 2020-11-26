---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Функция Ректангулараррайфакт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220422"
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

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Скуареаррайфакт](xref:Microsoft.Quantum.Arrays.SquareArrayFact)