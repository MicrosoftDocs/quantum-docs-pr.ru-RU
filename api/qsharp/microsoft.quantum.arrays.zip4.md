---
uid: Microsoft.Quantum.Arrays.Zip4
title: Функция Zip4
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d42b3b6db059163f6c766d4f133551be293c153d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729904"
---
# <a name="zip4-function"></a>Функция Zip4

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


> [!WARNING]
> Zip4 является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped4>.

При наличии четырех массивов возвращает новый массив из 4 кортежей таким, что каждый 4 кортежа содержит элемент из каждого исходного массива.

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
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

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zip)
- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)