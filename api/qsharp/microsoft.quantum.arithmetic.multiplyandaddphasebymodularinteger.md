---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Операция Мултипляндаддфасебимодуларинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: be7df50f040697329c2fe8bbc319c8cebb8b2687
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730640"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="0d164-102">Операция Мултипляндаддфасебимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="0d164-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="0d164-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0d164-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0d164-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0d164-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0d164-105">То же, что и Мултипляндаддбимодуларинтежер, но предполагает, что слагаемому кодирует целые числа в Кфт.</span><span class="sxs-lookup"><span data-stu-id="0d164-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="0d164-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0d164-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="0d164-107">Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0d164-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0d164-108">Целое число $a $, добавляемое к каждой метке состояния базы данных.</span><span class="sxs-lookup"><span data-stu-id="0d164-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="0d164-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0d164-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0d164-110">Модуль $N $, для которого выполняется сложение и умножение, относительно.</span><span class="sxs-lookup"><span data-stu-id="0d164-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="0d164-111">множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0d164-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0d164-112">Регистр такта, представляющий целое число без знака, значение которого добавляется к каждой метке состояния базы `summand` .</span><span class="sxs-lookup"><span data-stu-id="0d164-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="0d164-113">Фасесумманд: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0d164-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="0d164-114">Регистр такта, представляющий целое число без знака, которое будет использоваться в качестве целевого объекта для данной операции.</span><span class="sxs-lookup"><span data-stu-id="0d164-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0d164-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0d164-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="0d164-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="0d164-116">Remarks</span></span>

<span data-ttu-id="0d164-117">Предполагается, что `phaseSummand` имеет наивысший бит, равный 0.</span><span class="sxs-lookup"><span data-stu-id="0d164-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="0d164-118">Также предполагается, что значение `phaseSummand` меньше $N $.</span><span class="sxs-lookup"><span data-stu-id="0d164-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d164-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="0d164-119">See Also</span></span>

- [<span data-ttu-id="0d164-120">Microsoft. тактов. арифметик. Мултипляндаддбимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="0d164-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)