---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Функция Интасбуларрай
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 9783a49a77bdc39ffe8c7725196eb620f4cd0100
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713452"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="00b4c-102">Функция Интасбуларрай</span><span class="sxs-lookup"><span data-stu-id="00b4c-102">IntAsBoolArray function</span></span>

<span data-ttu-id="00b4c-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="00b4c-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="00b4c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="00b4c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="00b4c-105">Создает двоичное представление положительного целого числа с использованием представления с прямым порядком байтов для возвращаемого массива.</span><span class="sxs-lookup"><span data-stu-id="00b4c-105">Produces a binary representation of a positive integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="00b4c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="00b4c-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="00b4c-107">число: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="00b4c-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="00b4c-108">Положительное целое число, которое должно быть преобразовано в массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="00b4c-108">A positive integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="00b4c-109">бит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="00b4c-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="00b4c-110">Число битов в двоичном представлении `number` .</span><span class="sxs-lookup"><span data-stu-id="00b4c-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="00b4c-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="00b4c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="00b4c-112">Массив логических значений, представляющих `number` .</span><span class="sxs-lookup"><span data-stu-id="00b4c-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="00b4c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="00b4c-113">Remarks</span></span>

<span data-ttu-id="00b4c-114">Входные данные `bits` должны находиться в диапазоне от 0 до 63.</span><span class="sxs-lookup"><span data-stu-id="00b4c-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="00b4c-115">Входные данные `number` должны находиться в диапазоне от 0 до $2 ^ {\тексттт{Битс}}-$1.</span><span class="sxs-lookup"><span data-stu-id="00b4c-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>