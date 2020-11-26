---
uid: Microsoft.Quantum.Intrinsic.R1
title: Операция R1
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by a given angle.

  \begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}). \end{align}
ms.openlocfilehash: a98c2cc0b309a239650afd2910cc74dffa9f899a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198815"
---
# <a name="r1-operation"></a><span data-ttu-id="c1e44-102">Операция R1</span><span class="sxs-lookup"><span data-stu-id="c1e44-102">R1 operation</span></span>

<span data-ttu-id="c1e44-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c1e44-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c1e44-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c1e44-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c1e44-105">Применяет поворот к {1} состоянию $ \кет $ на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="c1e44-105">Applies a rotation about the $\ket{1}$ state by a given angle.</span></span>

<span data-ttu-id="c1e44-106">\бегин{алигн} R_1 (\сета) \масрел{: =} \операторнаме{диаг} (1, e ^ {и\сета}).</span><span class="sxs-lookup"><span data-stu-id="c1e44-106">\begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}).</span></span>
<span data-ttu-id="c1e44-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="c1e44-107">\end{align}</span></span>

```qsharp
operation R1 (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c1e44-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c1e44-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="c1e44-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c1e44-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c1e44-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="c1e44-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="c1e44-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c1e44-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c1e44-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="c1e44-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c1e44-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c1e44-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c1e44-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1e44-114">Remarks</span></span>

<span data-ttu-id="c1e44-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="c1e44-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);
```