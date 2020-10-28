---
uid: Microsoft.Quantum.Intrinsic.RFrac
title: Операция Рфрак
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: RFrac
qsharp.summary: >-
  Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.

  \begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r".
ms.openlocfilehash: 9fe6aee6c7bb9e52538eae5d2caa2a6025cb85d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732937"
---
# <a name="rfrac-operation"></a><span data-ttu-id="2a9e6-102">Операция Рфрак</span><span class="sxs-lookup"><span data-stu-id="2a9e6-102">RFrac operation</span></span>

<span data-ttu-id="2a9e6-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="2a9e6-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="2a9e6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2a9e6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2a9e6-105">Применяет поворот к заданной оси Паули на угол, заданный как дробь ДЯДИК.</span><span class="sxs-lookup"><span data-stu-id="2a9e6-105">Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="2a9e6-106">\бегин{алигн} R_ {\му} (n, k) \масрел{: =} e ^ {i \пи n \ sigma_ {\му}/2 ^ k}, \енд{алигн}, где $ \му \ин \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="2a9e6-106">\begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

> [!WARNING]
> <span data-ttu-id="2a9e6-107">В этой операции используется **противоположное** соглашение о знаках из @"microsoft.quantum.intrinsic.r" .</span><span class="sxs-lookup"><span data-stu-id="2a9e6-107">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r".</span></span>

```qsharp
operation RFrac (pauli : Pauli, numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="2a9e6-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2a9e6-108">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="2a9e6-109">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="2a9e6-109">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="2a9e6-110">Паули оператор возведен для образования вращения.</span><span class="sxs-lookup"><span data-stu-id="2a9e6-110">Pauli operator to be exponentiated to form the rotation.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="2a9e6-111">Числитель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a9e6-111">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a9e6-112">Числитель в ДЯДИК дробное представление угла, на которое поворачивается кубит.</span><span class="sxs-lookup"><span data-stu-id="2a9e6-112">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="2a9e6-113">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2a9e6-113">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2a9e6-114">Степень 2, указывающая знаменатель угла, на который будет поворачиваться кубит.</span><span class="sxs-lookup"><span data-stu-id="2a9e6-114">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="2a9e6-115">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2a9e6-115">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2a9e6-116">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="2a9e6-116">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2a9e6-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2a9e6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2a9e6-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="2a9e6-118">Remarks</span></span>

<span data-ttu-id="2a9e6-119">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="2a9e6-119">Equivalent to:</span></span>

```qsharp
// PI() is a Q# function that returns an approximation of π.
R(pauli, -PI() * IntAsDouble(numerator) / IntAsDouble(2 ^ (power - 1)), qubit);
```