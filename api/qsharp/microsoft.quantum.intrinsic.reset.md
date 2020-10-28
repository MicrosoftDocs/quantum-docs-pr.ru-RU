---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Операция сброса
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: c89cbbce49e294e56abc11b3b0492d2ed8e980a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731352"
---
# <a name="reset-operation"></a><span data-ttu-id="91afd-102">Операция сброса</span><span class="sxs-lookup"><span data-stu-id="91afd-102">Reset operation</span></span>

<span data-ttu-id="91afd-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="91afd-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="91afd-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91afd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="91afd-105">Учитывая один кубит, измеряет его и гарантирует, что он находится в состоянии | 0 ⟩, чтобы его можно было безопасно освободить.</span><span class="sxs-lookup"><span data-stu-id="91afd-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="91afd-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="91afd-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="91afd-107">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="91afd-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="91afd-108">Кубит, состояние которого должно быть сброшено в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="91afd-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="91afd-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91afd-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

