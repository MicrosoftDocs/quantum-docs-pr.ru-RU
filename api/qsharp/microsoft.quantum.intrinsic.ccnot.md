---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Операция ККНОТ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711534"
---
# <a name="ccnot-operation"></a><span data-ttu-id="c803e-102">Операция ККНОТ</span><span class="sxs-lookup"><span data-stu-id="c803e-102">CCNOT operation</span></span>

<span data-ttu-id="c803e-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c803e-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c803e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c803e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c803e-105">Применяет шлюз удвоенной управляемости — не (ККНОТ) к трем Кубитс.</span><span class="sxs-lookup"><span data-stu-id="c803e-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="c803e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c803e-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="c803e-107">Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c803e-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c803e-108">Первый элемент управления кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="c803e-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="c803e-109">control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c803e-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c803e-110">Второй элемент управления кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="c803e-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="c803e-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c803e-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c803e-112">Целевой кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="c803e-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c803e-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c803e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c803e-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="c803e-114">Remarks</span></span>

<span data-ttu-id="c803e-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="c803e-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```