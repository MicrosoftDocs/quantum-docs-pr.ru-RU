---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Операция дые
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 9966693eb7283e855f7b72e910aa3604d6c2bd61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730776"
---
# <a name="ry-operation"></a><span data-ttu-id="71c6f-102">Операция дые</span><span class="sxs-lookup"><span data-stu-id="71c6f-102">Ry operation</span></span>

<span data-ttu-id="71c6f-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="71c6f-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="71c6f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="71c6f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="71c6f-105">Применяет поворот к $y $-оси на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="71c6f-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="71c6f-106">\бегин{алигн} R_y (\сета) \масрел{: =} e ^ {-i \сета \ sigma_y/2} = \бегин{бматрикс} \кос \фрак{\сета} {2} &-\син \фрак{\сета} {2} \\ \\ \sin \frac{\theta} {2} & \cos \frac{\theta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="71c6f-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="71c6f-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="71c6f-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="71c6f-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="71c6f-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="71c6f-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="71c6f-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="71c6f-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="71c6f-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="71c6f-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="71c6f-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="71c6f-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="71c6f-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="71c6f-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="71c6f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="71c6f-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="71c6f-114">Remarks</span></span>

<span data-ttu-id="71c6f-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="71c6f-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```