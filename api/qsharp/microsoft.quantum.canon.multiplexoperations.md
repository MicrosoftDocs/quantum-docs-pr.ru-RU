---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Операция Мултиплексоператионс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 267c9c2858090ebe024fd387938e8bd2f8c76867
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715832"
---
# <a name="multiplexoperations-operation"></a><span data-ttu-id="336d8-102">Операция Мултиплексоператионс</span><span class="sxs-lookup"><span data-stu-id="336d8-102">MultiplexOperations operation</span></span>

<span data-ttu-id="336d8-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="336d8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="336d8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="336d8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="336d8-105">Применяет массив операций, управляемых массивом числовых состояний.</span><span class="sxs-lookup"><span data-stu-id="336d8-105">Applies an array of operations controlled by an array of number states.</span></span>

<span data-ttu-id="336d8-106">Это значит, что применяет операцию с множественным контролем, $U $, которая применяет единое $V _j $ при управлении с $n $-кубит номер состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="336d8-106">That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="336d8-107">$U = \сум ^ {2 ^ n-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.</span><span class="sxs-lookup"><span data-stu-id="336d8-107">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="336d8-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="336d8-108">Input</span></span>

### <a name="unitaries--t--unit-adj--ctl"></a><span data-ttu-id="336d8-109">унитариес: 'T => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL []</span><span class="sxs-lookup"><span data-stu-id="336d8-109">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="336d8-110">Массив операций до $2 ^ n $ от единой операции.</span><span class="sxs-lookup"><span data-stu-id="336d8-110">Array of up to $2^n$ unitary operations.</span></span> <span data-ttu-id="336d8-111">Операция $j $ TH индексируется по числу состояния $ \кет{ж} $, закодированному в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="336d8-111">The $j$th operation is indexed by the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="336d8-112">Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="336d8-112">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="336d8-113">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="336d8-113">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="336d8-114">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="336d8-114">target : 'T</span></span>

<span data-ttu-id="336d8-115">Универсальный кубит регистр, который $V _j $.</span><span class="sxs-lookup"><span data-stu-id="336d8-115">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="336d8-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="336d8-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="336d8-117">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="336d8-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="336d8-118">Е</span><span class="sxs-lookup"><span data-stu-id="336d8-118">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="336d8-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="336d8-119">Remarks</span></span>

<span data-ttu-id="336d8-120">`coefficients` будут заполнены элементами Identity, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="336d8-120">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="336d8-121">В этой реализации используется $n-$1 вспомогательная Кубитс.</span><span class="sxs-lookup"><span data-stu-id="336d8-121">This implementation uses $n - 1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="336d8-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="336d8-122">References</span></span>

- <span data-ttu-id="336d8-123">К первому моделированию такта с увеличением такта, Дмитрий Маслов, Вьетнам Юнсеонг, Нил J. Росс (, Юань SU https://arxiv.org/abs/1711.10980</span><span class="sxs-lookup"><span data-stu-id="336d8-123">Toward the first quantum simulation with quantum speedup Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su https://arxiv.org/abs/1711.10980</span></span>