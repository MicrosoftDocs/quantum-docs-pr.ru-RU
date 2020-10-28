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
# <a name="transposed-function"></a><span data-ttu-id="df441-102">Переданная функция</span><span class="sxs-lookup"><span data-stu-id="df441-102">Transposed function</span></span>

<span data-ttu-id="df441-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="df441-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="df441-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="df441-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="df441-105">Возвращает перестановку матрицы, представленной в виде массива массивов.</span><span class="sxs-lookup"><span data-stu-id="df441-105">Returns the transpose of a matrix represented as an array of arrays.</span></span>

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="df441-106">Описание</span><span class="sxs-lookup"><span data-stu-id="df441-106">Description</span></span>

<span data-ttu-id="df441-107">Входные данные в виде $r \тимес c $ Matrix с $r $ Rows и $c $ Columns.</span><span class="sxs-lookup"><span data-stu-id="df441-107">Input as an $r \times c$ matrix with $r$ rows and $c$ columns.</span></span>  <span data-ttu-id="df441-108">Матрица основана на строках, т. е. `matrix[i][j]` обращается к элементу в строке $i $ и столбцу $j $.</span><span class="sxs-lookup"><span data-stu-id="df441-108">The matrix is row-based, i.e., `matrix[i][j]` accesses the element at row $i$ and column $j$.</span></span>

<span data-ttu-id="df441-109">Эта функция возвращает матрицу $c \тимес r $, которая является трансэкземпляром входной матрицы.</span><span class="sxs-lookup"><span data-stu-id="df441-109">This function returns the $c \times r$ matrix that is the transpose of the input matrix.</span></span>

## <a name="input"></a><span data-ttu-id="df441-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="df441-110">Input</span></span>

### <a name="matrix--t"></a><span data-ttu-id="df441-111">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="df441-111">matrix : 'T[][]</span></span>

<span data-ttu-id="df441-112">Матрица на основе строк $r \тимес c $</span><span class="sxs-lookup"><span data-stu-id="df441-112">Row-based $r \times c$ matrix</span></span>



## <a name="output--t"></a><span data-ttu-id="df441-113">Выходные данные: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="df441-113">Output : 'T[][]</span></span>

<span data-ttu-id="df441-114">Матрица $c \тимес r $</span><span class="sxs-lookup"><span data-stu-id="df441-114">Transposed $c \times r$ matrix</span></span>

## <a name="type-parameters"></a><span data-ttu-id="df441-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="df441-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="df441-116">Е</span><span class="sxs-lookup"><span data-stu-id="df441-116">'T</span></span>

<span data-ttu-id="df441-117">Тип каждого элемента `matrix` .</span><span class="sxs-lookup"><span data-stu-id="df441-117">The type of each element of `matrix`.</span></span>