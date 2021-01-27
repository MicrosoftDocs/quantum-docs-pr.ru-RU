---
uid: Microsoft.Quantum.Canon.MultiplexOperationsBruteForceFromGenerator
title: Операция Мултиплексоператионсбрутефорцефромженератор
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsBruteForceFromGenerator
qsharp.summary: >-
  Applies multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 395102c7ffffa81d1a9b6cbf29c9cc22fae6057e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852518"
---
# <a name="multiplexoperationsbruteforcefromgenerator-operation"></a><span data-ttu-id="77bc5-102">Операция Мултиплексоператионсбрутефорцефромженератор</span><span class="sxs-lookup"><span data-stu-id="77bc5-102">MultiplexOperationsBruteForceFromGenerator operation</span></span>

<span data-ttu-id="77bc5-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="77bc5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="77bc5-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77bc5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77bc5-105">Применяет операцию с множественным контролем, $U $, которая применяет единое $V _j $ при управлении с помощью n-кубит числового состояния $ \кет{ж} $.</span><span class="sxs-lookup"><span data-stu-id="77bc5-105">Applies multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="77bc5-106">$U = \сум ^ {N-1} _ {j = 0} \кет{ж}\бра{ж}\отимес V_j $.</span><span class="sxs-lookup"><span data-stu-id="77bc5-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsBruteForceFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="77bc5-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="77bc5-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit--is-adj--ctl"></a><span data-ttu-id="77bc5-108">Унитариженератор: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [единицы измерения](xref:microsoft.quantum.lang-ref.unit)  "года + CTL")</span><span class="sxs-lookup"><span data-stu-id="77bc5-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

<span data-ttu-id="77bc5-109">Кортеж, в котором первый элемент `Int` — это число унитариес $N $, а второй элемент — это `(Int -> ('T => () is Adj + Ctl))` функция, принимающая целое число $j $ в $ [0, N-1] $ и выводит единую операцию $V _j $.</span><span class="sxs-lookup"><span data-stu-id="77bc5-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="77bc5-110">Индекс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="77bc5-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="77bc5-111">$n $-кубит управления регистром, который кодирует числовые состояния $ \кет{ж} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="77bc5-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="77bc5-112">Целевой объект: 'T</span><span class="sxs-lookup"><span data-stu-id="77bc5-112">target : 'T</span></span>

<span data-ttu-id="77bc5-113">Универсальный кубит регистр, который $V _j $.</span><span class="sxs-lookup"><span data-stu-id="77bc5-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77bc5-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77bc5-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="77bc5-115">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="77bc5-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="77bc5-116">Е</span><span class="sxs-lookup"><span data-stu-id="77bc5-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="77bc5-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="77bc5-117">Remarks</span></span>

<span data-ttu-id="77bc5-118">`coefficients` будут заполнены элементами Identity, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="77bc5-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="77bc5-119">Эта версия реализована непосредственно с помощью циклов в единых операторах, управляемых n.</span><span class="sxs-lookup"><span data-stu-id="77bc5-119">This version is implemented directly by looping through n-controlled unitary operators.</span></span>