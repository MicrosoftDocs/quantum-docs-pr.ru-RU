---
uid: Microsoft.Quantum.Intrinsic.R
title: Операция R
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 1df4b1197e885e479339e542e8c1ffaeb392543d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818713"
---
# <a name="r-operation"></a><span data-ttu-id="820f4-102">Операция R</span><span class="sxs-lookup"><span data-stu-id="820f4-102">R operation</span></span>

<span data-ttu-id="820f4-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="820f4-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="820f4-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="820f4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="820f4-105">Применяет поворот к заданной оси Паули.</span><span class="sxs-lookup"><span data-stu-id="820f4-105">Applies a rotation about the given Pauli axis.</span></span>

<span data-ttu-id="820f4-106">\бегин{алигн} R_ {\му} (\сета) \масрел{: =} e ^ {-i \сета \ sigma_ {\му}/2}, \енд{алигн}, где $ \му \ин \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="820f4-106">\begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="820f4-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="820f4-107">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="820f4-108">Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="820f4-108">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="820f4-109">Паули оператор ($ \му $) в возведен для образования вращения.</span><span class="sxs-lookup"><span data-stu-id="820f4-109">Pauli operator ($\mu$) to be exponentiated to form the rotation.</span></span>


### <a name="theta--double"></a><span data-ttu-id="820f4-110">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="820f4-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="820f4-111">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="820f4-111">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="820f4-112">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="820f4-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="820f4-113">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="820f4-113">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="820f4-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="820f4-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="820f4-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="820f4-115">Remarks</span></span>

<span data-ttu-id="820f4-116">При вызове с `pauli = PauliI` Эта операция применяет *глобальный этап*.</span><span class="sxs-lookup"><span data-stu-id="820f4-116">When called with `pauli = PauliI`, this operation applies a *global phase*.</span></span> <span data-ttu-id="820f4-117">Этот этап может быть важен при использовании с `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="820f4-117">This phase can be significant when used with the `Controlled` functor.</span></span>