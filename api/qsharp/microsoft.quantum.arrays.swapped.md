---
uid: Microsoft.Quantum.Arrays.Swapped
title: Переключенная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 173fb32b5a41ce054f19548a7fcca18c11c4c4cd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220133"
---
# <a name="swapped-function"></a>Переключенная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Пример

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

