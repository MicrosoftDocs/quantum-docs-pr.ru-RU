---
uid: Microsoft.Quantum.Arrays.Padded
title: Заполненная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 8742d4726e7ee32349bf3d0bd5077352ffca350b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730089"
---
# <a name="padded-function"></a>Заполненная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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