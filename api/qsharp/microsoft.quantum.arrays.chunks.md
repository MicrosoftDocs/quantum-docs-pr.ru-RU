---
uid: Microsoft.Quantum.Arrays.Chunks
title: Блоки, функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: 977594839a7d2fe09de8138d32a4a50e8a752390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842870"
---
# <a name="chunks-function"></a>Блоки, функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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