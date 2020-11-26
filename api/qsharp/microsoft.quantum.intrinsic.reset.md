---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Операция сброса
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: 61b5e4ccdf009dcb6c639e3d8e23bc73a6e475b5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198679"
---
# <a name="reset-operation"></a><span data-ttu-id="c89fc-102">Операция сброса</span><span class="sxs-lookup"><span data-stu-id="c89fc-102">Reset operation</span></span>

<span data-ttu-id="c89fc-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c89fc-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c89fc-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c89fc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c89fc-105">Учитывая один кубит, измеряет его и гарантирует, что он находится в состоянии | 0 ⟩, чтобы его можно было безопасно освободить.</span><span class="sxs-lookup"><span data-stu-id="c89fc-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="c89fc-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c89fc-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="c89fc-107">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c89fc-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c89fc-108">Кубит, состояние которого должно быть сброшено в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="c89fc-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c89fc-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c89fc-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

