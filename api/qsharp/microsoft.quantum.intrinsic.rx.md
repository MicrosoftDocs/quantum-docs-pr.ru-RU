---
uid: Microsoft.Quantum.Intrinsic.Rx
title: Операция RX
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rx
qsharp.summary: >-
  Applies a rotation about the $x$-axis by a given angle.

  \begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 6d11c8fa3c3fb2c07a88fdf2cba0ff2a7f51bf6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732936"
---
# <a name="rx-operation"></a><span data-ttu-id="b8ab2-102">Операция RX</span><span class="sxs-lookup"><span data-stu-id="b8ab2-102">Rx operation</span></span>

<span data-ttu-id="b8ab2-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="b8ab2-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="b8ab2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b8ab2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b8ab2-105">Применяет поворот к $x $-оси на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="b8ab2-105">Applies a rotation about the $x$-axis by a given angle.</span></span>

<span data-ttu-id="b8ab2-106">\бегин{алигн} R_x (\сета) \масрел{: =} e ^ {-i \сета \ sigma_x/2} = \бегин{бматрикс} \кос \фрак{\сета} {2} &-и\син \фрак{\сета} {2} \\ \\ -i\sin \frac{\theta} {2} & \cos \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="b8ab2-106">\begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="b8ab2-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="b8ab2-107">\end{align}</span></span>

```qsharp
operation Rx (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="b8ab2-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b8ab2-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="b8ab2-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b8ab2-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b8ab2-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="b8ab2-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="b8ab2-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b8ab2-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b8ab2-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="b8ab2-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b8ab2-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b8ab2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b8ab2-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="b8ab2-114">Remarks</span></span>

<span data-ttu-id="b8ab2-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="b8ab2-115">Equivalent to:</span></span>

```qsharp
R(PauliX, theta, qubit);
```