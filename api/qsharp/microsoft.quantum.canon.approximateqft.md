---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Операция Аппроксиматекфт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: ffa3a3737a43fbe6acc57700ae122a13586482e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716770"
---
# <a name="approximateqft-operation"></a><span data-ttu-id="5d78d-102">Операция Аппроксиматекфт</span><span class="sxs-lookup"><span data-stu-id="5d78d-102">ApproximateQFT operation</span></span>

<span data-ttu-id="5d78d-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5d78d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5d78d-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5d78d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5d78d-105">Примените примерное преобразование Фурье (АКФТ) к тактовому регистру.</span><span class="sxs-lookup"><span data-stu-id="5d78d-105">Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.</span></span>

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="5d78d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5d78d-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="5d78d-107">ответ. [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5d78d-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5d78d-108">параметр аппроксимации, определяющий уровень управляемых поворотов Z, происходящих в цепи Кфт.</span><span class="sxs-lookup"><span data-stu-id="5d78d-108">approximation parameter which determines at which level the controlled Z-rotations that occur in the QFT circuit are pruned.</span></span>

<span data-ttu-id="5d78d-109">Параметр аппроксимации определяет уровень очистки поворотов по оси Z, т. е. ∈ {0.. n} и все повороты Z 2π/2000, где k>a удаляется из канала Кфт.</span><span class="sxs-lookup"><span data-stu-id="5d78d-109">The approximation parameter a determines the pruning level of the Z-rotations, i.e., a ∈ {0..n} and all Z-rotations 2π/2ᵏ where k>a are removed from the QFT circuit.</span></span> <span data-ttu-id="5d78d-110">Известно, что для k >= log ₂ (n) + log ₂ (1/ε) + 3 можно привязать | | КФТ-АКФТ | |<ε.</span><span class="sxs-lookup"><span data-stu-id="5d78d-110">It is known that for k >= log₂(n)+log₂(1/ε)+3 one can bound ||QFT-AQFT||<ε.</span></span>


### <a name="qs--bigendian"></a><span data-ttu-id="5d78d-111">QS: [байтов](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="5d78d-111">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="5d78d-112">Регистр такта в n Кубитс, к которому применяется приблизительное преобразование тактов в виде Фурье.</span><span class="sxs-lookup"><span data-stu-id="5d78d-112">quantum register of n qubits to which the Approximate Quantum Fourier Transform is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5d78d-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5d78d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5d78d-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="5d78d-114">Remarks</span></span>

<span data-ttu-id="5d78d-115">АКФТ требует использования шлюзов Z в форме 2π/2000 и Хадамард Gates.</span><span class="sxs-lookup"><span data-stu-id="5d78d-115">AQFT requires Z-rotation gates of the form 2π/2ᵏ and Hadamard gates.</span></span>

<span data-ttu-id="5d78d-116">Предполагается, что входные и выходные данные кодируются в кодировке с обратным порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="5d78d-116">The input and output are assumed to be encoded in big endian encoding.</span></span>

## <a name="references"></a><span data-ttu-id="5d78d-117">Ссылки</span><span class="sxs-lookup"><span data-stu-id="5d78d-117">References</span></span>

- [<span data-ttu-id="5d78d-118">*M. роеттелер, TH. Бет* , прим. \ ENG. коммун. Учет. 19 (3): 177-193 (2008)</span><span class="sxs-lookup"><span data-stu-id="5d78d-118"> *M. Roetteler, Th. Beth* , Appl. Algebra Eng. Commun. Comput. 19(3): 177-193 (2008) </span></span>](http://doi.org/10.1007/s00200-008-0072-2)
- [<span data-ttu-id="5d78d-119">*D. копперсмис* арксив: Куант-pH/0201067v1</span><span class="sxs-lookup"><span data-stu-id="5d78d-119"> *D. Coppersmith* arXiv:quant-ph/0201067v1 </span></span>](https://arxiv.org/abs/quant-ph/0201067)