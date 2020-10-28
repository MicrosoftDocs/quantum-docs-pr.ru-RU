---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Операция Ассерткубитвисинтолеранце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 3fe4aa739c5e15199401aecb76ef551e52f6dcff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712878"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="9eb01-102">Операция Ассерткубитвисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="9eb01-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="9eb01-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9eb01-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9eb01-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9eb01-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9eb01-105">Утверждает, что кубит `q` находится в ожидаемом еиженстате оператора Паули Z вплоть до заданного допуска.</span><span class="sxs-lookup"><span data-stu-id="9eb01-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="9eb01-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="9eb01-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="9eb01-107">ожидалось __: <Result> недопустимо__</span><span class="sxs-lookup"><span data-stu-id="9eb01-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="9eb01-108">Состояние, в котором ожидается кубит: `Zero` или `One` .</span><span class="sxs-lookup"><span data-stu-id="9eb01-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="9eb01-109">вопрос. [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9eb01-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9eb01-110">Кубит, состояние которого утверждено.</span><span class="sxs-lookup"><span data-stu-id="9eb01-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="9eb01-111">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9eb01-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9eb01-112">Допуск на вероятность измерения кубит, возвращающего ожидаемый результат.</span><span class="sxs-lookup"><span data-stu-id="9eb01-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9eb01-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9eb01-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9eb01-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="9eb01-114">Remarks</span></span>

<span data-ttu-id="9eb01-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> позволяет утверждать произвольные состояния кубит, а не только $Z $ еиженстатес.</span><span class="sxs-lookup"><span data-stu-id="9eb01-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="9eb01-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="9eb01-116">See Also</span></span>

- [<span data-ttu-id="9eb01-117">Microsoft. тактов. Diagnostics. Ассерткубитисинстатевисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="9eb01-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)