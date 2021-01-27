---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Операция измерения
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: bf0a606b1bfc8c4762245422450ec26907ec1946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818773"
---
# <a name="measure-operation"></a><span data-ttu-id="d3415-102">Операция измерения</span><span class="sxs-lookup"><span data-stu-id="d3415-102">Measure operation</span></span>

<span data-ttu-id="d3415-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="d3415-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="d3415-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d3415-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d3415-105">Выполняет совместное измерение одного или нескольких Кубитс в указанных базовых базах Паули.</span><span class="sxs-lookup"><span data-stu-id="d3415-105">Performs a joint measurement of one or more qubits in the specified Pauli bases.</span></span>

<span data-ttu-id="d3415-106">Результат получается в результате распределения: \бегин{алигн} \Пр (\Тексттт{зеро} | \кет{\пси}) = \frac12 \бракет{\пси \мид | \лефт (\болдоне + P_0 \отимес P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align}, где $P _i $ — это $i $ TH `bases` , и where $N = \texttt{Length} (\texttt{bases}) $.</span><span class="sxs-lookup"><span data-stu-id="d3415-106">The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$.</span></span>
<span data-ttu-id="d3415-107">То есть измерение возвращает `Result` $d $ таким, что еиженвалуе наблюдаемый результат измерения равен $ (-1) ^ d $.</span><span class="sxs-lookup"><span data-stu-id="d3415-107">That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.</span></span>

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a><span data-ttu-id="d3415-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d3415-108">Input</span></span>

### <a name="bases--pauli"></a><span data-ttu-id="d3415-109">базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="d3415-109">bases : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="d3415-110">Массив значений Single-кубит Паули, указывающих факторы продукта тензорные для каждого кубит.</span><span class="sxs-lookup"><span data-stu-id="d3415-110">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="d3415-111">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d3415-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d3415-112">Регистрация Кубитс для измерения.</span><span class="sxs-lookup"><span data-stu-id="d3415-112">Register of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="d3415-113">Выходные данные __: <Result> Недопустимый__</span><span class="sxs-lookup"><span data-stu-id="d3415-113">Output : __invalid<Result>__</span></span>

<span data-ttu-id="d3415-114">`Zero` Если обнаружено значение $ + $1 еиженвалуе, а `One` также значение $-$1 еиженвалуе.</span><span class="sxs-lookup"><span data-stu-id="d3415-114">`Zero` if the $+1$ eigenvalue is observed, and `One` if the $-1$ eigenvalue is observed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3415-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="d3415-115">Remarks</span></span>

<span data-ttu-id="d3415-116">Если базовый массив и массив кубит имеют разную длину, операция завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d3415-116">If the basis array and qubit array are different lengths, then the operation will fail.</span></span>