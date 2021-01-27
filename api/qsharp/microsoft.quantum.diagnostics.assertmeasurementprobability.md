---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Операция Ассертмеасурементпробабилити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830823"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="43437-102">Операция Ассертмеасурементпробабилити</span><span class="sxs-lookup"><span data-stu-id="43437-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="43437-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="43437-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="43437-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="43437-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="43437-105">Утверждения, измеряющие заданный Кубитс в данной Паулиной базе, будут иметь заданный результат с заданной вероятностью в пределах некоторой допустимости.</span><span class="sxs-lookup"><span data-stu-id="43437-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="43437-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="43437-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="43437-107">базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="43437-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="43437-108">Результат измерения для утверждения вероятности, выраженный как кубит оператор Паули.</span><span class="sxs-lookup"><span data-stu-id="43437-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="43437-109">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="43437-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="43437-110">Регистр, для которого необходимо выполнить утверждение.</span><span class="sxs-lookup"><span data-stu-id="43437-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="43437-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="43437-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="43437-112">Ожидаемый результат `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="43437-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="43437-113">prob: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="43437-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="43437-114">Вероятность, с которой ожидается данный результат.</span><span class="sxs-lookup"><span data-stu-id="43437-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="43437-115">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="43437-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="43437-116">Сообщение, которое необходимо сообщить, если утверждение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43437-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="43437-117">принудительно применяли стойкое: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="43437-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="43437-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43437-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="43437-119">Пример</span><span class="sxs-lookup"><span data-stu-id="43437-119">Example</span></span>

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a><span data-ttu-id="43437-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="43437-120">Remarks</span></span>

<span data-ttu-id="43437-121">Обратите внимание, что смежная и контролируемая версии этой операции не будут проверять условие.</span><span class="sxs-lookup"><span data-stu-id="43437-121">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="43437-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="43437-122">See Also</span></span>

- [<span data-ttu-id="43437-123">Microsoft. тактов. Diagnostics. Ассертмеасуремент</span><span class="sxs-lookup"><span data-stu-id="43437-123">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)