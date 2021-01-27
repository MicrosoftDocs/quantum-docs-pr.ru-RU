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
# <a name="diagonal-function"></a><span data-ttu-id="e7ef2-102">Диагональная функция</span><span class="sxs-lookup"><span data-stu-id="e7ef2-102">Diagonal function</span></span>

<span data-ttu-id="e7ef2-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e7ef2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e7ef2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e7ef2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e7ef2-105">Возвращает массив диагональных элементов двухмерного массива</span><span class="sxs-lookup"><span data-stu-id="e7ef2-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="e7ef2-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e7ef2-106">Description</span></span>

<span data-ttu-id="e7ef2-107">Если двухмерный массив не имеет квадратной фигуры, возвращается Диагональ от минимума до количества строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="e7ef2-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="e7ef2-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e7ef2-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="e7ef2-109">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="e7ef2-109">matrix : 'T[][]</span></span>

<span data-ttu-id="e7ef2-110">двухмерную матрицу в порядке строкового уровня</span><span class="sxs-lookup"><span data-stu-id="e7ef2-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="e7ef2-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="e7ef2-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e7ef2-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e7ef2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e7ef2-113">Е</span><span class="sxs-lookup"><span data-stu-id="e7ef2-113">'T</span></span>

<span data-ttu-id="e7ef2-114">Тип каждого элемента `matrix` .</span><span class="sxs-lookup"><span data-stu-id="e7ef2-114">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="e7ef2-115">Пример</span><span class="sxs-lookup"><span data-stu-id="e7ef2-115">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let diagonal = Diagonal(matrix);
// same as: column = [1, 5, 9]
```

## <a name="see-also"></a><span data-ttu-id="e7ef2-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="e7ef2-116">See Also</span></span>

- [<span data-ttu-id="e7ef2-117">Microsoft. тактов. Arrays. наложено</span><span class="sxs-lookup"><span data-stu-id="e7ef2-117">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)