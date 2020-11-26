---
uid: Microsoft.Quantum.Arrays.Transposed
title: Переданная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219997"
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