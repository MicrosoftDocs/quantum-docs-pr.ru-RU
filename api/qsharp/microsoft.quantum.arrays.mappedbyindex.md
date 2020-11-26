---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Функция Маппедбиндекс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 430495517974b641c249fa146aa9effec542e825
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209933"
---
# <a name="mappedbyindex-function"></a>Функция Маппедбиндекс

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


При наличии массива и функции, определенной для индексированных элементов массива, возвращает новый массив, состоящий из изображений исходного массива в функции.

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Входные данные

### <a name="mapper--intt---u"></a>сопоставитель: ([int](xref:microsoft.quantum.lang-ref.int), 't) — > ' U

Функция из `(Int, 'T)` в `'U` , используемая для отображения элементов и их индексов.


### <a name="array--t"></a>массив: 'T []

Массив элементов `'T` .



## <a name="output--u"></a>Выходные данные: ' U []

Массив `'U[]` элементов, сопоставленных с `mapper` функцией.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип `array` элементов.
### <a name="u"></a>' U

Тип результата `mapper` функции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. сопоставить](xref:Microsoft.Quantum.Arrays.Mapped)