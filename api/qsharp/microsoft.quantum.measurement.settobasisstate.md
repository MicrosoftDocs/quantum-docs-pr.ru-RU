---
uid: Microsoft.Quantum.Measurement.SetToBasisState
title: Операция Сеттобасисстате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: SetToBasisState
qsharp.summary: Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.
ms.openlocfilehash: 2612bfe488c830abd835be89b2f8ea6795abf675
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194157"
---
# <a name="settobasisstate-operation"></a><span data-ttu-id="8939d-102">Операция Сеттобасисстате</span><span class="sxs-lookup"><span data-stu-id="8939d-102">SetToBasisState operation</span></span>

<span data-ttu-id="8939d-103">Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="8939d-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="8939d-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="8939d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="8939d-105">Задает кубит для заданного вычислительного состояния, измеряя кубит и применяя бит отражения при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8939d-105">Sets a qubit to a given computational basis state by measuring the qubit and applying a bit flip if needed.</span></span>

```qsharp
operation SetToBasisState (desired : Result, target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="8939d-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8939d-106">Input</span></span>

### <a name="desired--__invalidresult__"></a><span data-ttu-id="8939d-107">требуемое __: <Result> недопустимо__</span><span class="sxs-lookup"><span data-stu-id="8939d-107">desired : __invalid<Result>__</span></span>

<span data-ttu-id="8939d-108">Состояние основания, для которого должно быть установлено значение кубит.</span><span class="sxs-lookup"><span data-stu-id="8939d-108">The basis state that the qubit should be set to.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8939d-109">Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8939d-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8939d-110">Кубит, состояние которого должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="8939d-110">The qubit whose state is to be set.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8939d-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8939d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8939d-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8939d-112">Remarks</span></span>

<span data-ttu-id="8939d-113">В качестве инварианта этой операции вызов `M(q)` сразу после вернет значение `SetToBasisState(result, q)` `result` .</span><span class="sxs-lookup"><span data-stu-id="8939d-113">As an invariant of this operation, calling `M(q)` immediately after `SetToBasisState(result, q)` will return `result`.</span></span>