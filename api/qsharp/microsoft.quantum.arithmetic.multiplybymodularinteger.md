---
uid: Microsoft.Quantum.Arithmetic.MultiplyByModularInteger
title: Операция Мултиплибимодуларинтежер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyByModularInteger
qsharp.summary: Performs modular multiplication by an integer constant on a qubit register.
ms.openlocfilehash: 6deced7862ab4cb74315219eaaab97380cdf0f92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730632"
---
# <a name="multiplybymodularinteger-operation"></a><span data-ttu-id="4febf-102">Операция Мултиплибимодуларинтежер</span><span class="sxs-lookup"><span data-stu-id="4febf-102">MultiplyByModularInteger operation</span></span>

<span data-ttu-id="4febf-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="4febf-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="4febf-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4febf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4febf-105">Выполняет модульное умножение с помощью целочисленной константы в регистре кубит.</span><span class="sxs-lookup"><span data-stu-id="4febf-105">Performs modular multiplication by an integer constant on a qubit register.</span></span>

```qsharp
operation MultiplyByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="4febf-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4febf-106">Description</span></span>

<span data-ttu-id="4febf-107">Отметим `modulus` , что $N $ и `constMultiplier` $a $.</span><span class="sxs-lookup"><span data-stu-id="4febf-107">Let us denote `modulus` by $N$ and `constMultiplier` by $a$.</span></span>
<span data-ttu-id="4febf-108">Затем эта операция реализует единую операцию, определенную следующей картой на основе вычислений: $ $ \бегин{алигн} \кет{и} \мапсто \кет{(a \кдот y) \операторнаме{мод} N} \енд{алигн} $ $ для всех $y $ между $0 $ и $N-$1.</span><span class="sxs-lookup"><span data-stu-id="4febf-108">Then this operation implements a unitary operation defined by the following map on the computational basis: $$ \begin{align} \ket{y} \mapsto \ket{(a \cdot y) \operatorname{mod} N} \end{align} $$ for all $y$ between $0$ and $N - 1$.</span></span>

## <a name="input"></a><span data-ttu-id="4febf-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4febf-109">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="4febf-110">Констмултиплиер: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4febf-110">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4febf-111">Константа, на которую умножается множитель.</span><span class="sxs-lookup"><span data-stu-id="4febf-111">Constant by which multiplier is being multiplied.</span></span> <span data-ttu-id="4febf-112">Должно быть состоять в виде модуля.</span><span class="sxs-lookup"><span data-stu-id="4febf-112">Must be co-prime to modulus.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="4febf-113">модуль: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4febf-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4febf-114">Операция умножения выполняется по модулю `modulus` .</span><span class="sxs-lookup"><span data-stu-id="4febf-114">The multiplication operation is performed modulo `modulus`.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="4febf-115">множитель: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4febf-115">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="4febf-116">Число, умноженное на константу.</span><span class="sxs-lookup"><span data-stu-id="4febf-116">The number being multiplied by a constant.</span></span>
<span data-ttu-id="4febf-117">Это массив из Кубитс кодирования целого числа в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="4febf-117">This is an array of qubits encoding an integer in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4febf-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4febf-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4febf-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="4febf-119">Remarks</span></span>

- <span data-ttu-id="4febf-120">Схема канала и описание см. на рис. 7 на [стр. 8 из арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span><span class="sxs-lookup"><span data-stu-id="4febf-120">For the circuit diagram and explanation see Figure 7 on [Page 8 of arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)</span></span>
- <span data-ttu-id="4febf-121">Эта операция соответствует U ₐ в [арксив: Куант-pH/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span><span class="sxs-lookup"><span data-stu-id="4febf-121">This operation corresponds to Uₐ in [arXiv:quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)</span></span>