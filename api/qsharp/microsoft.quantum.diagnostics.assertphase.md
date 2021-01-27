---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Операция Ассертфасе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830082"
---
# <a name="assertphase-operation"></a><span data-ttu-id="fffcd-102">Операция Ассертфасе</span><span class="sxs-lookup"><span data-stu-id="fffcd-102">AssertPhase operation</span></span>

<span data-ttu-id="fffcd-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="fffcd-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="fffcd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fffcd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fffcd-105">Утверждает, что фаза равного пресостояния перестановки имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="fffcd-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="fffcd-106">Описание</span><span class="sxs-lookup"><span data-stu-id="fffcd-106">Description</span></span>

<span data-ttu-id="fffcd-107">Эта операция подтверждает, что фаза $ \фи $ состояния такта, которая может быть выражена как $ \фрак{е ^ {i t}} {\скрт {2} } (e ^ {и\фи} \ Сисакет {0} + e ^ {-и\фи} \ Сисакет {1} ) $ для некоторых произвольных реальных $t $ имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="fffcd-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="fffcd-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fffcd-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="fffcd-109">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fffcd-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fffcd-110">Ожидаемое значение $ \фи \ин (-\пи, \пи] $.</span><span class="sxs-lookup"><span data-stu-id="fffcd-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="fffcd-111">Кубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fffcd-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fffcd-112">Кубит, в котором хранится ожидаемое состояние.</span><span class="sxs-lookup"><span data-stu-id="fffcd-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="fffcd-113">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fffcd-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fffcd-114">Абсолютная погрешность разности между фактическим и ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="fffcd-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fffcd-115">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fffcd-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="fffcd-116">Пример</span><span class="sxs-lookup"><span data-stu-id="fffcd-116">Example</span></span>

<span data-ttu-id="fffcd-117">Следующее утверждение выполнено: `qubit` находится в состоянии $ \кет{\пси} = e ^ {i 0,5} \ sqrt {1/2} \ Сисакет {0} + e ^ {i 0,5} \ sqrt {1/2} \ Сисакет {1} $;</span><span class="sxs-lookup"><span data-stu-id="fffcd-117">The following assert succeeds: `qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.0,qubit,10e-10);`

<span data-ttu-id="fffcd-118">`qubit` находится в состоянии $ \кет{\пси} = e ^ {i 0,5} \ sqrt {1/2} \ Сисакет {0} + e ^ {-i 0,5} \ sqrt {1/2} \ Сисакет {1} $;</span><span class="sxs-lookup"><span data-stu-id="fffcd-118">`qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{-i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.5,qubit,10e-10);`

<span data-ttu-id="fffcd-119">`qubit` находится в состоянии $ \кет{\пси} = e ^ {-i 2.2} \ корень {1/2} \ Сисакет {0} + e ^ {i 0,2} \ sqrt {1/2} \ Сисакет {1} $;</span><span class="sxs-lookup"><span data-stu-id="fffcd-119">`qubit` is in state $\ket{\psi}=e^{-i 2.2}\sqrt{1/2}\ket{0}+e^{i 0.2}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(-1.2,qubit,10e-10);`