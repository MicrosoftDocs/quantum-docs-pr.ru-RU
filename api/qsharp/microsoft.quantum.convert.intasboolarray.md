---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Функция Интасбуларрай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833305"
---
# <a name="intasboolarray-function"></a>Функция Интасбуларрай

Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает двоичное представление неотрицательного целого числа, используя представление возвращаемого массива с прямым порядком байтов.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>Входные данные

### <a name="number--int"></a>число: [int](xref:microsoft.quantum.lang-ref.int)

Неотрицательное целое число, которое должно быть преобразовано в массив логических значений.


### <a name="bits--int"></a>бит: [int](xref:microsoft.quantum.lang-ref.int)

Число битов в двоичном представлении `number` .



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Массив логических значений, представляющих `number` .

## <a name="remarks"></a>Remarks

Входные данные `bits` должны находиться в диапазоне от 0 до 63.
Входные данные `number` должны находиться в диапазоне от 0 до $2 ^ {\тексттт{Битс}}-$1.