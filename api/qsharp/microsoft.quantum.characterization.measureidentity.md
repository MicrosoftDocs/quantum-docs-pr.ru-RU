---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Операция Меасуреидентити
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 71a103fddb3a27703318975bea94bc7a22a9ce81
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714964"
---
# <a name="measureidentity-operation"></a><span data-ttu-id="ceb6c-102">Операция Меасуреидентити</span><span class="sxs-lookup"><span data-stu-id="ceb6c-102">MeasureIdentity operation</span></span>

<span data-ttu-id="ceb6c-103">Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="ceb6c-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="ceb6c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ceb6c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ceb6c-105">Измеряет оператор Identity в регистре Кубитс.</span><span class="sxs-lookup"><span data-stu-id="ceb6c-105">Measures the identity operator on a register of qubits.</span></span>

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="ceb6c-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ceb6c-106">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="ceb6c-107">Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ceb6c-107">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ceb6c-108">Регистр для измерения.</span><span class="sxs-lookup"><span data-stu-id="ceb6c-108">The register to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="ceb6c-109">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="ceb6c-109">Output : __invalid<Result>__</span></span>

<span data-ttu-id="ceb6c-110">Результирующее значение `Zero` .</span><span class="sxs-lookup"><span data-stu-id="ceb6c-110">The result value `Zero`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb6c-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="ceb6c-111">Remarks</span></span>

<span data-ttu-id="ceb6c-112">Поскольку $ \болдоне $ имеет только еиженвалуе $1 $ и не имеет отрицательного еиженвалуе, эта операция всегда возвращает значение `Zero` , соответствующее еиженвалуе $ + 1 = (-1) ^ 0 $, и не приводит к свертыванию состояния `register` .</span><span class="sxs-lookup"><span data-stu-id="ceb6c-112">Since $\boldone$ has only the eigenvalue $1$, and does not have a negative eigenvalue, this operation always returns `Zero`, corresponding to the eigenvalue $+1 = (-1)^0$, and does not cause a collapse of the state of `register`.</span></span>

<span data-ttu-id="ceb6c-113">Сам по себе эта операция нецелесообразна, но она полезна в контексте процесса томографи, так как она предоставляет сведения о сохранении трассировки процесса обработки такта.</span><span class="sxs-lookup"><span data-stu-id="ceb6c-113">On its own, this operation is not useful, but is helpful in the context of process tomography, as it provides information about the trace preservation of a quantum process.</span></span>
<span data-ttu-id="ceb6c-114">В частности, целевой компьютер с измерением потери данных должен заменить эту операцию фактическим измерением $ \болдоне $.</span><span class="sxs-lookup"><span data-stu-id="ceb6c-114">In particular, a target machine with lossy measurement should replace this operation by an actual measurement of $\boldone$.</span></span>