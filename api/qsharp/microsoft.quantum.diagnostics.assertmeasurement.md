---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Операция Ассертмеасуремент
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 09024cd8cd6e713360dcf7f42f55941590f35883
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713032"
---
# <a name="assertmeasurement-operation"></a><span data-ttu-id="22ff6-102">Операция Ассертмеасуремент</span><span class="sxs-lookup"><span data-stu-id="22ff6-102">AssertMeasurement operation</span></span>

<span data-ttu-id="22ff6-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="22ff6-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="22ff6-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="22ff6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="22ff6-105">Утверждения, которые измеряют данный Кубитс в заданной Паули базисе, всегда будут иметь заданный результат.</span><span class="sxs-lookup"><span data-stu-id="22ff6-105">Asserts that measuring the given qubits in the given Pauli basis will always have the given result.</span></span>

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit
```


## <a name="input"></a><span data-ttu-id="22ff6-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="22ff6-106">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="22ff6-107">базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="22ff6-107">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="22ff6-108">Результат измерения для утверждения вероятности, выраженный как кубит оператор Паули.</span><span class="sxs-lookup"><span data-stu-id="22ff6-108">A measurement effect to assert the probability of, expressed as a multi-qubit Pauli operator.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="22ff6-109">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="22ff6-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="22ff6-110">Регистр, для которого необходимо выполнить утверждение.</span><span class="sxs-lookup"><span data-stu-id="22ff6-110">A register on which to make the assertion.</span></span>


### <a name="result--__invalidresult__"></a><span data-ttu-id="22ff6-111">результат: __недопустимо <Result>__</span><span class="sxs-lookup"><span data-stu-id="22ff6-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="22ff6-112">Ожидаемый результат `Measure(bases, qubits)` .</span><span class="sxs-lookup"><span data-stu-id="22ff6-112">The expected result of `Measure(bases, qubits)`.</span></span>


### <a name="msg--string"></a><span data-ttu-id="22ff6-113">сообщение: [строка](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="22ff6-113">msg : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="22ff6-114">Сообщение, которое необходимо сообщить, если утверждение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22ff6-114">A message to be reported if the assertion fails.</span></span>



## <a name="output--unit"></a><span data-ttu-id="22ff6-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="22ff6-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="22ff6-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="22ff6-116">Remarks</span></span>

<span data-ttu-id="22ff6-117">Обратите внимание, что смежная и контролируемая версии этой операции не будут проверять условие.</span><span class="sxs-lookup"><span data-stu-id="22ff6-117">Note that the Adjoint and Controlled versions of this operation will not check the condition.</span></span>

## <a name="see-also"></a><span data-ttu-id="22ff6-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="22ff6-118">See Also</span></span>

- [<span data-ttu-id="22ff6-119">Microsoft. тактов. Diagnostics. Ассертмеасурементпробабилити</span><span class="sxs-lookup"><span data-stu-id="22ff6-119">Microsoft.Quantum.Diagnostics.AssertMeasurementProbability</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)