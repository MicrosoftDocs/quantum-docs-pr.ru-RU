---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Операция ККНОТ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: a9186269a868c2ac9d2f15727a3b0ed1bfec3fa4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819030"
---
# <a name="ccnot-operation"></a><span data-ttu-id="e689b-102">Операция ККНОТ</span><span class="sxs-lookup"><span data-stu-id="e689b-102">CCNOT operation</span></span>

<span data-ttu-id="e689b-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="e689b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="e689b-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e689b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e689b-105">Применяет шлюз удвоенной управляемости — не (ККНОТ) к трем Кубитс.</span><span class="sxs-lookup"><span data-stu-id="e689b-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e689b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e689b-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="e689b-107">Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e689b-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e689b-108">Первый элемент управления кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="e689b-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="e689b-109">control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e689b-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e689b-110">Второй элемент управления кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="e689b-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e689b-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e689b-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e689b-112">Целевой кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="e689b-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e689b-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e689b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e689b-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="e689b-114">Remarks</span></span>

<span data-ttu-id="e689b-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="e689b-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```