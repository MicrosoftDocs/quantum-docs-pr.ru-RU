---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Несжатая функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845378"
---
# <a name="unzipped-function"></a>Несжатая функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива из двух кортежей функция возвращает кортеж с двумя массивами, каждый из которых содержит элементы кортежей входного массива.

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a>Входные данные

### <a name="arr--tu"></a>ARR: ('T, ' U) []

Массив, содержащий два кортежа



## <a name="output--tu"></a>Выходные данные: ('T [], ' U [])

Два массива, первый из которых содержит все первые элементы входных кортежей, второй из которых содержит все остальные элементы входных кортежей.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип первого элемента в каждом кортеже
### <a name="u"></a>' U

Тип второго элемента в каждом кортеже

## <a name="example"></a>Пример

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a>См. также:

- [Microsoft.Quantum.Arrays.Zipпед](xref:Microsoft.Quantum.Arrays.Zipped)