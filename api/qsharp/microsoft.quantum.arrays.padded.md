---
uid: Microsoft.Quantum.Arrays.Padded
title: Заполненная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 2b7a80d1cf5c82a1ff52bc4aa207cfe335b40061
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220541"
---
# <a name="padded-function"></a>Заполненная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает массив, дополненный с указанными значениями вплоть до указанной длины.

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="nelementstotal--int"></a>Нелементстотал: [int](xref:microsoft.quantum.lang-ref.int)

Длина заполненного массива. Если это положительное значение, `inputArray` то оно дополняется заголовком. Если это отрицательное значение, `inputArray` то оно дополняется на хвосте.


### <a name="defaultelement--t"></a>defaultElement: 'T

Значение по умолчанию, используемое для заполнения элементов.


### <a name="inputarray--t"></a>Инпутаррай: не[]

Массив, значения которого находятся в заголовке выходного массива.



## <a name="output--t"></a>Выходные данные: 'T []

Массив `output` , являющийся `inputArray` дополнением к заголовку с `defaultElement` s до `output` длины `nElementsTotal`

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип элементов массива.