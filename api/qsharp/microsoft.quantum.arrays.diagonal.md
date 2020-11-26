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
# <a name="diagonal-function"></a><span data-ttu-id="8b910-102">Диагональная функция</span><span class="sxs-lookup"><span data-stu-id="8b910-102">Diagonal function</span></span>

<span data-ttu-id="8b910-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8b910-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8b910-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b910-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b910-105">Возвращает массив диагональных элементов двухмерного массива</span><span class="sxs-lookup"><span data-stu-id="8b910-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="8b910-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8b910-106">Description</span></span>

<span data-ttu-id="8b910-107">Если двухмерный массив не имеет квадратной фигуры, возвращается Диагональ от минимума до количества строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="8b910-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="8b910-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8b910-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="8b910-109">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="8b910-109">matrix : 'T[][]</span></span>

<span data-ttu-id="8b910-110">двухмерную матрицу в порядке строкового уровня</span><span class="sxs-lookup"><span data-stu-id="8b910-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="8b910-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="8b910-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8b910-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="8b910-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8b910-113">Е</span><span class="sxs-lookup"><span data-stu-id="8b910-113">'T</span></span>

<span data-ttu-id="8b910-114">Тип каждого элемента `matrix` .</span><span class="sxs-lookup"><span data-stu-id="8b910-114">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b910-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="8b910-115">See Also</span></span>

- [<span data-ttu-id="8b910-116">Microsoft. тактов. Arrays. наложено</span><span class="sxs-lookup"><span data-stu-id="8b910-116">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)