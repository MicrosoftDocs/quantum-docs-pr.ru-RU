---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Функция Интасбуларрай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 9783a49a77bdc39ffe8c7725196eb620f4cd0100
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713452"
---
# <a name="intasboolarray-function"></a>Функция Интасбуларрай

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакеты [](https://nuget.org/packages/)


Создает двоичное представление положительного целого числа с использованием представления с прямым порядком байтов для возвращаемого массива.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>Входные данные

### <a name="number--int"></a>число: [int](xref:microsoft.quantum.lang-ref.int)

Положительное целое число, которое должно быть преобразовано в массив логических значений.


### <a name="bits--int"></a>бит: [int](xref:microsoft.quantum.lang-ref.int)

Число битов в двоичном представлении `number` .



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Массив логических значений, представляющих `number` .

## <a name="remarks"></a>Remarks

Входные данные `bits` должны находиться в диапазоне от 0 до 63.
Входные данные `number` должны находиться в диапазоне от 0 до $2 ^ {\тексттт{Битс}}-$1.