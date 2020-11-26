---
uid: Microsoft.Quantum.Intrinsic.S
title: Операция S
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: c697408c4efe1963787b5aee8f0d3bb6b9e64dd5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198458"
---
# <a name="s-operation"></a><span data-ttu-id="c164a-102">Операция S</span><span class="sxs-lookup"><span data-stu-id="c164a-102">S operation</span></span>

<span data-ttu-id="c164a-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c164a-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c164a-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c164a-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c164a-105">Применяет шлюз S к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="c164a-105">Applies the S gate to a single qubit.</span></span>

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="c164a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c164a-106">Description</span></span>

<span data-ttu-id="c164a-107">Эта операция может быть смоделирована единой матрицей \бегин{алигн} S \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ 0 & i \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="c164a-107">This operation can be simulated by the unitary matrix \begin{align} S \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="c164a-108">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="c164a-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="c164a-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c164a-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="c164a-110">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c164a-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c164a-111">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="c164a-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c164a-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c164a-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

