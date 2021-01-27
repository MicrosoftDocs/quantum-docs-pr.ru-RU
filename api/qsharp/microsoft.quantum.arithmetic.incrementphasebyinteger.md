---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Операция Инкрементфасебинтежер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: cc7922b2940cb979394958d5eb4e9933144eb062
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843143"
---
# <a name="incrementphasebyinteger-operation"></a><span data-ttu-id="3f67c-102">Операция Инкрементфасебинтежер</span><span class="sxs-lookup"><span data-stu-id="3f67c-102">IncrementPhaseByInteger operation</span></span>

<span data-ttu-id="3f67c-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3f67c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3f67c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f67c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f67c-105">Увеличивает значение регистра неподписанного такта на классическое целое число с использованием ротаций фазы.</span><span class="sxs-lookup"><span data-stu-id="3f67c-105">Increments an unsigned quantum register by a classical integer, using phase rotations.</span></span>

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="3f67c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3f67c-106">Description</span></span>

<span data-ttu-id="3f67c-107">Предположим, что `target` кодирует целое число без знака $x $ в кодировке с прямым порядком байтов и `increment` равно $a $.</span><span class="sxs-lookup"><span data-stu-id="3f67c-107">Suppose that `target` encodes an unsigned integer $x$ in a little-endian encoding and that `increment` is equal to $a$.</span></span>
<span data-ttu-id="3f67c-108">Затем эта операция реализует единую $ \кет{КС} \мапсто \кет{КС + a} $, где сложение выполняется по модулю $2 ^ n $, где $n = \Тексттт{ленгс (Target!)} $.</span><span class="sxs-lookup"><span data-stu-id="3f67c-108">Then, this operation implements the unitary $\ket{x} \mapsto \ket{x + a}$, where the addition is performed modulo $2^n$, where $n = \texttt{Length(target!)}$.</span></span>

## <a name="input"></a><span data-ttu-id="3f67c-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3f67c-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="3f67c-110">приращение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3f67c-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3f67c-111">Целое число, на которое `target` увеличивается значение.</span><span class="sxs-lookup"><span data-stu-id="3f67c-111">The integer by which the `target` is incremented by.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="3f67c-112">Целевой объект: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3f67c-112">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="3f67c-113">Тактовый регистр кодирует целое число без знака, используя обратную кодировку с прямым порядком байтов в двойном (Кфт) уровне.</span><span class="sxs-lookup"><span data-stu-id="3f67c-113">A quantum register encoding an unsigned integer using little-endian encoding in the dual (QFT) basis.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3f67c-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3f67c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3f67c-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="3f67c-115">Remarks</span></span>

<span data-ttu-id="3f67c-116">Обратите внимание, что мы упростили канал, так как инкремент является классической константой, а не тактовой регистром.</span><span class="sxs-lookup"><span data-stu-id="3f67c-116">Note that we have simplified the circuit because the increment is a classical constant, not a quantum register.</span></span>

<span data-ttu-id="3f67c-117">См. рисунок на [ стр. 6 из арксив: Куант-pH/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) для схемы канала и объяснения.</span><span class="sxs-lookup"><span data-stu-id="3f67c-117">See the figure on [ Page 6 of arXiv:quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) for the circuit diagram and explanation.</span></span>

## <a name="references"></a><span data-ttu-id="3f67c-118">Ссылки</span><span class="sxs-lookup"><span data-stu-id="3f67c-118">References</span></span>

- [<span data-ttu-id="3f67c-119">*Томас G. Драпер*, арксив: Куант-pH/0008033</span><span class="sxs-lookup"><span data-stu-id="3f67c-119"> *Thomas G. Draper*, arXiv:quant-ph/0008033</span></span>](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a><span data-ttu-id="3f67c-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="3f67c-120">See Also</span></span>

- [<span data-ttu-id="3f67c-121">Microsoft. тактов. арифметик. Инкрементбинтежер</span><span class="sxs-lookup"><span data-stu-id="3f67c-121">Microsoft.Quantum.Arithmetic.IncrementByInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)