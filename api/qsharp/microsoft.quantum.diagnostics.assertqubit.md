---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Операция Ассерткубит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: fa1f52da5a011cd914a0fda69b78cf5a4fd71e16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712947"
---
# <a name="assertqubit-operation"></a><span data-ttu-id="dc7a4-102">Операция Ассерткубит</span><span class="sxs-lookup"><span data-stu-id="dc7a4-102">AssertQubit operation</span></span>

<span data-ttu-id="dc7a4-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="dc7a4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="dc7a4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc7a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc7a4-105">Утверждает, что кубит `q` находится в ожидаемом еиженстате оператора Паули Z.</span><span class="sxs-lookup"><span data-stu-id="dc7a4-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.</span></span>

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="dc7a4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="dc7a4-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="dc7a4-107">ожидалось __: <Result> недопустимо__</span><span class="sxs-lookup"><span data-stu-id="dc7a4-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="dc7a4-108">Состояние, в котором ожидается кубит: `Zero` или `One` .</span><span class="sxs-lookup"><span data-stu-id="dc7a4-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="dc7a4-109">вопрос. [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="dc7a4-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="dc7a4-110">Кубит, состояние которого утверждено.</span><span class="sxs-lookup"><span data-stu-id="dc7a4-110">The qubit whose state is asserted.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dc7a4-111">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dc7a4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="dc7a4-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="dc7a4-112">Remarks</span></span>

<span data-ttu-id="dc7a4-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> позволяет утверждать произвольные состояния кубит, а не только $Z $ еиженстатес.</span><span class="sxs-lookup"><span data-stu-id="dc7a4-113"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc7a4-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="dc7a4-114">See Also</span></span>

- [<span data-ttu-id="dc7a4-115">Microsoft. тактов. Diagnostics. Ассерткубитисинстатевисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="dc7a4-115">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)