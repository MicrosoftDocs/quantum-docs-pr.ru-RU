---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: Операция R1Frac
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: bfa6cd60eebd05feec8cfa2bf71e09dc0d02843a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731369"
---
# <a name="r1frac-operation"></a><span data-ttu-id="93a63-102">Операция R1Frac</span><span class="sxs-lookup"><span data-stu-id="93a63-102">R1Frac operation</span></span>

<span data-ttu-id="93a63-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="93a63-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="93a63-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="93a63-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="93a63-105">Применяет поворот к {1} состоянию $ \кет $ на угол, заданный как дробь ДЯДИК.</span><span class="sxs-lookup"><span data-stu-id="93a63-105">Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="93a63-106">\бегин{алигн} R_1 (n, k) \масрел{: =} \операторнаме{диаг} (1, e ^ {i \пи k/2 ^ n}).</span><span class="sxs-lookup"><span data-stu-id="93a63-106">\begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}).</span></span>
<span data-ttu-id="93a63-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="93a63-107">\end{align}</span></span>

> [!WARNING]
> <span data-ttu-id="93a63-108">Эта операция использует **противоположное** соглашение о знаках из @"microsoft.quantum.intrinsic.r" и не включает фактор $1/2 $, включенный в @"microsoft.quantum.intrinsic.r1" .</span><span class="sxs-lookup"><span data-stu-id="93a63-108">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r", and does not include the factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".</span></span>

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="93a63-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="93a63-109">Input</span></span>

### <a name="numerator--int"></a><span data-ttu-id="93a63-110">Числитель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="93a63-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="93a63-111">Числитель в ДЯДИК дробное представление угла, на которое поворачивается кубит.</span><span class="sxs-lookup"><span data-stu-id="93a63-111">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="93a63-112">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="93a63-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="93a63-113">Степень 2, указывающая знаменатель угла, на который будет поворачиваться кубит.</span><span class="sxs-lookup"><span data-stu-id="93a63-113">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="93a63-114">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="93a63-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="93a63-115">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="93a63-115">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="93a63-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="93a63-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="93a63-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="93a63-117">Remarks</span></span>

<span data-ttu-id="93a63-118">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="93a63-118">Equivalent to:</span></span>

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```