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
# <a name="columnat-function"></a><span data-ttu-id="0cacf-102">Функция Колумнат</span><span class="sxs-lookup"><span data-stu-id="0cacf-102">ColumnAt function</span></span>

<span data-ttu-id="0cacf-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0cacf-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0cacf-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0cacf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0cacf-105">Извлекает столбец из матрицы.</span><span class="sxs-lookup"><span data-stu-id="0cacf-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="0cacf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0cacf-106">Description</span></span>

<span data-ttu-id="0cacf-107">Эта функция извлекает столбец в матрице в порядке по строкам.</span><span class="sxs-lookup"><span data-stu-id="0cacf-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="0cacf-108">Извлечение строки коррспондс к доступу к элементам первого индекса и, следовательно, не требует дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="0cacf-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="0cacf-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0cacf-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="0cacf-110">столбец: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0cacf-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0cacf-111">Столбец матрицы</span><span class="sxs-lookup"><span data-stu-id="0cacf-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="0cacf-112">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="0cacf-112">matrix : 'T[][]</span></span>

<span data-ttu-id="0cacf-113">двухмерную матрицу в порядке строкового уровня</span><span class="sxs-lookup"><span data-stu-id="0cacf-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="0cacf-114">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="0cacf-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0cacf-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0cacf-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0cacf-116">Е</span><span class="sxs-lookup"><span data-stu-id="0cacf-116">'T</span></span>

<span data-ttu-id="0cacf-117">Тип каждого элемента `matrix` .</span><span class="sxs-lookup"><span data-stu-id="0cacf-117">The type of each element of `matrix`.</span></span>

## <a name="example"></a><span data-ttu-id="0cacf-118">Пример</span><span class="sxs-lookup"><span data-stu-id="0cacf-118">Example</span></span>

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let column = ColumnAt(0, matrix);
// same as: column = [1, 4, 7]
```

## <a name="see-also"></a><span data-ttu-id="0cacf-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="0cacf-119">See Also</span></span>

- [<span data-ttu-id="0cacf-120">Microsoft. тактов. Arrays. наложено</span><span class="sxs-lookup"><span data-stu-id="0cacf-120">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="0cacf-121">Microsoft. тактов. Arrays. по диагонали</span><span class="sxs-lookup"><span data-stu-id="0cacf-121">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)