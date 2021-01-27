---
uid: Microsoft.Quantum.Convert.BigIntAsBoolArray
title: Функция Бигинтасбуларрай
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BigIntAsBoolArray
qsharp.summary: Converts a given big integer to an array of Booleans. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 1ce83389f2ac3ce9ab2898f9d167941ca2973508
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834591"
---
# <a name="bigintasboolarray-function"></a><span data-ttu-id="240e6-102">Функция Бигинтасбуларрай</span><span class="sxs-lookup"><span data-stu-id="240e6-102">BigIntAsBoolArray function</span></span>

<span data-ttu-id="240e6-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="240e6-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="240e6-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="240e6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="240e6-105">Преобразует заданное большое целое число в массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="240e6-105">Converts a given big integer to an array of Booleans.</span></span>
<span data-ttu-id="240e6-106">Элемент 0 массива является наименее значащим битом длинного целого числа.</span><span class="sxs-lookup"><span data-stu-id="240e6-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BigIntAsBoolArray (a : BigInt) : Bool[]
```


## <a name="input"></a><span data-ttu-id="240e6-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="240e6-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="240e6-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="240e6-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bool"></a><span data-ttu-id="240e6-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="240e6-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="240e6-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="240e6-110">Remarks</span></span>

<span data-ttu-id="240e6-111">Дополнительные сведения см. в разделе [конструктор C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) .</span><span class="sxs-lookup"><span data-stu-id="240e6-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>