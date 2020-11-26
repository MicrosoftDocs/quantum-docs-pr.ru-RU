---
uid: Microsoft.Quantum.Convert.BigIntAsBoolArray
title: Функция Бигинтасбуларрай
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BigIntAsBoolArray
qsharp.summary: Converts a given big integer to an array of Booleans. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 593fad99ef22d3c906b9f10adc07638bed227509
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224553"
---
# <a name="bigintasboolarray-function"></a><span data-ttu-id="2c2c8-102">Функция Бигинтасбуларрай</span><span class="sxs-lookup"><span data-stu-id="2c2c8-102">BigIntAsBoolArray function</span></span>

<span data-ttu-id="2c2c8-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="2c2c8-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="2c2c8-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2c2c8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2c2c8-105">Преобразует заданное большое целое число в массив логических значений.</span><span class="sxs-lookup"><span data-stu-id="2c2c8-105">Converts a given big integer to an array of Booleans.</span></span>
<span data-ttu-id="2c2c8-106">Элемент 0 массива является наименее значащим битом длинного целого числа.</span><span class="sxs-lookup"><span data-stu-id="2c2c8-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BigIntAsBoolArray (a : BigInt) : Bool[]
```


## <a name="input"></a><span data-ttu-id="2c2c8-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2c2c8-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="2c2c8-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2c2c8-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bool"></a><span data-ttu-id="2c2c8-109">Выходные данные: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="2c2c8-109">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="2c2c8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c2c8-110">Remarks</span></span>

<span data-ttu-id="2c2c8-111">Дополнительные сведения см. в разделе [конструктор C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) .</span><span class="sxs-lookup"><span data-stu-id="2c2c8-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>