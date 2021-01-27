---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Операция РЗ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 4282fcc216173234ec742991b8f0fa1be203da0d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849289"
---
# <a name="rz-operation"></a><span data-ttu-id="01222-102">Операция РЗ</span><span class="sxs-lookup"><span data-stu-id="01222-102">Rz operation</span></span>

<span data-ttu-id="01222-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="01222-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="01222-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="01222-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="01222-105">Применяет поворот к $z $-оси на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="01222-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="01222-106">\бегин{алигн} R_z (\сета) \масрел{: =} e ^ {-i \сета \ sigma_z/2} = \бегин{бматрикс} e ^ {-i \сета/2} & 0 \\ \\ 0 & е ^ {i \сета/2} \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="01222-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="01222-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="01222-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="01222-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="01222-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="01222-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="01222-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="01222-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="01222-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="01222-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="01222-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="01222-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="01222-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="01222-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="01222-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="01222-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="01222-114">Remarks</span></span>

<span data-ttu-id="01222-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="01222-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```