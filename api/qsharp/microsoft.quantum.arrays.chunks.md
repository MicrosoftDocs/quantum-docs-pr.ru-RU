---
uid: Microsoft.Quantum.Arrays.Chunks
title: Блоки, функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: fe10999d35ed05908fd59b9dad8b5c0c51233ae6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730416"
---
# <a name="chunks-function"></a>Блоки, функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


Разделяет массив на несколько частей равной длины.

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a>Входные данные

### <a name="nelements--int"></a>Нелементс: [int](xref:microsoft.quantum.lang-ref.int)

Длина каждого блока.


### <a name="arr--t"></a>ARR: 'T []

Массив для разбиения.



## <a name="output--t"></a>Выходные данные: 'T [] []

Массив, содержащий каждый фрагмент исходного массива.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="remarks"></a>Remarks

Обратите внимание, что последний элемент выходных данных может быть короче, чем `nElements` `Length(arr)` , если не делится на `nElements` .