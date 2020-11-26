---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Операция Ассертоператионсекуалинплаце
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 9b17bac9d95baf5a542604892c64130bf35d7f69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202436"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="bdac4-102">Операция Ассертоператионсекуалинплаце</span><span class="sxs-lookup"><span data-stu-id="bdac4-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="bdac4-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="bdac4-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="bdac4-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bdac4-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="bdac4-105">Учитывая две операции, утверждает, что они действуют одинаково для всех входных состояний.</span><span class="sxs-lookup"><span data-stu-id="bdac4-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="bdac4-106">Это утверждение реализуется путем проверки действия операций во всех состояниях формы $V _0 \отимес... \отимес V_ {n-1} $, где $V _k $ является одним из состояний $ \кет {0} $, $ \кет {1} $, $ \кет{+} $ и $ \кет{и} $ (+ 1 Еиженстате of Паули Y).</span><span class="sxs-lookup"><span data-stu-id="bdac4-106">This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).</span></span>

<span data-ttu-id="bdac4-107">Это утверждение использует $n $ Кубитс и требует нескольких вызовов сравниваемых операций.</span><span class="sxs-lookup"><span data-stu-id="bdac4-107">This assertion uses $n$ qubits and requires multiple calls of the operations being compared.</span></span>

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="bdac4-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bdac4-108">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="bdac4-109">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bdac4-109">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bdac4-110">Число Кубитс $n $, с которыми работают операции `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="bdac4-110">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="bdac4-111">Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="bdac4-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="bdac4-112">Операция с $n $ Кубитс будет проверена.</span><span class="sxs-lookup"><span data-stu-id="bdac4-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit--is-adj"></a><span data-ttu-id="bdac4-113">Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="bdac4-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="bdac4-114">Операция ссылки на $n $ Кубитс `givenU` для сравнения с.</span><span class="sxs-lookup"><span data-stu-id="bdac4-114">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bdac4-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bdac4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="bdac4-116">Ссылки</span><span class="sxs-lookup"><span data-stu-id="bdac4-116">References</span></span>

<span data-ttu-id="bdac4-117">Основной частью состояний $ \кет {0} $, $ \кет {1} $, $ \кет{+} $ и $ \кет{и} $ является Chuang-Nielsen, описанный в [ *i. L. Чжуанский, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).</span><span class="sxs-lookup"><span data-stu-id="bdac4-117">The basis of states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ is the Chuang-Nielsen basis, described in [ *I. L. Chuang, M. A. Nielsen* ](https://arxiv.org/abs/quant-ph/9610001).</span></span>

## <a name="see-also"></a><span data-ttu-id="bdac4-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="bdac4-118">See Also</span></span>

- [<span data-ttu-id="bdac4-119">Microsoft. тактов. Diagnostics. Ассертоператионсекуалреференцед</span><span class="sxs-lookup"><span data-stu-id="bdac4-119">Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)