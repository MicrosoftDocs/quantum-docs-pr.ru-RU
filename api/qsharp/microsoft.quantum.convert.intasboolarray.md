---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Функция Интасбуларрай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833305"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="a4aa6-102">Функция Интасбуларрай</span><span class="sxs-lookup"><span data-stu-id="a4aa6-102">IntAsBoolArray function</span></span>

<span data-ttu-id="a4aa6-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="a4aa6-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="a4aa6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4aa6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4aa6-105">Создает двоичное представление неотрицательного целого числа, используя представление возвращаемого массива с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="a4aa6-105">Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="a4aa6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4aa6-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="a4aa6-107">число: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a4aa6-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a4aa6-108">Неотрицательное целое число, которое должно быть преобразовано в массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="a4aa6-108">A non-negative integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="a4aa6-109">бит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a4aa6-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a4aa6-110">Число битов в двоичном представлении `number` .</span><span class="sxs-lookup"><span data-stu-id="a4aa6-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a4aa6-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="a4aa6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="a4aa6-112">Массив логических значений, представляющих `number` .</span><span class="sxs-lookup"><span data-stu-id="a4aa6-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4aa6-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="a4aa6-113">Remarks</span></span>

<span data-ttu-id="a4aa6-114">Входные данные `bits` должны находиться в диапазоне от 0 до 63.</span><span class="sxs-lookup"><span data-stu-id="a4aa6-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="a4aa6-115">Входные данные `number` должны находиться в диапазоне от 0 до $2 ^ {\тексттт{Битс}}-$1.</span><span class="sxs-lookup"><span data-stu-id="a4aa6-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>