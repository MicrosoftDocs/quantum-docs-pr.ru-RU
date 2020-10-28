---
uid: Microsoft.Quantum.Arrays.Transposed
title: Переданная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 54071c461cf9f9411c332763b81e3bc448fb6c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92729977"
---
# <a name="transposed-function"></a>Переданная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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