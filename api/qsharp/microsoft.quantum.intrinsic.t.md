---
uid: Microsoft.Quantum.Intrinsic.T
title: Операция T
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 352ef2c1b15a46dea85c420fc6f1cfab0382e73a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198407"
---
# <a name="t-operation"></a><span data-ttu-id="1b994-102">Операция T</span><span class="sxs-lookup"><span data-stu-id="1b994-102">T operation</span></span>

<span data-ttu-id="1b994-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="1b994-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="1b994-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1b994-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1b994-105">Применяет T-шлюз к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="1b994-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="1b994-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1b994-106">Description</span></span>

<span data-ttu-id="1b994-107">Эта операция может быть смоделирована единой матрицей \бегин{алигн} T \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ 0 & e ^ {i \пи/4} \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="1b994-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="1b994-108">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="1b994-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="1b994-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="1b994-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="1b994-110">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="1b994-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="1b994-111">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="1b994-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1b994-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1b994-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

