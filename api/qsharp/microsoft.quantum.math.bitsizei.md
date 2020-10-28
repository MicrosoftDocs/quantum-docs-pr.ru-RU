---
uid: Microsoft.Quantum.Math.BitSizeI
title: Функция Битсизеи
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7cfe03908a8a394fc8ceb1c9facbf02f3db2d48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732760"
---
# <a name="bitsizei-function"></a><span data-ttu-id="d21ce-102">Функция Битсизеи</span><span class="sxs-lookup"><span data-stu-id="d21ce-102">BitSizeI function</span></span>

<span data-ttu-id="d21ce-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d21ce-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d21ce-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d21ce-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d21ce-105">Для неотрицательного целого числа `a` возвращает число битов, необходимых для представления `a` .</span><span class="sxs-lookup"><span data-stu-id="d21ce-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="d21ce-106">То есть возвращает наименьшее $n $ например, $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="d21ce-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="d21ce-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d21ce-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="d21ce-108">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d21ce-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d21ce-109">Целое число, для которого требуется вычислить битовую длину.</span><span class="sxs-lookup"><span data-stu-id="d21ce-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="d21ce-110">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d21ce-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d21ce-111">Разрядный размер `a` .</span><span class="sxs-lookup"><span data-stu-id="d21ce-111">The bit-size of `a`.</span></span>