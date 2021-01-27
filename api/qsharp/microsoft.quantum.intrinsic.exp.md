---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Операция exp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 7aa6974e83e917125b63ef91fb5c3b1238f6e856
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819016"
---
# <a name="exp-operation"></a><span data-ttu-id="e9257-102">Операция exp</span><span class="sxs-lookup"><span data-stu-id="e9257-102">Exp operation</span></span>

<span data-ttu-id="e9257-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="e9257-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="e9257-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e9257-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e9257-105">Применяет экспоненту оператора Multi-кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="e9257-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="e9257-106">\бегин{алигн} e ^ {i \сета [P_0 \отимес P_1 \кдотс P_ {N-1}]}, \енд{алигн}, где $P _i $ — это $i $ TH элемент `paulis` , а $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="e9257-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e9257-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e9257-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="e9257-108">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="e9257-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="e9257-109">Массив значений Single-кубит Паули, указывающих факторы продукта тензорные для каждого кубит.</span><span class="sxs-lookup"><span data-stu-id="e9257-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="e9257-110">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e9257-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e9257-111">Угол для данного оператора Multi-кубит Паули, на который будет повернут целевой регистр.</span><span class="sxs-lookup"><span data-stu-id="e9257-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="e9257-112">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e9257-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e9257-113">Зарегистрируйтесь, чтобы применить заданный поворот к.</span><span class="sxs-lookup"><span data-stu-id="e9257-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e9257-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e9257-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

