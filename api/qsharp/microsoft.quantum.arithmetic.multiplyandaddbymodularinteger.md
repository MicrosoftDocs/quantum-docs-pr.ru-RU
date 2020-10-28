---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Операция Мултипляндаддбимодуларинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 3f85f6aaea1d6f8095709c6f387322df7a5e047c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730641"
---
# <a name="multiplyandaddbymodularinteger-operation"></a><span data-ttu-id="9d10a-102">Операция Мултипляндаддбимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="9d10a-102">MultiplyAndAddByModularInteger operation</span></span>

<span data-ttu-id="9d10a-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9d10a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9d10a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9d10a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9d10a-105">Выполняет модульные целочисленные константы умножения и добавления в регистре кубит.</span><span class="sxs-lookup"><span data-stu-id="9d10a-105">Performs a modular multiply-and-add by integer constants on a qubit register.</span></span>

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="9d10a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="9d10a-106">Description</span></span>

<span data-ttu-id="9d10a-107">Реализует карту $ $ \бегин{алигн} \кет{КС} \кет{б} \мапсто \кет{КС} \кет{(b + a \кдот x) \операторнаме{мод} N} \енд{алигн} $ $ для данного модуля $N $, постоянный множитель $a $ и слагаемому $y $.</span><span class="sxs-lookup"><span data-stu-id="9d10a-107">Implements the map $$ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatorname{mod} N} \end{align} $$ for a given modulus $N$, constant multiplier $a$, and summand $y$.</span></span>

## <a name="input"></a><span data-ttu-id="9d10a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9d10a-108">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="9d10a-109">Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9d10a-109">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9d10a-110">Целое число $a $, добавляемое к каждой метке состояния базы данных.</span><span class="sxs-lookup"><span data-stu-id="9d10a-110">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="9d10a-111">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9d10a-111">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9d10a-112">Модуль $N $, для которого выполняется сложение и умножение, относительно.</span><span class="sxs-lookup"><span data-stu-id="9d10a-112">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="9d10a-113">множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9d10a-113">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9d10a-114">Регистр такта, представляющий целое число без знака, значение которого добавляется к каждой метке состояния базы `summand` .</span><span class="sxs-lookup"><span data-stu-id="9d10a-114">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="summand--littleendian"></a><span data-ttu-id="9d10a-115">слагаемому: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9d10a-115">summand : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9d10a-116">Регистр такта, представляющий целое число без знака, которое будет использоваться в качестве целевого объекта для данной операции.</span><span class="sxs-lookup"><span data-stu-id="9d10a-116">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9d10a-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d10a-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9d10a-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="9d10a-118">Remarks</span></span>

- <span data-ttu-id="9d10a-119">Схема канала и описание см. на рис. 6 на [стр. 7 из арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span><span class="sxs-lookup"><span data-stu-id="9d10a-119">For the circuit diagram and explanation see Figure 6 on [Page 7 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)</span></span>
- <span data-ttu-id="9d10a-120">Эта операция соответствует КМУЛТ (a) MOD (N) в [арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="9d10a-120">This operation corresponds to CMULT(a)MOD(N) in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>

## <a name="see-also"></a><span data-ttu-id="9d10a-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="9d10a-121">See Also</span></span>

- [<span data-ttu-id="9d10a-122">Microsoft. тактов. арифметик. Мултипляндаддфасебимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="9d10a-122">Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)