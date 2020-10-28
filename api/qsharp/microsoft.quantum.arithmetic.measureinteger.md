---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Операция Меасуреинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 7cd2d93332eb168c7c2be92a3b910033ca8c10ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731416"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="40e08-102">Операция Меасуреинтежер</span><span class="sxs-lookup"><span data-stu-id="40e08-102">MeasureInteger operation</span></span>

<span data-ttu-id="40e08-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="40e08-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="40e08-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40e08-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40e08-105">Измеряет содержимое регистра такта и преобразует его в целое число.</span><span class="sxs-lookup"><span data-stu-id="40e08-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="40e08-106">Измерение выполняется в соответствии со стандартной вычислительной единицей, т. е. еиженбасис `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="40e08-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="40e08-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="40e08-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="40e08-108">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="40e08-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="40e08-109">Регистр такта в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="40e08-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="40e08-110">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40e08-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="40e08-111">Целое число без знака, содержащее измеряемое значение `target` .</span><span class="sxs-lookup"><span data-stu-id="40e08-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="40e08-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="40e08-112">Remarks</span></span>

<span data-ttu-id="40e08-113">Эта операция сбрасывает регистр входных данных в состояние $ \ket{00\cdots 0} $, подходящее для освобождения на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="40e08-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="40e08-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="40e08-114">See Also</span></span>

- [<span data-ttu-id="40e08-115">Microsoft. тактов. Canon. Меасуреинтежербе</span><span class="sxs-lookup"><span data-stu-id="40e08-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)