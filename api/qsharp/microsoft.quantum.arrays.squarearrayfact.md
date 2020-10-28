---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Функция Скуареаррайфакт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: f7f0573db9098feebfd481624e11119c58fd9eed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730008"
---
# <a name="squarearrayfact-function"></a>Функция Скуареаррайфакт

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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