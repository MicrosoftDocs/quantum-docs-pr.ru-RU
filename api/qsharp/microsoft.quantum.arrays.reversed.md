---
uid: Microsoft.Quantum.Arrays.Reversed
title: Обратная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 270f15c1d10b4397e258c750876095efc2b8e951
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220439"
---
# <a name="reversed-function"></a>Обратная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создайте массив, содержащий те же элементы, что и входной массив, но в обратный порядок.

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T []

Массив, элементы которого должны быть скопированы в обратный порядок.



## <a name="output--t"></a>Выходные данные: 'T []

Массив, содержащий элементы `array[Length(array) - 1]` .. `array[0]`.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов массива.