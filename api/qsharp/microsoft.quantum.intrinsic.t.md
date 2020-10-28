---
uid: Microsoft.Quantum.Intrinsic.T
title: Операция T
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 868031386c95f65ae956b5e444c6d87d7ea0a697
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731337"
---
# <a name="t-operation"></a><span data-ttu-id="3ad9b-102">Операция T</span><span class="sxs-lookup"><span data-stu-id="3ad9b-102">T operation</span></span>

<span data-ttu-id="3ad9b-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="3ad9b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="3ad9b-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3ad9b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3ad9b-105">Применяет T-шлюз к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="3ad9b-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="3ad9b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3ad9b-106">Description</span></span>

<span data-ttu-id="3ad9b-107">Эта операция может быть смоделирована единой матрицей \бегин{алигн} T \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ 0 & e ^ {i \пи/4} \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="3ad9b-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="3ad9b-108">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="3ad9b-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="3ad9b-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3ad9b-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="3ad9b-110">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3ad9b-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3ad9b-111">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="3ad9b-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ad9b-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ad9b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

