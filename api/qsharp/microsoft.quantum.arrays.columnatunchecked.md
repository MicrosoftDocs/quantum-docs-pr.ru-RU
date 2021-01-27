---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Функция Колумнатунчеккед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 4f4631bb49f769816a3df772f7b2f346c8ccfc78
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842863"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="f541e-102">Функция Колумнатунчеккед</span><span class="sxs-lookup"><span data-stu-id="f541e-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="f541e-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f541e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f541e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f541e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f541e-105">Эта функция не проверяет фигуру матрицы</span><span class="sxs-lookup"><span data-stu-id="f541e-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="f541e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f541e-106">Description</span></span>

<span data-ttu-id="f541e-107">Эту функцию можно использовать в других многомерных функциях, которые уже проверяют входную матрицу для допустимой прямоугольной фигуры.</span><span class="sxs-lookup"><span data-stu-id="f541e-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="f541e-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f541e-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="f541e-109">столбец: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f541e-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="f541e-110">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="f541e-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="f541e-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="f541e-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f541e-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="f541e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f541e-113">Е</span><span class="sxs-lookup"><span data-stu-id="f541e-113">'T</span></span>

