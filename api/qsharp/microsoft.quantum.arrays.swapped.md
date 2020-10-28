---
uid: Microsoft.Quantum.Arrays.Swapped
title: Переключенная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: fa5b37b4caf5d8f19ed05075ddd7bc4217036bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729985"
---
# <a name="swapped-function"></a>Переключенная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


Применяет перестановку двух элементов в массиве.

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="firstindex--int"></a>Фирстиндекс: [int](xref:microsoft.quantum.lang-ref.int)

Индекс первого заменяемого элемента.


### <a name="secondindex--int"></a>Секондиндекс: [int](xref:microsoft.quantum.lang-ref.int)

Индекс второго заменяемого элемента.


### <a name="arr--t"></a>ARR: 'T []

Массив с элементами для обмена.



## <a name="output--t"></a>Выходные данные: 'T []

Массив с примененным переключением на месте.

## <a name="example"></a>Например, .

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

