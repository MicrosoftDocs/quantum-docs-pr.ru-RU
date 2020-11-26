---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Операция РЗ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: d637abf3562eb60705da517467939dc588229c39
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198628"
---
# <a name="rz-operation"></a><span data-ttu-id="9103d-102">Операция РЗ</span><span class="sxs-lookup"><span data-stu-id="9103d-102">Rz operation</span></span>

<span data-ttu-id="9103d-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9103d-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9103d-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="9103d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="9103d-105">Применяет поворот к $z $-оси на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="9103d-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="9103d-106">\бегин{алигн} R_z (\сета) \масрел{: =} e ^ {-i \сета \ sigma_z/2} = \бегин{бматрикс} e ^ {-i \сета/2} & 0 \\ \\ 0 & е ^ {i \сета/2} \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="9103d-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="9103d-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="9103d-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9103d-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9103d-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="9103d-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9103d-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9103d-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="9103d-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="9103d-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9103d-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9103d-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="9103d-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9103d-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9103d-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9103d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9103d-114">Remarks</span></span>

<span data-ttu-id="9103d-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="9103d-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```