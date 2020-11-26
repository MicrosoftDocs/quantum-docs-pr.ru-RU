---
uid: Microsoft.Quantum.Arrays.Rest
title: Функция RESTful
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: 4dd10b6e8839fd906ca9c2e36c89c626d5772149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220402"
---
# <a name="rest-function"></a>Функция RESTful

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает массив, равный входному массиву, за исключением того, что первый элемент массива удаляется.

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T []

Массив, второй с последними элементами которого образуют выходной массив.



## <a name="output--t"></a>Выходные данные: 'T []

Массив, содержащий элементы `array[1..Length(array) - 1]` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов массива.