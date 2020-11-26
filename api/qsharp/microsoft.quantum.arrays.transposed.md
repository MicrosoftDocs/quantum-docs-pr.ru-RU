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
# <a name="transposed-function"></a><span data-ttu-id="86037-102">Переданная функция</span><span class="sxs-lookup"><span data-stu-id="86037-102">Transposed function</span></span>

<span data-ttu-id="86037-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="86037-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="86037-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="86037-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="86037-105">Возвращает перестановку матрицы, представленной в виде массива массивов.</span><span class="sxs-lookup"><span data-stu-id="86037-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="86037-106">Описание</span><span class="sxs-lookup"><span data-stu-id="86037-106">Description</span></span>

<span data-ttu-id="86037-107">Входные данные в виде $r \тимес c $ Matrix с $r $ Rows и $c $ Columns.</span><span class="sxs-lookup"><span data-stu-id="86037-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="86037-108">Матрица основана на строках, т. е. `matrix[i][j]` обращается к элементу в строке $i $ и столбцу $j $.</span><span class="sxs-lookup"><span data-stu-id="86037-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="86037-109">Эта функция возвращает матрицу $c \тимес r $, которая является трансэкземпляром входной матрицы.</span><span class="sxs-lookup"><span data-stu-id="86037-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="86037-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="86037-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="86037-111">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="86037-111">matrix : 'T[][]</span></span>

<span data-ttu-id="86037-112">Матрица на основе строк $r \тимес c $</span><span class="sxs-lookup"><span data-stu-id="86037-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="86037-113">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="86037-113">Output : 'T[][]</span></span>

<span data-ttu-id="86037-114">Матрица $c \тимес r $</span><span class="sxs-lookup"><span data-stu-id="86037-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="86037-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="86037-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="86037-116">Е</span><span class="sxs-lookup"><span data-stu-id="86037-116">'T</span></span>

<span data-ttu-id="86037-117">Тип каждого элемента `matrix` .</span><span class="sxs-lookup"><span data-stu-id="86037-117">The type of each element of `matrix`.</span></span>