---
uid: Microsoft.Quantum.Intrinsic.T
title: Операция T
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: bee252d9905aed26f6bf663f895e464e38073f44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817514"
---
# <a name="t-operation"></a><span data-ttu-id="e0f9c-102">Операция T</span><span class="sxs-lookup"><span data-stu-id="e0f9c-102">T operation</span></span>

<span data-ttu-id="e0f9c-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="e0f9c-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="e0f9c-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e0f9c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e0f9c-105">Применяет T-шлюз к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e0f9c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e0f9c-106">Description</span></span>

<span data-ttu-id="e0f9c-107">Эта операция может быть смоделирована единой матрицей \бегин{алигн} T \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ 0 & e ^ {i \пи/4} \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="e0f9c-108">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="e0f9c-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="e0f9c-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e0f9c-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="e0f9c-110">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e0f9c-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e0f9c-111">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="e0f9c-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e0f9c-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e0f9c-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

