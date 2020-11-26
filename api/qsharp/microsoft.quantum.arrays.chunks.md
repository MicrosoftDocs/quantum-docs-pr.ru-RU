---
uid: Microsoft.Quantum.Arrays.Chunks
title: Блоки, функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: b323fdab1b207c72a4f46d5ca4cb368ecf0df818
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221612"
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



## <a name="remarks"></a>Комментарии

Обратите внимание, что последний элемент выходных данных может быть короче, чем `nElements` `Length(arr)` , если не делится на `nElements` .