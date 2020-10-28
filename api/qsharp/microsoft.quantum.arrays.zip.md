---
uid: Microsoft.Quantum.Arrays.Zip
title: Функция ZIP
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 32fea60fc36bfdbaa2ab2f3560f291bf4ce4fa51
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729921"
---
# <a name="zip-function"></a>Функция ZIP

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


> [!WARNING]
> ZIP является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped>.

При наличии двух массивов возвращает новый массив пар, в котором каждая пара содержит элемент из каждого исходного массива.

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a>Входные данные

### <a name="left--t"></a>Left: ' ' []

Массив, содержащий значения для первого элемента каждого кортежа.


### <a name="right--u"></a>Right: ' U []

Массив, содержащий значения для второго элемента каждого кортежа.



## <a name="output--tu"></a>Выходные данные: ('T, ' U) []

Массив, содержащий пары форм `(left[idx], right[idx])` для каждого из них `idx` . Если два массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов левого массива.
### <a name="u"></a>' U

Тип правых элементов массива.

## <a name="see-also"></a>См. также:

- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)
- [Microsoft.Quantum.Arrays.Zip4](xref:Microsoft.Quantum.Arrays.Zip4)
- [Microsoft. тактов. Arrays. unzipped](xref:Microsoft.Quantum.Arrays.Unzipped)