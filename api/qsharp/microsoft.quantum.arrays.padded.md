---
uid: Microsoft.Quantum.Arrays.Padded
title: Заполненная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 556e5f5175ee54470a99f32c037eeb2cd80588d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845565"
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

## <a name="example"></a>Пример

```qsharp
let array = [10, 11, 12];
// The following line returns [10, 12, 15, 2, 2, 2].
let output = Padded(-6, array, 2);
// The following line returns [2, 2, 2, 10, 12, 15].
let output = Padded(6, array, 2);
```