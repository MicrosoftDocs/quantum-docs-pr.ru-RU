---
uid: Microsoft.Quantum.Arrays.Exclude
title: Функция Exclude
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: e1fa7e728d4846db90872055454a8182a77a518b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730289"
---
# <a name="exclude-function"></a>Функция Exclude

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


Возвращает массив, содержащий элементы другого массива, за исключением элементов в указанном списке индексов.

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
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