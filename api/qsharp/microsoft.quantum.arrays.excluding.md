---
uid: Microsoft.Quantum.Arrays.Excluding
title: Исключение функции
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 6585e619834a96953c9eae2d36a8ebe0a11dbda0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221323"
---
# <a name="excluding-function"></a>Исключение функции

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает массив, содержащий элементы другого массива, за исключением элементов в указанном списке индексов.

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="remove--int"></a>Remove: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив индексов, обозначающий, какие элементы следует исключить из выходных данных.


### <a name="array--t"></a>массив: 'T []

Массив, в котором берутся значения в выходном массиве.



## <a name="output--t"></a>Выходные данные: 'T []

Массив, `output` который `output[0]` является первым элементом, `array` индекс которого не отображается в `remove` , например, `output[1]` вторым таким элементом и т. д.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов массива.