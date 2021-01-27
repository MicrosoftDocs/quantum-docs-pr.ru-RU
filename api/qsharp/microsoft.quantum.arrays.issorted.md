---
uid: Microsoft.Quantum.Arrays.IsSorted
title: Функция IsSorted
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: a5916b5cbf36e1b6c421a81e04016a333e2b5be7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845736"
---
# <a name="issorted-function"></a>Функция IsSorted

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива возвращает значение, указывающее, сортируется ли этот массив как определенный данной функцией сравнения.

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Входные данные

### <a name="comparison--tt---bool"></a>Сравнение: ('T) — > [bool](xref:microsoft.quantum.lang-ref.bool)

Функция, которая сравнивает два элемента, которые `a` считаются меньше или равными, `b` Если `comparison(a, b)` имеет значение `true` .


### <a name="array--t"></a>массив: 'T []

Проверяемый массив.



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` Если и только для каждой пары элементов `a` и `b` `array` в этом порядке, `comparison(a, b)` то имеет значение `true` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `array` .

## <a name="remarks"></a>Remarks

`comparison`Предполагается, что функция является транзитивным, например, если `comparison(a, b)` `comparison(b, c)` `comparison(a, c)` предполагается и. Если это свойство не удерживает, выходные данные этой функции могут быть неправильными.