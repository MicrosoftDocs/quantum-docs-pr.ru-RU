---
uid: Microsoft.Quantum.Arithmetic.IdenticalPointPosFactFxP
title: Функция Идентикалпоинтпосфактфксп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IdenticalPointPosFactFxP
qsharp.summary: Assert that all fixed-point numbers in the provided array have identical point positions when counting from the least- significant bit. I.e., number of bits minus point position must be constant for all fixed-point numbers in the array.
ms.openlocfilehash: 7212f918e1d0ee86b12b85caa6e0c27bc2cebe58
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846621"
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

