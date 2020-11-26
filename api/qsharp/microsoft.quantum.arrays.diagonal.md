---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Диагональная функция
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: fe6bac0acfa07b14620c7c35ae5e1cec2287d13d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221544"
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

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. наложено](xref:Microsoft.Quantum.Arrays.Transposed)