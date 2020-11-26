---
uid: Microsoft.Quantum.Intrinsic.RFrac
title: Операция Рфрак
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: RFrac
qsharp.summary: >-
  Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.

  \begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r".
ms.openlocfilehash: bd182ea50d747e07bb0f8051c5dbc128b7ff7674
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198645"
---
# <a name="rfrac-operation"></a><span data-ttu-id="660b1-102">Операция Рфрак</span><span class="sxs-lookup"><span data-stu-id="660b1-102">RFrac operation</span></span>

<span data-ttu-id="660b1-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="660b1-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="660b1-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="660b1-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="660b1-105">Применяет поворот к заданной оси Паули на угол, заданный как дробь ДЯДИК.</span><span class="sxs-lookup"><span data-stu-id="660b1-105">Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="660b1-106">\бегин{алигн} R_ {\му} (n, k) \масрел{: =} e ^ {i \пи n \ sigma_ {\му}/2 ^ k}, \енд{алигн}, где $ \му \ин \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="660b1-106">\begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

> [!WARNING]
> <span data-ttu-id="660b1-107">В этой операции используется **противоположное** соглашение о знаках из @"microsoft.quantum.intrinsic.r" .</span><span class="sxs-lookup"><span data-stu-id="660b1-107">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r".</span></span>

```qsharp
operation RFrac (pauli : Pauli, numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="660b1-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="660b1-108">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="660b1-109">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="660b1-109">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="660b1-110">Паули оператор возведен для образования вращения.</span><span class="sxs-lookup"><span data-stu-id="660b1-110">Pauli operator to be exponentiated to form the rotation.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="660b1-111">Числитель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="660b1-111">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="660b1-112">Числитель в ДЯДИК дробное представление угла, на которое поворачивается кубит.</span><span class="sxs-lookup"><span data-stu-id="660b1-112">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="660b1-113">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="660b1-113">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="660b1-114">Степень 2, указывающая знаменатель угла, на который будет поворачиваться кубит.</span><span class="sxs-lookup"><span data-stu-id="660b1-114">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="660b1-115">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="660b1-115">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="660b1-116">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="660b1-116">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="660b1-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="660b1-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="660b1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="660b1-118">Remarks</span></span>

<span data-ttu-id="660b1-119">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="660b1-119">Equivalent to:</span></span>

```qsharp
// PI() is a Q# function that returns an approximation of π.
R(pauli, -PI() * IntAsDouble(numerator) / IntAsDouble(2 ^ (power - 1)), qubit);
```