---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: Операция Мултиплексоператионсфромженератор
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 2fde0bf391568f39128e6dca4b535aa6b78407c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715803"
---
# <a name="multiplexoperationsfromgenerator-operation"></a><span data-ttu-id="e449c-102">Операция Мултиплексоператионсфромженератор</span><span class="sxs-lookup"><span data-stu-id="e449c-102">MultiplexOperationsFromGenerator operation</span></span>

<span data-ttu-id="e449c-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e449c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e449c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e449c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e449c-105">Применяет операцию, управляемую умножением, $U $, которая применяет единое $V _j $ при управлении с помощью n-кубит числового состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="e449c-105">Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="e449c-106">$U = \сум ^ {N-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.</span><span class="sxs-lookup"><span data-stu-id="e449c-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="e449c-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e449c-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit-adj--ctl"></a><span data-ttu-id="e449c-108">Унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL)</span><span class="sxs-lookup"><span data-stu-id="e449c-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

<span data-ttu-id="e449c-109">Кортеж, в котором первый элемент `Int` — это число унитариес $N $, а второй элемент — это `(Int -> ('T => () is Adj + Ctl))` функция, принимающая целое число $j $ в $ [0, N-1] $ и выводит единую операцию $V _j $.</span><span class="sxs-lookup"><span data-stu-id="e449c-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="e449c-110">Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e449c-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e449c-111">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="e449c-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="e449c-112">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="e449c-112">target : 'T</span></span>

<span data-ttu-id="e449c-113">Универсальный кубит регистр, который $V _j $.</span><span class="sxs-lookup"><span data-stu-id="e449c-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e449c-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e449c-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e449c-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="e449c-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e449c-116">Е</span><span class="sxs-lookup"><span data-stu-id="e449c-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="e449c-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="e449c-117">Remarks</span></span>

<span data-ttu-id="e449c-118">`coefficients` будут заполнены элементами Identity, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="e449c-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="e449c-119">В этой реализации используется $n-$1 вспомогательная Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e449c-119">This implementation uses $n-1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="e449c-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="e449c-120">References</span></span>

- [<span data-ttu-id="e449c-121">*Эндрю M. дочерние, Дмитрий Маслов, Вьетнам юнсеонг, Нил J. Росс (, Юань SU* , арксив: 1711.10980</span><span class="sxs-lookup"><span data-stu-id="e449c-121"> *Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su* , arXiv:1711.10980</span></span>](https://arxiv.org/abs/1711.10980)