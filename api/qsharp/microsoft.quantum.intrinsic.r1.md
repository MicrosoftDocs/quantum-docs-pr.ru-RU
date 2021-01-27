---
uid: Microsoft.Quantum.Intrinsic.R1
title: Операция R1
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by a given angle.

  \begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}). \end{align}
ms.openlocfilehash: 07cce580b50fef5664fdac32bb4fae0ba22d25e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849348"
---
# <a name="r1-operation"></a><span data-ttu-id="ef96d-102">Операция R1</span><span class="sxs-lookup"><span data-stu-id="ef96d-102">R1 operation</span></span>

<span data-ttu-id="ef96d-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="ef96d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="ef96d-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ef96d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ef96d-105">Применяет поворот к {1} состоянию $ \кет $ на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="ef96d-105">Applies a rotation about the $\ket{1}$ state by a given angle.</span></span>

<span data-ttu-id="ef96d-106">\бегин{алигн} R_1 (\сета) \масрел{: =} \операторнаме{диаг} (1, e ^ {и\сета}).</span><span class="sxs-lookup"><span data-stu-id="ef96d-106">\begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}).</span></span>
<span data-ttu-id="ef96d-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="ef96d-107">\end{align}</span></span>

```qsharp
operation R1 (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ef96d-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ef96d-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="ef96d-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ef96d-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ef96d-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="ef96d-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="ef96d-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ef96d-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ef96d-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="ef96d-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ef96d-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef96d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ef96d-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="ef96d-114">Remarks</span></span>

<span data-ttu-id="ef96d-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="ef96d-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);
```