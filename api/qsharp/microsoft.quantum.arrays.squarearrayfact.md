---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Функция Скуареаррайфакт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: 3529718f0c903266d21fd593c11c0149dae0fa2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220201"
---
# <a name="squarearrayfact-function"></a>Функция Скуареаррайфакт

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет условие, которое двумерный массив имеет квадратную фигуру

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>Описание

Эта функция утверждает, что каждая строка в массиве содержит столько элементов, сколько строк (элементов) в массиве.

## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T [] []

Двухмерный массив элементов


### <a name="message--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Выводимое сообщение, если массив не является квадратным массивом



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `array` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Ректангулараррайфакт](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)