---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Функция Ректангулараррайфакт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: f0d3f4d6bfa9e86f1c7a91792c09e16fe86433a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730049"
---
# <a name="rectangulararrayfact-function"></a>Функция Ректангулараррайфакт

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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