---
uid: Microsoft.Quantum.Arrays.Transposed
title: Переданная функция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 913f1829ef53ec3eb6944be8b8e3eb37b431f27e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850936"
---
# <a name="transposed-function"></a>Переданная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Возвращает перестановку матрицы, представленной в виде массива массивов.

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a>Описание

Входные данные в виде $r \тимес c $ Matrix с $r $ Rows и $c $ Columns.  Матрица основана на строках, т. е. `matrix[i][j]` обращается к элементу в строке $i $ и столбцу $j $.

Эта функция возвращает матрицу $c \тимес r $, которая является трансэкземпляром входной матрицы.

## <a name="input"></a>Входные данные

### <a name="matrix--t"></a>Матрица: 'T [] []

Матрица на основе строк $r \тимес c $



## <a name="output--t"></a>Выходные данные: 'T [] []

Матрица $c \тимес r $

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип каждого элемента `matrix` .

## <a name="example"></a>Пример

```qsharp
// same as [[1, 4], [2, 5], [3, 6]]
let transposed = Transposed([[1, 2, 3], [4, 5, 6]]);
```