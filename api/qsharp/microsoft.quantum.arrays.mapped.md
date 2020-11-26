---
uid: Microsoft.Quantum.Arrays.Mapped
title: Сопоставленная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 9632b9f53ffad8ece958ab1dc9ad446c7dcb9e13
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220745"
---
# <a name="mapped-function"></a>Сопоставленная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Комментарии

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `mapper: 'T -> 'U` мы можем сопоставлять элементы массива и создавать новый массив типа `'U[]` .