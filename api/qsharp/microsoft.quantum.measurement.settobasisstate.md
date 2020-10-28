---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Операция Сеттобасисстате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: bb40ddcf6518a30f5d88eec21cf8e2c2d6e0bbaf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733601"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="6de11-102">Операция Сеттобасисстате</span><span class="sxs-lookup"><span data-stu-id="6de11-102">SetToBasisState operation</span></span>

<span data-ttu-id="6de11-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="6de11-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="6de11-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6de11-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6de11-105">Задает кубит для заданного вычислительного состояния, измеряя кубит и применяя бит отражения при необходимости.</span><span class="sxs-lookup"><span data-stu-id="6de11-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="6de11-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6de11-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="6de11-107">требуемое __: <Result> недопустимо__</span><span class="sxs-lookup"><span data-stu-id="6de11-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="6de11-108">Состояние основания, для которого должно быть установлено значение кубит.</span><span class="sxs-lookup"><span data-stu-id="6de11-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="6de11-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6de11-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6de11-110">Кубит, состояние которого должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="6de11-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6de11-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6de11-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6de11-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="6de11-112">Remarks</span></span>

<span data-ttu-id="6de11-113">В качестве инварианта этой операции вызов `M(q)` сразу после вернет значение `SetToBasisState(result, q)` `result` .</span><span class="sxs-lookup"><span data-stu-id="6de11-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>