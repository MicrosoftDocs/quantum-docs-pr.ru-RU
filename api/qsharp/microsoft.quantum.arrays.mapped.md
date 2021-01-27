---
uid: Microsoft.Quantum.Arrays.Mapped
title: Сопоставленная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 00ea0803faf6e8edfa748af63dd6c7e217b1de41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845686"
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

## <a name="remarks"></a>Remarks

Функция определена для универсальных типов, т. е. при наличии массива `'T[]` и функции `mapper: 'T -> 'U` мы можем сопоставлять элементы массива и создавать новый массив типа `'U[]` .