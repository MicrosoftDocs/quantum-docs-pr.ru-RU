---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Операция Меасуреинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: e3ff06e5cbb2ef8a63e4ad12308b382347c90fc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222649"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="8daf5-102">Операция Меасуреинтежер</span><span class="sxs-lookup"><span data-stu-id="8daf5-102">MeasureInteger operation</span></span>

<span data-ttu-id="8daf5-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8daf5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8daf5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8daf5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8daf5-105">Измеряет содержимое регистра такта и преобразует его в целое число.</span><span class="sxs-lookup"><span data-stu-id="8daf5-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="8daf5-106">Измерение выполняется в соответствии со стандартной вычислительной единицей, т. е. еиженбасис `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="8daf5-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="8daf5-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8daf5-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="8daf5-108">Целевой объект: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8daf5-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8daf5-109">Регистр такта в кодировке с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="8daf5-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="8daf5-110">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8daf5-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8daf5-111">Целое число без знака, содержащее измеряемое значение `target` .</span><span class="sxs-lookup"><span data-stu-id="8daf5-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8daf5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8daf5-112">Remarks</span></span>

<span data-ttu-id="8daf5-113">Эта операция сбрасывает регистр входных данных в состояние $ \ket{00\cdots 0} $, подходящее для освобождения на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="8daf5-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="8daf5-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="8daf5-114">See Also</span></span>

- [<span data-ttu-id="8daf5-115">Microsoft. тактов. Canon. Меасуреинтежербе</span><span class="sxs-lookup"><span data-stu-id="8daf5-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)