---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: Операция Мултиплексоператионсфромженератор
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 9fbbd9268d4a6b9f3d5fd203969f4bbeebe81b68
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205955"
---
# <a name="multiplexoperationsfromgenerator-operation"></a><span data-ttu-id="c63ef-102">Операция Мултиплексоператионсфромженератор</span><span class="sxs-lookup"><span data-stu-id="c63ef-102">MultiplexOperationsFromGenerator operation</span></span>

<span data-ttu-id="c63ef-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c63ef-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c63ef-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c63ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c63ef-105">Применяет операцию, управляемую умножением, $U $, которая применяет единое $V _j $ при управлении с помощью n-кубит числового состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="c63ef-105">Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="c63ef-106">$U = \сум ^ {N-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.</span><span class="sxs-lookup"><span data-stu-id="c63ef-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c63ef-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c63ef-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit--is-adj--ctl"></a><span data-ttu-id="c63ef-108">Унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  "года + CTL")</span><span class="sxs-lookup"><span data-stu-id="c63ef-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

<span data-ttu-id="c63ef-109">Кортеж, в котором первый элемент `Int` — это число унитариес $N $, а второй элемент — это `(Int -> ('T => () is Adj + Ctl))` функция, принимающая целое число $j $ в $ [0, N-1] $ и выводит единую операцию $V _j $.</span><span class="sxs-lookup"><span data-stu-id="c63ef-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="c63ef-110">Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c63ef-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c63ef-111">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="c63ef-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="c63ef-112">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="c63ef-112">target : 'T</span></span>

<span data-ttu-id="c63ef-113">Универсальный кубит регистр, который $V _j $.</span><span class="sxs-lookup"><span data-stu-id="c63ef-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c63ef-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c63ef-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c63ef-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="c63ef-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c63ef-116">Е</span><span class="sxs-lookup"><span data-stu-id="c63ef-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="c63ef-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c63ef-117">Remarks</span></span>

<span data-ttu-id="c63ef-118">`coefficients` будут заполнены элементами Identity, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="c63ef-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="c63ef-119">В этой реализации используется $n-$1 вспомогательная Кубитс.</span><span class="sxs-lookup"><span data-stu-id="c63ef-119">This implementation uses $n-1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="c63ef-120">Ссылки</span><span class="sxs-lookup"><span data-stu-id="c63ef-120">References</span></span>

- [<span data-ttu-id="c63ef-121">*Эндрю M. дочерние, Дмитрий Маслов, Вьетнам юнсеонг, Нил J. Росс (, Юань SU*, арксив: 1711.10980</span><span class="sxs-lookup"><span data-stu-id="c63ef-121"> *Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su*, arXiv:1711.10980</span></span>](https://arxiv.org/abs/1711.10980)