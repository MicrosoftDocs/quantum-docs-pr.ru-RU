---
uid: Microsoft.Quantum.Arrays.Zipped4
title: Функция Zipped4
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d5ee10ac9776383e75bc16a5c003a8b1a65c5698
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219640"
---
# <a name="zipped4-function"></a>Функция Zipped4

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии четырех массивов возвращает новый массив из 4 кортежей таким, что каждый 4 кортежа содержит элемент из каждого исходного массива.

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a>Входные данные

### <a name="first--t1"></a>Первый: 1 []

Массив, содержащий значения для первого элемента каждого кортежа.


### <a name="second--t2"></a>секунда: 'T 2 []

Массив, содержащий значения для второго элемента каждого кортежа.


### <a name="third--t3"></a>Третий: 'T 3 []

Массив, содержащий значения для третьего элемента каждого кортежа.


### <a name="fourth--t4"></a>четвертый: 'T 4 []

Массив, содержащий значения для четвертого элемента каждого кортежа.



## <a name="output--t1t2t3t4"></a>Выходные данные: (т. е. 1, 'T 2, No 3, 'T 4) []

Массив, содержащий 4 кортежа формы `(first[idx], second[idx], third[idx], fourth[idx])` для каждого из них `idx` . Если четыре массива не имеют одинаковую длину, выходные данные будут иметь длину до более короткой из входных значений.

## <a name="type-parameters"></a>Параметры типа

### <a name="t1"></a>Т 1

Тип первого элемента массива.
### <a name="t2"></a>Е 2

Тип второго элемента массива.
### <a name="t3"></a>Т 3

Тип третьего элемента массива.
### <a name="t4"></a>No 4

Тип четвертых элементов массива.

## <a name="see-also"></a>См. также:

- [Microsoft.Quantum.Arrays.Zipпед](xref:Microsoft.Quantum.Arrays.Zipped)
- [Microsoft.Quantum.Arrays.Zipped3](xref:Microsoft.Quantum.Arrays.Zipped3)