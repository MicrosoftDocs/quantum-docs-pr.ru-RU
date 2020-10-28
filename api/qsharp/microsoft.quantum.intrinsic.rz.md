---
uid: Microsoft.Quantum.Intrinsic.Rz
title: Операция РЗ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 954b0b097d4bffcb8047a9f0c8a4c28445653c5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731345"
---
# <a name="rz-operation"></a><span data-ttu-id="ef722-102">Операция РЗ</span><span class="sxs-lookup"><span data-stu-id="ef722-102">Rz operation</span></span>

<span data-ttu-id="ef722-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="ef722-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="ef722-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ef722-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ef722-105">Применяет поворот к $z $-оси на заданный угол.</span><span class="sxs-lookup"><span data-stu-id="ef722-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="ef722-106">\бегин{алигн} R_z (\сета) \масрел{: =} e ^ {-i \сета \ sigma_z/2} = \бегин{бматрикс} e ^ {-i \сета/2} & 0 \\ \\ 0 & е ^ {i \сета/2} \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="ef722-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="ef722-107">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="ef722-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ef722-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ef722-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="ef722-109">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ef722-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ef722-110">Угол поворота кубит.</span><span class="sxs-lookup"><span data-stu-id="ef722-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="ef722-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ef722-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ef722-112">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="ef722-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ef722-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ef722-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ef722-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="ef722-114">Remarks</span></span>

<span data-ttu-id="ef722-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="ef722-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```