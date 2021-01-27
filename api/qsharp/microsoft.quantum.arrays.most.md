---
uid: Microsoft.Quantum.Arrays.Most
title: Большинство функций
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 2b212b38ec55f3798eb9397f03b842573173eb88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845581"
---
# <a name="most-function"></a>Большинство функций

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Создает массив, равный входному массиву, за исключением того, что последний элемент массива удален.

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="array--t"></a>массив: 'T []

Массив, к элементам которого сначала приотносятся элементы, которые образуют выходной массив.



## <a name="output--t"></a>Выходные данные: 'T []

Массив, содержащий элементы `array[0..Length(array) - 2]` .

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов массива.