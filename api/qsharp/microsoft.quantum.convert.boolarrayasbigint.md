---
uid: Microsoft.Quantum.Convert.BoolArrayAsBigInt
title: Функция Буларрайасбигинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsBigInt
qsharp.summary: Converts a given array of Booleans to an equivalent big integer. The 0 element of the array is the least significant bit of the big integer.
ms.openlocfilehash: 220a733b94fd62cef21ab13e1cb3d3f973861506
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834417"
---
# <a name="boolarrayasbigint-function"></a><span data-ttu-id="ac9cf-102">Функция Буларрайасбигинт</span><span class="sxs-lookup"><span data-stu-id="ac9cf-102">BoolArrayAsBigInt function</span></span>

<span data-ttu-id="ac9cf-103">Пространство имен: [Microsoft. тактов. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="ac9cf-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="ac9cf-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ac9cf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ac9cf-105">Преобразует заданный массив логических значений в эквивалентное большое целое число.</span><span class="sxs-lookup"><span data-stu-id="ac9cf-105">Converts a given array of Booleans to an equivalent big integer.</span></span>
<span data-ttu-id="ac9cf-106">Элемент 0 массива является наименее значащим битом длинного целого числа.</span><span class="sxs-lookup"><span data-stu-id="ac9cf-106">The 0 element of the array is the least significant bit of the big integer.</span></span>

```qsharp
function BoolArrayAsBigInt (a : Bool[]) : BigInt
```


## <a name="input"></a><span data-ttu-id="ac9cf-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ac9cf-107">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="ac9cf-108">a: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="ac9cf-108">a : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>





## <a name="output--bigint"></a><span data-ttu-id="ac9cf-109">Выходные данные: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ac9cf-109">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="ac9cf-110">Remarks</span><span class="sxs-lookup"><span data-stu-id="ac9cf-110">Remarks</span></span>

<span data-ttu-id="ac9cf-111">Дополнительные сведения см. в разделе [конструктор C# BigInteger](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) .</span><span class="sxs-lookup"><span data-stu-id="ac9cf-111">See [C# BigInteger constructor](https://docs.microsoft.com/dotnet/api/system.numerics.biginteger.-ctor?view=netframework-4.7.2#System_Numerics_BigInteger__ctor_System_Int64_) for more details.</span></span>