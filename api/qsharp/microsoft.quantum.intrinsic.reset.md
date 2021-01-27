---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Операция сброса
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: b4275796b966bfe7f55271f4e92866410a14e830
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818629"
---
# <a name="reset-operation"></a><span data-ttu-id="16a1b-102">Операция сброса</span><span class="sxs-lookup"><span data-stu-id="16a1b-102">Reset operation</span></span>

<span data-ttu-id="16a1b-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="16a1b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="16a1b-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="16a1b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="16a1b-105">Учитывая один кубит, измеряет его и гарантирует, что он находится в состоянии | 0 ⟩, чтобы его можно было безопасно освободить.</span><span class="sxs-lookup"><span data-stu-id="16a1b-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="16a1b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="16a1b-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="16a1b-107">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="16a1b-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="16a1b-108">Кубит, состояние которого должно быть сброшено в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="16a1b-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="16a1b-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="16a1b-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

