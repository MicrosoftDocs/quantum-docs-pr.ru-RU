---
uid: Microsoft.Quantum.Arrays.Zip
title: Функция ZIP
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 8ed658003f749efd31b8d841cecbb0a23a471af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850903"
---
# <a name="zip-function"></a>Функция ZIP

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Пример

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zip(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a>См. также:

- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)
- [Microsoft.Quantum.Arrays.Zip4](xref:Microsoft.Quantum.Arrays.Zip4)
- [Microsoft. тактов. Arrays. unzipped](xref:Microsoft.Quantum.Arrays.Unzipped)