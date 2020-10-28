---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Диагональная функция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 180b7185c94d712fa02100cb97abfbb6c464d12a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730360"
---
# <a name="diagonal-function"></a>Диагональная функция

Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)

Пакеты [](https://nuget.org/packages/)


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

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. наложено](xref:Microsoft.Quantum.Arrays.Transposed)