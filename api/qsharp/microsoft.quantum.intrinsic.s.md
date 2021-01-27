---
uid: Microsoft.Quantum.Intrinsic.S
title: Операция S
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: be9078dfdcc4eecf317b0542b1c42a8d60466a5f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817529"
---
# <a name="s-operation"></a><span data-ttu-id="b0ccb-102">Операция S</span><span class="sxs-lookup"><span data-stu-id="b0ccb-102">S operation</span></span>

<span data-ttu-id="b0ccb-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="b0ccb-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="b0ccb-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b0ccb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b0ccb-105">Применяет шлюз S к одному кубит.</span><span class="sxs-lookup"><span data-stu-id="b0ccb-105">Applies the S gate to a single qubit.</span></span>

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="b0ccb-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b0ccb-106">Description</span></span>

<span data-ttu-id="b0ccb-107">Эта операция может быть смоделирована единой матрицей \бегин{алигн} S \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ 0 & i \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="b0ccb-107">This operation can be simulated by the unitary matrix \begin{align} S \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="b0ccb-108">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="b0ccb-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="b0ccb-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b0ccb-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="b0ccb-110">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b0ccb-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b0ccb-111">Кубит, к которому должен быть применен шлюз.</span><span class="sxs-lookup"><span data-stu-id="b0ccb-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b0ccb-112">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b0ccb-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

