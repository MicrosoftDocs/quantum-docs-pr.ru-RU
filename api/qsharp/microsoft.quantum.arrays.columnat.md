---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Функция Колумнат
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 097b3fdd6fc1843ada27052fcf08ee80d894d25a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210107"
---
# <a name="columnat-function"></a>Функция Колумнат

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Извлекает столбец из матрицы.

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Описание

Эта функция извлекает столбец в матрице в порядке по строкам.
Извлечение строки коррспондс к доступу к элементам первого индекса и, следовательно, не требует дальнейшей обработки.

## <a name="input"></a>Входные данные

### <a name="column--int"></a>столбец: [int](xref:microsoft.quantum.lang-ref.int)

Столбец матрицы


### <a name="matrix--t"></a>Матрица: 'T [] []

двухмерную матрицу в порядке строкового уровня



## <a name="output--t"></a>Выходные данные: 'T []



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `matrix` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. наложено](xref:Microsoft.Quantum.Arrays.Transposed)
- [Microsoft. тактов. Arrays. по диагонали](xref:Microsoft.Quantum.Arrays.Diagonal)