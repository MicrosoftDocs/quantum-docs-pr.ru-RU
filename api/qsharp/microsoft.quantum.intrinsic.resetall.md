---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: Операция Ресеталл
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 2b8e7fc0e7881d8c1bd6f14c150476262b7a2b19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849316"
---
# <a name="resetall-operation"></a><span data-ttu-id="2bddf-102">Операция Ресеталл</span><span class="sxs-lookup"><span data-stu-id="2bddf-102">ResetAll operation</span></span>

<span data-ttu-id="2bddf-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="2bddf-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="2bddf-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2bddf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2bddf-105">Учитывая массив Кубитс, измерьте их и убедитесь, что они находятся в состоянии | 0 ⟩, чтобы их можно было безопасно освободить.</span><span class="sxs-lookup"><span data-stu-id="2bddf-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="2bddf-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2bddf-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="2bddf-107">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="2bddf-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="2bddf-108">Массив Кубитс, чьи состояния должны быть сброшены в $ \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="2bddf-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2bddf-109">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2bddf-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

