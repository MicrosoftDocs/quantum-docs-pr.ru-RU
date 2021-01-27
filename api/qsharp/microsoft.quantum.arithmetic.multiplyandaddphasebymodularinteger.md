---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Операция Мултипляндаддфасебимодуларинтежер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: b1214acc2cafc3fede9fcb6663a435c0b1d2cf4a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843062"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="9c7a4-102">Операция Мултипляндаддфасебимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="9c7a4-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="9c7a4-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9c7a4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9c7a4-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9c7a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9c7a4-105">То же, что и Мултипляндаддбимодуларинтежер, но предполагает, что слагаемому кодирует целые числа в Кфт.</span><span class="sxs-lookup"><span data-stu-id="9c7a4-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9c7a4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9c7a4-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="9c7a4-107">Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9c7a4-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9c7a4-108">Целое число $a $, добавляемое к каждой метке состояния базы данных.</span><span class="sxs-lookup"><span data-stu-id="9c7a4-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="9c7a4-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9c7a4-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9c7a4-110">Модуль $N $, для которого выполняется сложение и умножение, относительно.</span><span class="sxs-lookup"><span data-stu-id="9c7a4-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="9c7a4-111">множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9c7a4-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9c7a4-112">Регистр такта, представляющий целое число без знака, значение которого добавляется к каждой метке состояния базы `summand` .</span><span class="sxs-lookup"><span data-stu-id="9c7a4-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="9c7a4-113">Фасесумманд: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9c7a4-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="9c7a4-114">Регистр такта, представляющий целое число без знака, которое будет использоваться в качестве целевого объекта для данной операции.</span><span class="sxs-lookup"><span data-stu-id="9c7a4-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9c7a4-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9c7a4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9c7a4-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="9c7a4-116">Remarks</span></span>

<span data-ttu-id="9c7a4-117">Предполагается, что `phaseSummand` имеет наивысший бит, равный 0.</span><span class="sxs-lookup"><span data-stu-id="9c7a4-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="9c7a4-118">Также предполагается, что значение `phaseSummand` меньше $N $.</span><span class="sxs-lookup"><span data-stu-id="9c7a4-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c7a4-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="9c7a4-119">See Also</span></span>

- [<span data-ttu-id="9c7a4-120">Microsoft. тактов. арифметик. Мултипляндаддбимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="9c7a4-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)