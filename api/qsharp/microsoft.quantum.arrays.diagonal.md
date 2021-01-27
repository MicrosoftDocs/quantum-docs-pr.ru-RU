---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Диагональная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 2857046f59a958fed106af0944b75baaa3292e96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842831"
---
# <a name="diagonal-function"></a>Диагональная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает массив диагональных элементов двухмерного массива

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Описание

Если двухмерный массив не имеет квадратной фигуры, возвращается Диагональ от минимума до количества строк и столбцов.

## <a name="input"></a>Входные данные

### <a name="matrix--t"></a>Матрица: 'T [] []

двухмерную матрицу в порядке строкового уровня



## <a name="output--t"></a>Выходные данные: 'T []



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `matrix` .

## <a name="example"></a>Пример

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let diagonal = Diagonal(matrix);
// same as: column = [1, 5, 9]
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. наложено](xref:Microsoft.Quantum.Arrays.Transposed)