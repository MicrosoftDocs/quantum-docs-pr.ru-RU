---
uid: Microsoft.Quantum.Arrays.ColumnAtUnchecked
title: Функция Колумнатунчеккед
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAtUnchecked
qsharp.summary: This function does not check for matrix shape
ms.openlocfilehash: 17211c1ae1fe12fcadf34a9411f9b0cf0cdcab50
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730401"
---
# <a name="columnatunchecked-function"></a><span data-ttu-id="0b382-102">Функция Колумнатунчеккед</span><span class="sxs-lookup"><span data-stu-id="0b382-102">ColumnAtUnchecked function</span></span>

<span data-ttu-id="0b382-103">Пространство имен: [Microsoft. тактов. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0b382-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0b382-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0b382-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0b382-105">Эта функция не проверяет фигуру матрицы</span><span class="sxs-lookup"><span data-stu-id="0b382-105">This function does not check for matrix shape</span></span>

```qsharp
function ColumnAtUnchecked<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="0b382-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0b382-106">Description</span></span>

<span data-ttu-id="0b382-107">Эту функцию можно использовать в других многомерных функциях, которые уже проверяют входную матрицу для допустимой прямоугольной фигуры.</span><span class="sxs-lookup"><span data-stu-id="0b382-107">This function can be used in other multidimensional functions, which already check the input matrix for a valid rectangular shape.</span></span>

## <a name="input"></a><span data-ttu-id="0b382-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0b382-108">Input</span></span>

### <a name="column--int"></a><span data-ttu-id="0b382-109">столбец: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0b382-109">column : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="matrix--t"></a><span data-ttu-id="0b382-110">Матрица: 'T [] []</span><span class="sxs-lookup"><span data-stu-id="0b382-110">matrix : 'T[][]</span></span>





## <a name="output--t"></a><span data-ttu-id="0b382-111">Выходные данные: 'T []</span><span class="sxs-lookup"><span data-stu-id="0b382-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="0b382-112">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0b382-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0b382-113">Е</span><span class="sxs-lookup"><span data-stu-id="0b382-113">'T</span></span>

