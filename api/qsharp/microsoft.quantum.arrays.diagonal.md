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
# <a name="diagonal-function"></a><span data-ttu-id="ed096-102">Диагональная функция</span><span class="sxs-lookup"><span data-stu-id="ed096-102">Diagonal function</span></span>

<span data-ttu-id="ed096-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ed096-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ed096-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ed096-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ed096-105">Возвращает массив диагональных элементов двухмерного массива</span><span class="sxs-lookup"><span data-stu-id="ed096-105">Returns an array of diagonal elements of a 2-dimensional array</span></span>

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="ed096-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ed096-106">Description</span></span>

<span data-ttu-id="ed096-107">Если двухмерный массив не имеет квадратной фигуры, возвращается Диагональ от минимума до количества строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="ed096-107">If the 2-dimensional array has not a square shape, the diagonal over the minimum over the number of rows and columns will be returned.</span></span>

## <a name="input"></a><span data-ttu-id="ed096-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ed096-108">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="ed096-109">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="ed096-109">matrix : 'T[][]</span></span>

<span data-ttu-id="ed096-110">двухмерную матрицу в порядке строкового уровня</span><span class="sxs-lookup"><span data-stu-id="ed096-110">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="ed096-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="ed096-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ed096-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="ed096-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ed096-113">Е</span><span class="sxs-lookup"><span data-stu-id="ed096-113">'T</span></span>

<span data-ttu-id="ed096-114">Тип каждого элемента `matrix` .</span><span class="sxs-lookup"><span data-stu-id="ed096-114">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed096-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="ed096-115">See Also</span></span>

- [<span data-ttu-id="ed096-116">Microsoft. тактов. Arrays. наложено</span><span class="sxs-lookup"><span data-stu-id="ed096-116">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)