---
uid: Microsoft.Quantum.Math.BitSizeL
title: Функция Битсизел
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: c94d873d7117fd2ee66226fab6d4bfc5b33bc46d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848915"
---
# <a name="bitsizel-function"></a><span data-ttu-id="b391a-102">Функция Битсизел</span><span class="sxs-lookup"><span data-stu-id="b391a-102">BitSizeL function</span></span>

<span data-ttu-id="b391a-103">Пространство имен: [Microsoft. тактов. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b391a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b391a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b391a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b391a-105">Для неотрицательного целого числа `a` возвращает число битов, необходимых для представления `a` .</span><span class="sxs-lookup"><span data-stu-id="b391a-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="b391a-106">То есть возвращает наименьшее $n $ например, $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="b391a-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="b391a-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b391a-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="b391a-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b391a-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b391a-109">Целое число, для которого требуется вычислить битовую длину.</span><span class="sxs-lookup"><span data-stu-id="b391a-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="b391a-110">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b391a-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b391a-111">Разрядный размер `a` .</span><span class="sxs-lookup"><span data-stu-id="b391a-111">The bit-size of `a`.</span></span>