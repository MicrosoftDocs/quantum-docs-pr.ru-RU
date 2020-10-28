---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Функция Колумнат
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730408"
---
# <a name="columnat-function"></a><span data-ttu-id="61d87-102">Функция Колумнат</span><span class="sxs-lookup"><span data-stu-id="61d87-102">ColumnAt function</span></span>

<span data-ttu-id="61d87-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="61d87-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="61d87-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="61d87-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="61d87-105">Извлекает столбец из матрицы.</span><span class="sxs-lookup"><span data-stu-id="61d87-105">Extracts a column from a matrix.</span></span>

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="61d87-106">Описание</span><span class="sxs-lookup"><span data-stu-id="61d87-106">Description</span></span>

<span data-ttu-id="61d87-107">Эта функция извлекает столбец в матрице в порядке по строкам.</span><span class="sxs-lookup"><span data-stu-id="61d87-107">This function extracts a column in a matrix in row-wise order.</span></span>
<span data-ttu-id="61d87-108">Извлечение строки коррспондс к доступу к элементам первого индекса и, следовательно, не требует дальнейшей обработки.</span><span class="sxs-lookup"><span data-stu-id="61d87-108">Extracting a row corrsponds to element access of the first index and therefore requires no further treatment.</span></span>

## <a name="input"></a><span data-ttu-id="61d87-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="61d87-109">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="61d87-110">столбец: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="61d87-110">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="61d87-111">Столбец матрицы</span><span class="sxs-lookup"><span data-stu-id="61d87-111">Column of the matrix</span></span>


### <a name="matrix--t"></a><span data-ttu-id="61d87-112">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="61d87-112">matrix : 'T[][]</span></span>

<span data-ttu-id="61d87-113">двухмерную матрицу в порядке строкового уровня</span><span class="sxs-lookup"><span data-stu-id="61d87-113">2-dimensional matrix in row-wise order</span></span>



## <a name="output--t"></a><span data-ttu-id="61d87-114">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="61d87-114">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="61d87-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="61d87-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="61d87-116">Е</span><span class="sxs-lookup"><span data-stu-id="61d87-116">'T</span></span>

<span data-ttu-id="61d87-117">Тип каждого элемента `matrix` .</span><span class="sxs-lookup"><span data-stu-id="61d87-117">The type of each element of `matrix`.</span></span>

## <a name="see-also"></a><span data-ttu-id="61d87-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="61d87-118">See Also</span></span>

- [<span data-ttu-id="61d87-119">Microsoft. тактов. Arrays. наложено</span><span class="sxs-lookup"><span data-stu-id="61d87-119">Microsoft.Quantum.Arrays.Transposed</span></span>](xref:Microsoft.Quantum.Arrays.Transposed)
- [<span data-ttu-id="61d87-120">Microsoft. тактов. Arrays. по диагонали</span><span class="sxs-lookup"><span data-stu-id="61d87-120">Microsoft.Quantum.Arrays.Diagonal</span></span>](xref:Microsoft.Quantum.Arrays.Diagonal)