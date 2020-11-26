---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Функция Интасбуларрай
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: f89cb3d7ca29d7deaaf49573b2670534166caded
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224349"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="30a08-102">Функция Интасбуларрай</span><span class="sxs-lookup"><span data-stu-id="30a08-102">IntAsBoolArray function</span></span>

<span data-ttu-id="30a08-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="30a08-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="30a08-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30a08-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30a08-105">Создает двоичное представление положительного целого числа с использованием представления с прямым порядком байтов для возвращаемого массива.</span><span class="sxs-lookup"><span data-stu-id="30a08-105">Produces a binary representation of a positive integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="30a08-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="30a08-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="30a08-107">число: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="30a08-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="30a08-108">Положительное целое число, которое должно быть преобразовано в массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="30a08-108">A positive integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="30a08-109">бит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="30a08-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="30a08-110">Число битов в двоичном представлении `number` .</span><span class="sxs-lookup"><span data-stu-id="30a08-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="30a08-111">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="30a08-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="30a08-112">Массив логических значений, представляющих `number` .</span><span class="sxs-lookup"><span data-stu-id="30a08-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a08-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30a08-113">Remarks</span></span>

<span data-ttu-id="30a08-114">Входные данные `bits` должны находиться в диапазоне от 0 до 63.</span><span class="sxs-lookup"><span data-stu-id="30a08-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="30a08-115">Входные данные `number` должны находиться в диапазоне от 0 до $2 ^ {\тексттт{Битс}}-$1.</span><span class="sxs-lookup"><span data-stu-id="30a08-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>