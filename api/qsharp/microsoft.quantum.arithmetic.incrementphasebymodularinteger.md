---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Операция Инкрементфасебимодуларинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 52309c056a3eae25ffdfbfa848f94bf744c71132
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731473"
---
# <a name="incrementphasebymodularinteger-operation"></a><span data-ttu-id="ad8d6-102">Операция Инкрементфасебимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="ad8d6-102">IncrementPhaseByModularInteger operation</span></span>

<span data-ttu-id="ad8d6-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ad8d6-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ad8d6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ad8d6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ad8d6-105">Выполняет модульное увеличение регистра кубит с помощью целочисленной константы.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-105">Performs a modular increment of a qubit register by an integer constant.</span></span>

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="ad8d6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="ad8d6-106">Description</span></span>

<span data-ttu-id="ad8d6-107">Отметим, `increment` что $a $, `modulus` $N $ и целое число, закодированные `target` $y $.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-107">Let us denote `increment` by $a$, `modulus` by $N$ and integer encoded in `target` by $y$.</span></span>
<span data-ttu-id="ad8d6-108">Затем операция выполняет следующее преобразование: \бегин{алигн} \кет{и} \мапсто \кет{(y + a) \операторнаме{мод} N} \енд{алигн} целые числа в Кфт кодируются в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-108">Then the operation performs the following transformation: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} Integers are encoded in little-endian format in QFT basis.</span></span>

## <a name="input"></a><span data-ttu-id="ad8d6-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ad8d6-109">Input</span></span>

### <a name="increment--int"></a><span data-ttu-id="ad8d6-110">приращение: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ad8d6-110">increment : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ad8d6-111">Целочисленное приращение $a $, добавляемое в $y $.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-111">Integer increment $a$ to be added to $y$.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="ad8d6-112">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ad8d6-112">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ad8d6-113">Integer $N $, МОДС $y + a $.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-113">Integer $N$ that mods $y + a$.</span></span>


### <a name="target--phaselittleendian"></a><span data-ttu-id="ad8d6-114">Целевой объект: [фаселиттлиндиан](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ad8d6-114">target : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="ad8d6-115">Целое число $y $ в формате с прямым порядком байтов в кодировке, который `increment` $a $ добавляется в.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-115">Integer $y$ in phase-encoded little-endian format that `increment` $a$ is added to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ad8d6-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ad8d6-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ad8d6-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="ad8d6-117">Remarks</span></span>

<span data-ttu-id="ad8d6-118">Предполагается, что `target` имеет наивысший бит, равный 0.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-118">Assumes that `target` has the highest bit set to 0.</span></span>
<span data-ttu-id="ad8d6-119">Также предполагается, что значение целевого объекта меньше $N $.</span><span class="sxs-lookup"><span data-stu-id="ad8d6-119">Also assumes that the value of target is less than $N$.</span></span>

<span data-ttu-id="ad8d6-120">Схема канала и описание см. на рис. 5 на [стр. 5 из арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span><span class="sxs-lookup"><span data-stu-id="ad8d6-120">For the circuit diagram and explanation see Figure 5 on [Page 5 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).</span></span>

## <a name="see-also"></a><span data-ttu-id="ad8d6-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="ad8d6-121">See Also</span></span>

- [<span data-ttu-id="ad8d6-122">Microsoft. тактов. арифметик. Инкрементбимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="ad8d6-122">Microsoft.Quantum.Arithmetic.IncrementByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)