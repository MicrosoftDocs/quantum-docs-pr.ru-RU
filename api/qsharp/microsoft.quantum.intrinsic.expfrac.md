---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Операция Експфрак
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: d11912a272387b087098f59e7ac071534b01c054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711491"
---
# <a name="expfrac-operation"></a><span data-ttu-id="67100-102">Операция Експфрак</span><span class="sxs-lookup"><span data-stu-id="67100-102">ExpFrac operation</span></span>

<span data-ttu-id="67100-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="67100-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="67100-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67100-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67100-105">Применяет экспоненту оператора Multi-кубит Паули с аргументом, заданным в дробной части ДЯДИК.</span><span class="sxs-lookup"><span data-stu-id="67100-105">Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.</span></span>

<span data-ttu-id="67100-106">\бегин{алигн} e ^ {i \пи k [P_0 \отимес P_1 \кдотс P_ {N-1}]/2 ^ N}, \енд{алигн}, где $P _i $ — это $i $ th элемента `paulis` , где $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="67100-106">\begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="67100-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="67100-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="67100-108">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="67100-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="67100-109">Массив значений Single-кубит Паули, указывающих факторы продукта тензорные для каждого кубит.</span><span class="sxs-lookup"><span data-stu-id="67100-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="67100-110">Числитель: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="67100-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="67100-111">Числитель ($k $) в дробном представлении ДЯДИК угла, на которое будет поворачиваться регистр кубит.</span><span class="sxs-lookup"><span data-stu-id="67100-111">Numerator ($k$) in the dyadic fraction representation of the angle by which the qubit register is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="67100-112">степень: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="67100-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="67100-113">Степень двух ($n $), указывающая знаменатель угла, на который будет повернут регистр кубит.</span><span class="sxs-lookup"><span data-stu-id="67100-113">Power of two ($n$) specifying the denominator of the angle by which the qubit register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="67100-114">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="67100-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="67100-115">Зарегистрируйтесь, чтобы применить заданный поворот к.</span><span class="sxs-lookup"><span data-stu-id="67100-115">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="67100-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="67100-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

