---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Операция Ассертпробинт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: a8e4217e18528adc0aa9923f1c0dcfb59e1d2488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731680"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="be25a-102">Операция Ассертпробинт</span><span class="sxs-lookup"><span data-stu-id="be25a-102">AssertProbInt operation</span></span>

<span data-ttu-id="be25a-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="be25a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="be25a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="be25a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="be25a-105">Утверждает, что вероятность определенного состояния регистра такта имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="be25a-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="be25a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="be25a-106">Description</span></span>

<span data-ttu-id="be25a-107">Учитывая $n $-кубит State $ \кет{\пси} = \сум ^ {2 ^ n-1} _ {j = 0} \ alpha_j \кет{ж} $, утверждает, что вероятность $ | \ alpha_j | ^ 2 $ из состояния $ \кет{ж} $, индексируемого $j $, имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="be25a-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="be25a-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="be25a-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="be25a-109">Статеиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="be25a-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="be25a-110">Индекс $j $ из состояния $ \кет{ж} $, представленного `LittleEndian` регистром.</span><span class="sxs-lookup"><span data-stu-id="be25a-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="be25a-111">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="be25a-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="be25a-112">Ожидаемое значение $ | \ alpha_j | ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="be25a-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="be25a-113">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="be25a-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="be25a-114">Регистр кубит, в котором хранится $ \кет{\пси} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="be25a-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="be25a-115">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="be25a-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="be25a-116">Абсолютная погрешность разности между фактическим и ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="be25a-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be25a-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be25a-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

