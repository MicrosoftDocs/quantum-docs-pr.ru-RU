---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Операция Ассерткубитвисинтолеранце
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 56b7f93f33ae18146c1fb13d404fc1d119eee72e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202198"
---
# <a name="assertqubitwithintolerance-operation"></a><span data-ttu-id="c6f05-102">Операция Ассерткубитвисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="c6f05-102">AssertQubitWithinTolerance operation</span></span>

<span data-ttu-id="c6f05-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c6f05-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c6f05-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c6f05-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c6f05-105">Утверждает, что кубит `q` находится в ожидаемом еиженстате оператора Паули Z вплоть до заданного допуска.</span><span class="sxs-lookup"><span data-stu-id="c6f05-105">Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.</span></span>

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="c6f05-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c6f05-106">Input</span></span>

### <a name="expected--__invalidresult__"></a><span data-ttu-id="c6f05-107">ожидалось __: <Result> недопустимо__</span><span class="sxs-lookup"><span data-stu-id="c6f05-107">expected : __invalid<Result>__</span></span>

<span data-ttu-id="c6f05-108">Состояние, в котором ожидается кубит: `Zero` или `One` .</span><span class="sxs-lookup"><span data-stu-id="c6f05-108">Which state the qubit is expected to be in: `Zero` or `One`.</span></span>


### <a name="q--qubit"></a><span data-ttu-id="c6f05-109">вопрос. [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c6f05-109">q : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c6f05-110">Кубит, состояние которого утверждено.</span><span class="sxs-lookup"><span data-stu-id="c6f05-110">The qubit whose state is asserted.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="c6f05-111">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c6f05-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c6f05-112">Допуск на вероятность измерения кубит, возвращающего ожидаемый результат.</span><span class="sxs-lookup"><span data-stu-id="c6f05-112">Tolerance on the probability of a measurement of the qubit returning the expected result.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c6f05-113">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c6f05-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c6f05-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6f05-114">Remarks</span></span>

<span data-ttu-id="c6f05-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> позволяет утверждать произвольные состояния кубит, а не только $Z $ еиженстатес.</span><span class="sxs-lookup"><span data-stu-id="c6f05-115"><xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> allows for asserting arbitrary qubit states rather than only $Z$ eigenstates.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6f05-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="c6f05-116">See Also</span></span>

- [<span data-ttu-id="c6f05-117">Microsoft. тактов. Diagnostics. Ассерткубитисинстатевисинтолеранце</span><span class="sxs-lookup"><span data-stu-id="c6f05-117">Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)