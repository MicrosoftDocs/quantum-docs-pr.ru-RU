---
uid: Microsoft.Quantum.Arrays.Zipped
title: Функция ZIP
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 56ed97d573bf29dddb7cdb1c3f360218bf97889a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219759"
---
# <a name="zipped-function"></a>Функция ZIP

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии двух массивов возвращает новый массив пар, в котором каждая пара содержит элемент из каждого исходного массива.

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
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

- [Microsoft.Quantum.Arrays.Zipped3](xref:Microsoft.Quantum.Arrays.Zipped3)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
- [Microsoft. тактов. Arrays. unzipped](xref:Microsoft.Quantum.Arrays.Unzipped)