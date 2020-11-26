---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Операция Ассертмеасурементпробабилити
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 032b9224ad728f0637596668c2928a889deeba55
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202368"
---
# <a name="assertmeasurementprobability-operation"></a><span data-ttu-id="7733e-102">Операция Ассертмеасурементпробабилити</span><span class="sxs-lookup"><span data-stu-id="7733e-102">AssertMeasurementProbability operation</span></span>

<span data-ttu-id="7733e-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="7733e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="7733e-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7733e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7733e-105">Утверждения, измеряющие заданный Кубитс в данной Паулиной базе, будут иметь заданный результат с заданной вероятностью в пределах некоторой допустимости.</span><span class="sxs-lookup"><span data-stu-id="7733e-105">Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.</span></span>

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7733e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7733e-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="7733e-107">базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="7733e-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="7733e-108">Результат измерения для утверждения вероятности, выраженный как кубит оператор Паули.</span><span class="sxs-lookup"><span data-stu-id="7733e-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="7733e-109">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7733e-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7733e-110">Регистр, для которого необходимо выполнить утверждение.</span><span class="sxs-lookup"><span data-stu-id="7733e-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="7733e-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="7733e-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="7733e-112">Ожидаемый результат `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="7733e-112">An expected result of `Measure(bases, qubits)`.</span></span>


### <a name="prob--double"></a><span data-ttu-id="7733e-113">prob: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7733e-113">prob : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7733e-114">Вероятность, с которой ожидается данный результат.</span><span class="sxs-lookup"><span data-stu-id="7733e-114">The probability with which the given result is expected.</span></span>


### <a name="msg--string"></a><span data-ttu-id="7733e-115">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="7733e-115">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="7733e-116">Сообщение, которое необходимо сообщить, если утверждение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7733e-116">A message to be reported if the assertion fails.</span></span>


### <a name="tol--double"></a><span data-ttu-id="7733e-117">принудительно применяли стойкое: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7733e-117">tol : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--unit"></a><span data-ttu-id="7733e-118">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7733e-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7733e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7733e-119">Remarks</span></span>

<span data-ttu-id="7733e-120">Обратите внимание, что смежная и контролируемая версии этой операции не будут проверять условие.</span><span class="sxs-lookup"><span data-stu-id="7733e-120">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="7733e-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="7733e-121">See Also</span></span>

- [<span data-ttu-id="7733e-122">Microsoft. тактов. Diagnostics. Ассертмеасуремент</span><span class="sxs-lookup"><span data-stu-id="7733e-122">Microsoft.Quantum.Diagnostics.AssertMeasurement</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)