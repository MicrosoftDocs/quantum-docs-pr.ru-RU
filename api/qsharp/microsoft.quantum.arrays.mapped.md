---
uid: Microsoft.Quantum.Arrays.Mapped
title: Сопоставленная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 1abb9d6fb1a921b49554bef968442f4f2b346b71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730153"
---
# <a name="mapped-function"></a>Сопоставленная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


При наличии массива и функции, определенной для элементов массива, возвращает новый массив, состоящий из изображений исходного массива в функции.

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Входные данные

### <a name="mapper--t---u"></a>сопоставитель: не> ' U

Функция из `'T` в `'U` , используемая для отображения элементов.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--u"></a>Выходные данные: ' U []

Массив `'U[]` элементов, сопоставленных с `mapper` функцией.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.
### <a name="u"></a>' U

Тип результата `mapper` функции.

## <a name="remarks"></a>Remarks

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `mapper: 'T -> 'U` мы можем сопоставлять элементы массива и создавать новый массив типа `'U[]` .