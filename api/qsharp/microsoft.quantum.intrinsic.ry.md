---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Операция дые
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 5a1f762aacca5c72dc8dbe450ab8e8a4aef12c69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198611"
---
# <a name="ry-operation"></a><span data-ttu-id="d4d2a-102">Операция дые</span><span class="sxs-lookup"><span data-stu-id="d4d2a-102">Ry operation</span></span>

<span data-ttu-id="d4d2a-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="d4d2a-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="d4d2a-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d4d2a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d4d2a-105">Применяет поворот к $y $-оси на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="d4d2a-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="d4d2a-106">\бегин{алигн} R_y (\сета) \масрел{: =} e ^ {-i \сета \ sigma_y/2} = \бегин{бматрикс} \кос \фрак{\сета} {2} &-\син \фрак{\сета} {2} \\ \\ \sin \frac{\theta} {2} & \cos \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="d4d2a-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="d4d2a-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="d4d2a-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d4d2a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d4d2a-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="d4d2a-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d4d2a-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d4d2a-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="d4d2a-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="d4d2a-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d4d2a-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d4d2a-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="d4d2a-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d4d2a-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4d2a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d4d2a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4d2a-114">Remarks</span></span>

<span data-ttu-id="d4d2a-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="d4d2a-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```