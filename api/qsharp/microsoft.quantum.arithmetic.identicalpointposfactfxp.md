---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Функция Идентикалпоинтпосфактфксп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 907e270e1c3710fb346044ad7757171c6d5f568d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223057"
---
# <a name="identicalpointposfactfxp-function"></a>Функция Идентикалпоинтпосфактфксп

Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)

Пакет: [Microsoft. тактов. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Утверждает, что все числа с фиксированной запятой в предоставленном массиве имеют одинаковые позиции точек при подсчете из наименьшего значащих битов. Т. е. количество битов минус позиции точки должно быть константой для всех чисел с фиксированной запятой в массиве.

```qsharp
function IdenticalPointPosFactFxP (fixedPoints : Microsoft.Quantum.Arithmetic.FixedPoint[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="fixedpoints--fixedpoint"></a>Фикседпоинтс: [фикседпоинт](xref:Microsoft.Quantum.Arithmetic.FixedPoint)[]

Массив чисел с фиксированной запятой, которые будут проверяться на совместимость (с помощью утверждений).



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

