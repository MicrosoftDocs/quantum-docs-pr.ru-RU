---
uid: Microsoft.Quantum.Arrays.All
title: ALL, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 17e61ea161b90fe089b7df7c10188d604d72dcfa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842899"
---
# <a name="all-function"></a>ALL, функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива и предиката, определенного для элементов массива, и проверяет, удовлетворяет ли предикату все элементы массива.

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Входные данные

### <a name="predicate--t---bool"></a>предикат: не> [bool](xref:microsoft.quantum.lang-ref.bool)

Функция из `'T` в `Bool` , используемая для проверки элементов.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--bool"></a>Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)

`Bool`Значение функции и предиката, применяемого ко всем элементам.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.

## <a name="example"></a>Пример

Следующий код проверяет, не являются ли все элементы массива ненулевыми:

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function AllDemo() : Unit {
    let predicate = NotEqualI(_, 0);
    let isNonZero = All(predicate, [2, 3, 4, 5, 6, 0]);
    Message($"{isNonZero}");
}
```

## <a name="remarks"></a>Remarks

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `predicate: 'T -> Bool` мы можем получить `Bool` значение, которое указывает, соответствуют ли все элементы `predicate` .