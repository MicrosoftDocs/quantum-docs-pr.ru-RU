---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Функция Колумнат
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 32dc814de9b04563c2798a768f121723a1a8252c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846257"
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

## <a name="example"></a>Пример

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let column = ColumnAt(0, matrix);
// same as: column = [1, 4, 7]
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. наложено](xref:Microsoft.Quantum.Arrays.Transposed)
- [Microsoft. тактов. Arrays. по диагонали](xref:Microsoft.Quantum.Arrays.Diagonal)