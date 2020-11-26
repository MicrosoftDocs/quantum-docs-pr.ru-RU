---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Операция Мултипляндаддфасебимодуларинтежер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: 1ca20b525d2a76e554d5a2e8d4f40060b5ef51cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223873"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="7b426-102">Операция Мултипляндаддфасебимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="7b426-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="7b426-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7b426-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7b426-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7b426-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7b426-105">То же, что и Мултипляндаддбимодуларинтежер, но предполагает, что слагаемому кодирует целые числа в Кфт.</span><span class="sxs-lookup"><span data-stu-id="7b426-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7b426-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7b426-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="7b426-107">Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7b426-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7b426-108">Целое число $a $, добавляемое к каждой метке состояния базы данных.</span><span class="sxs-lookup"><span data-stu-id="7b426-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="7b426-109">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7b426-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7b426-110">Модуль $N $, для которого выполняется сложение и умножение, относительно.</span><span class="sxs-lookup"><span data-stu-id="7b426-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="7b426-111">множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7b426-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7b426-112">Регистр такта, представляющий целое число без знака, значение которого добавляется к каждой метке состояния базы `summand` .</span><span class="sxs-lookup"><span data-stu-id="7b426-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="7b426-113">Фасесумманд: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7b426-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="7b426-114">Регистр такта, представляющий целое число без знака, которое будет использоваться в качестве целевого объекта для данной операции.</span><span class="sxs-lookup"><span data-stu-id="7b426-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7b426-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7b426-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7b426-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b426-116">Remarks</span></span>

<span data-ttu-id="7b426-117">Предполагается, что `phaseSummand` имеет наивысший бит, равный 0.</span><span class="sxs-lookup"><span data-stu-id="7b426-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="7b426-118">Также предполагается, что значение `phaseSummand` меньше $N $.</span><span class="sxs-lookup"><span data-stu-id="7b426-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b426-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="7b426-119">See Also</span></span>

- [<span data-ttu-id="7b426-120">Microsoft. тактов. арифметик. Мултипляндаддбимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="7b426-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)