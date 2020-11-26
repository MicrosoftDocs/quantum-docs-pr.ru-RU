---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Несжатая функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: aee1d48c9e0a1f104040bc56c78fdbb8bc4d34ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219963"
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

## <a name="see-also"></a>См. также:

- [Microsoft.Quantum.Arrays.Zipпед](xref:Microsoft.Quantum.Arrays.Zipped)