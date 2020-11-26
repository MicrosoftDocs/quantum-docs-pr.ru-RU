---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Операция ККНОТ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: 715796ddd915d80036933e3f1ceefa97aa62cecf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212483"
---
# <a name="ccnot-operation"></a><span data-ttu-id="20d1b-102">Операция ККНОТ</span><span class="sxs-lookup"><span data-stu-id="20d1b-102">CCNOT operation</span></span>

<span data-ttu-id="20d1b-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="20d1b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="20d1b-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="20d1b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="20d1b-105">Применяет шлюз удвоенной управляемости — не (ККНОТ) к трем Кубитс.</span><span class="sxs-lookup"><span data-stu-id="20d1b-105">Applies the doubly controlled–NOT (CCNOT) gate to three qubits.</span></span>

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="20d1b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="20d1b-106">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="20d1b-107">Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="20d1b-107">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="20d1b-108">Первый элемент управления кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="20d1b-108">First control qubit for the CCNOT gate.</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="20d1b-109">control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="20d1b-109">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="20d1b-110">Второй элемент управления кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="20d1b-110">Second control qubit for the CCNOT gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="20d1b-111">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="20d1b-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="20d1b-112">Целевой кубит для шлюза ККНОТ.</span><span class="sxs-lookup"><span data-stu-id="20d1b-112">Target qubit for the CCNOT gate.</span></span>



## <a name="output--unit"></a><span data-ttu-id="20d1b-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20d1b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="20d1b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20d1b-114">Remarks</span></span>

<span data-ttu-id="20d1b-115">Эквивалентно:</span><span class="sxs-lookup"><span data-stu-id="20d1b-115">Equivalent to:</span></span>

```qsharp
Controlled X([control1, control2], target);
```