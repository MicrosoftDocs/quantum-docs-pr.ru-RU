---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Операция Ассерткубит
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: 0e005230427bbd570133712679c51661e7ae6496
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202249"
---
# <a name="assertqubit-operation"></a><span data-ttu-id="3d79f-102">Операция Ассерткубит</span><span class="sxs-lookup"><span data-stu-id="3d79f-102">AssertQubit operation</span></span>

<span data-ttu-id="3d79f-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="3d79f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="3d79f-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3d79f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3d79f-105">Утверждает, что кубит `q` находится в ожидаемом еиженстате оператора Паули Z.</span><span class="sxs-lookup"><span data-stu-id="3d79f-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.</span></span>

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="3d79f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="3d79f-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="3d79f-107">ожидалось __: <Result> недопустимо__</span><span class="sxs-lookup"><span data-stu-id="3d79f-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="3d79f-108">Состояние, в котором ожидается кубит: `Zero` или `One` .</span><span class="sxs-lookup"><span data-stu-id="3d79f-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="3d79f-109">вопрос. [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3d79f-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3d79f-110">Кубит, состояние которого утверждено.</span><span class="sxs-lookup"><span data-stu-id="3d79f-110">The qubit whose state is asserted.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3d79f-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3d79f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3d79f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d79f-112">Remarks</span></span>

<span data-ttu-id="3d79f-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> позволяет утверждать произвольные состояния кубит, а не только $Z $ еиженстатес.</span><span class="sxs-lookup"><span data-stu-id="3d79f-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d79f-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="3d79f-114">See Also</span></span>

- [<span data-ttu-id="3d79f-115">Microsoft. тактов. Diagnostics. Ассерткубитисинстатевисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="3d79f-115">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)