---
uid: Microsoft.Quantum.Arrays.Rest
title: Функция RESTful
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: c14e4b2902741d7ea70c895aa715cbcaa849af3e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730048"
---
# <a name="rest-function"></a>Функция RESTful

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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