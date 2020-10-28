---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualInPlace
title: Операция Ассертоператионсекуалинплаце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualInPlace
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).

  This assertion uses $n$ qubits and requires multiple calls of the operations being compared.
ms.openlocfilehash: 407a139da816281346eb06849f81e91b83202653
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712975"
---
# <a name="assertoperationsequalinplace-operation"></a><span data-ttu-id="f5b6e-102">Операция Ассертоператионсекуалинплаце</span><span class="sxs-lookup"><span data-stu-id="f5b6e-102">AssertOperationsEqualInPlace operation</span></span>

<span data-ttu-id="f5b6e-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="f5b6e-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="f5b6e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f5b6e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f5b6e-105">Учитывая две операции, утверждает, что они действуют одинаково для всех входных состояний.</span><span class="sxs-lookup"><span data-stu-id="f5b6e-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="f5b6e-106">Это утверждение реализуется путем проверки действия операций во всех состояниях формы $V _0 \отимес... \отимес V_ {n-1} $, где $V _k $ является одним из состояний $ \кет {0} $, $ \кет {1} $, $ \кет{+} $ и $ \кет{и} $ (+ 1 Еиженстате of Паули Y).</span><span class="sxs-lookup"><span data-stu-id="f5b6e-106">This assertion is implemented by checking the action of the operations on all states of the form $V_0 \otimes ... \otimes V_{n-1}$, where $V_k$ is one of the states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ (+1 eigenstate of Pauli Y operator).</span></span>

<span data-ttu-id="f5b6e-107">Это утверждение использует $n $ Кубитс и требует нескольких вызовов сравниваемых операций.</span><span class="sxs-lookup"><span data-stu-id="f5b6e-107">This assertion uses $n$ qubits and requires multiple calls of the operations being compared.</span></span>

```qsharp
operation AssertOperationsEqualInPlace (nQubits : Int, givenU : (Qubit[] => Unit), expectedU : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="f5b6e-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f5b6e-108">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="f5b6e-109">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f5b6e-109">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f5b6e-110">Число Кубитс $n $, с которыми работают операции `givenU` `expectedU` .</span><span class="sxs-lookup"><span data-stu-id="f5b6e-110">The number of qubits $n$ that the operations `givenU` and `expectedU` operate on.</span></span>


### <a name="givenu--qubit--unit"></a><span data-ttu-id="f5b6e-111">Гивену: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="f5b6e-111">givenU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f5b6e-112">Операция с $n $ Кубитс будет проверена.</span><span class="sxs-lookup"><span data-stu-id="f5b6e-112">Operation on $n$ qubits to be checked.</span></span>


### <a name="expectedu--qubit--unit-adj"></a><span data-ttu-id="f5b6e-113">Експектеду: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода</span><span class="sxs-lookup"><span data-stu-id="f5b6e-113">expectedU : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="f5b6e-114">Операция ссылки на $n $ Кубитс `givenU` для сравнения с.</span><span class="sxs-lookup"><span data-stu-id="f5b6e-114">Reference operation on $n$ qubits that `givenU` is to be compared against.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f5b6e-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f5b6e-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="f5b6e-116">Ссылки</span><span class="sxs-lookup"><span data-stu-id="f5b6e-116">References</span></span>

<span data-ttu-id="f5b6e-117">Основной частью состояний $ \кет {0} $, $ \кет {1} $, $ \кет{+} $ и $ \кет{и} $ является Chuang-Nielsen, описанный в [ *i. L. Чжуанский, M. A. Nielsen*](https://arxiv.org/abs/quant-ph/9610001).</span><span class="sxs-lookup"><span data-stu-id="f5b6e-117">The basis of states $\ket{0}$, $\ket{1}$, $\ket{+}$ and $\ket{i}$ is the Chuang-Nielsen basis, described in [ *I. L. Chuang, M. A. Nielsen* ](https://arxiv.org/abs/quant-ph/9610001).</span></span>

## <a name="see-also"></a><span data-ttu-id="f5b6e-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="f5b6e-118">See Also</span></span>

- [<span data-ttu-id="f5b6e-119">Microsoft. тактов. Diagnostics. Ассертоператионсекуалреференцед</span><span class="sxs-lookup"><span data-stu-id="f5b6e-119">Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced)