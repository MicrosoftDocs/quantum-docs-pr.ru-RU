---
uid: Microsoft.Quantum.Math.BitSizeI
title: Функция Битсизеи
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 561450ef43144aa4d7820e1f15d9300018104acd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195857"
---
# <a name="bitsizei-function"></a><span data-ttu-id="5b16c-102">Функция Битсизеи</span><span class="sxs-lookup"><span data-stu-id="5b16c-102">BitSizeI function</span></span>

<span data-ttu-id="5b16c-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="5b16c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="5b16c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5b16c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5b16c-105">Для неотрицательного целого числа `a` возвращает число битов, необходимых для представления `a` .</span><span class="sxs-lookup"><span data-stu-id="5b16c-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="5b16c-106">То есть возвращает наименьшее $n $ например, $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="5b16c-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="5b16c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5b16c-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="5b16c-108">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5b16c-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5b16c-109">Целое число, для которого требуется вычислить битовую длину.</span><span class="sxs-lookup"><span data-stu-id="5b16c-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="5b16c-110">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5b16c-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5b16c-111">Разрядный размер `a` .</span><span class="sxs-lookup"><span data-stu-id="5b16c-111">The bit-size of `a`.</span></span>