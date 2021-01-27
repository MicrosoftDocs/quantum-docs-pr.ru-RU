---
uid: Microsoft.Quantum.Arrays.Zip3
title: Функция zip3
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: b41b0789cdf90db534ee7a50ff25eb3a931ec683
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845356"
---
# <a name="zip3-function"></a>Функция zip3

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Zip3 является устаревшим. Взамен рекомендуется использовать <xref:Microsoft.Quantum.Arrays.Zipped3>.

При наличии трех массивов возвращает новый массив из трех кортежей, в которых каждый кортеж из трех элементов содержит элемент из каждого исходного массива.

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a>Входные данные

### <a name="first--t1"></a>Первый: 1 []

Массив, содержащий значения для первого элемента каждого кортежа.


### <a name="second--t2"></a>секунда: 'T 2 []

Массив, содержащий значения для второго элемента каждого кортежа.


### <a name="third--t3"></a>Третий: 'T 3 []

Массив, содержащий значения для третьего элемента каждого кортежа.



## <a name="output--t1t2t3"></a>Выходные данные: ('T 1, е 2, 'T 3) []

Массив, содержащий три кортежа формы `(first[idx], second[idx], third[idx])` для каждого из них `idx` . Если массивы имеют неравную длину, выходные данные будут иметь длину до более короткой из входных значений.

## <a name="type-parameters"></a>Параметры типа

### <a name="t1"></a>Т 1

Тип первого элемента массива.
### <a name="t2"></a>Е 2

Тип второго элемента массива.
### <a name="t3"></a>Т 3

Тип третьего элемента массива.

## <a name="see-also"></a>См. также:

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zip)
- [Microsoft.Quantum.Arrays.Zip4](xref:Microsoft.Quantum.Arrays.Zip4)