---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Операция exp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: b923374a954f90aba2deaead79dd419fbf67fea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711520"
---
# <a name="exp-operation"></a><span data-ttu-id="5a6d7-102">Операция exp</span><span class="sxs-lookup"><span data-stu-id="5a6d7-102">Exp operation</span></span>

<span data-ttu-id="5a6d7-103">Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="5a6d7-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="5a6d7-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5a6d7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5a6d7-105">Применяет экспоненту оператора Multi-кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="5a6d7-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="5a6d7-106">\бегин{алигн} e ^ {i \сета [P_0 \отимес P_1 \кдотс P_ {N-1}]}, \енд{алигн}, где $P _i $ — это $i $ TH элемент `paulis` , а $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="5a6d7-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5a6d7-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="5a6d7-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="5a6d7-108">Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="5a6d7-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="5a6d7-109">Массив значений Single-кубит Паули, указывающих факторы продукта тензорные для каждого кубит.</span><span class="sxs-lookup"><span data-stu-id="5a6d7-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="5a6d7-110">тета: [двойной](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a6d7-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5a6d7-111">Угол для данного оператора Multi-кубит Паули, на который будет повернут целевой регистр.</span><span class="sxs-lookup"><span data-stu-id="5a6d7-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5a6d7-112">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5a6d7-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5a6d7-113">Зарегистрируйтесь, чтобы применить заданный поворот к.</span><span class="sxs-lookup"><span data-stu-id="5a6d7-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5a6d7-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5a6d7-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

