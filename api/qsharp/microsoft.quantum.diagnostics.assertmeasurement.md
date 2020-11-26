---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Операция Ассертмеасуремент
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 3fbe000202abbd8a206b0c83dfa35f4546ea91cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202453"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="b089f-102">Операция Ассертмеасуремент</span><span class="sxs-lookup"><span data-stu-id="b089f-102">AssertMeasurement operation</span></span>

<span data-ttu-id="b089f-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="b089f-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="b089f-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b089f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b089f-105">Утверждения, которые измеряют данный Кубитс в заданной Паули базисе, всегда будут иметь заданный результат.</span><span class="sxs-lookup"><span data-stu-id="b089f-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b089f-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b089f-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="b089f-107">базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="b089f-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="b089f-108">Результат измерения для утверждения вероятности, выраженный как кубит оператор Паули.</span><span class="sxs-lookup"><span data-stu-id="b089f-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="b089f-109">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b089f-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b089f-110">Регистр, для которого необходимо выполнить утверждение.</span><span class="sxs-lookup"><span data-stu-id="b089f-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="b089f-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="b089f-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="b089f-112">Ожидаемый результат `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="b089f-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="b089f-113">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="b089f-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="b089f-114">Сообщение, которое необходимо сообщить, если утверждение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b089f-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b089f-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b089f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b089f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b089f-116">Remarks</span></span>

<span data-ttu-id="b089f-117">Обратите внимание, что смежная и контролируемая версии этой операции не будут проверять условие.</span><span class="sxs-lookup"><span data-stu-id="b089f-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="b089f-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="b089f-118">See Also</span></span>

- [<span data-ttu-id="b089f-119">Microsoft. тактов. Diagnostics. Ассертмеасурементпробабилити</span><span class="sxs-lookup"><span data-stu-id="b089f-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)