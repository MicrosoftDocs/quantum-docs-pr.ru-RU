---
uid: Microsoft.Quantum.Arrays.Reversed
title: Обратная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 50699465711de45ff994095e6c098550d637d608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845454"
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