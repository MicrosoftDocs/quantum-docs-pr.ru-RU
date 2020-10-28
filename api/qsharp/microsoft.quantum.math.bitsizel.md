---
uid: Microsoft.Quantum.Math.BitSizeL
title: Функция Битсизел
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 97068f12050317a9aa17c95f33650ef6f406066d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732753"
---
# <a name="bitsizel-function"></a><span data-ttu-id="4b6ed-102">Функция Битсизел</span><span class="sxs-lookup"><span data-stu-id="4b6ed-102">BitSizeL function</span></span>

<span data-ttu-id="4b6ed-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="4b6ed-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="4b6ed-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4b6ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4b6ed-105">Для неотрицательного целого числа `a` возвращает число битов, необходимых для представления `a` .</span><span class="sxs-lookup"><span data-stu-id="4b6ed-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="4b6ed-106">То есть возвращает наименьшее $n $ например, $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="4b6ed-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="4b6ed-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4b6ed-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="4b6ed-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="4b6ed-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="4b6ed-109">Целое число, для которого требуется вычислить битовую длину.</span><span class="sxs-lookup"><span data-stu-id="4b6ed-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="4b6ed-110">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4b6ed-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4b6ed-111">Разрядный размер `a` .</span><span class="sxs-lookup"><span data-stu-id="4b6ed-111">The bit-size of `a`.</span></span>