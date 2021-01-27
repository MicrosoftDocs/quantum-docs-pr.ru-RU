---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Операция Ассертпробинт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843402"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="8d127-102">Операция Ассертпробинт</span><span class="sxs-lookup"><span data-stu-id="8d127-102">AssertProbInt operation</span></span>

<span data-ttu-id="8d127-103">Пространство имен: [Microsoft. тактов. арифметика](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8d127-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8d127-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d127-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d127-105">Утверждает, что вероятность определенного состояния регистра такта имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="8d127-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="8d127-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8d127-106">Description</span></span>

<span data-ttu-id="8d127-107">Учитывая $n $-кубит State $ \кет{\пси} = \сум ^ {2 ^ n-1} _ {j = 0} \ alpha_j \кет{ж} $, утверждает, что вероятность $ | \ alpha_j | ^ 2 $ из состояния $ \кет{ж} $, индексируемого $j $, имеет ожидаемое значение.</span><span class="sxs-lookup"><span data-stu-id="8d127-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="8d127-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8d127-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="8d127-109">Статеиндекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8d127-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8d127-110">Индекс $j $ из состояния $ \кет{ж} $, представленного `LittleEndian` регистром.</span><span class="sxs-lookup"><span data-stu-id="8d127-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="8d127-111">ожидалось: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8d127-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8d127-112">Ожидаемое значение $ | \ alpha_j | ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="8d127-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="8d127-113">Кубитс: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8d127-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8d127-114">Регистр кубит, в котором хранится $ \кет{\пси} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="8d127-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="8d127-115">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8d127-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8d127-116">Абсолютная погрешность разности между фактическим и ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="8d127-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8d127-117">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8d127-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="8d127-118">Пример</span><span class="sxs-lookup"><span data-stu-id="8d127-118">Example</span></span>

<span data-ttu-id="8d127-119">Предположим, что `qubits` регистр кодирует 3-кубитное состояние такта $ \кет{\пси} = \ sqrt {1/8} \ Сисакет {0} + \ sqrt {7/8} \ Сисакет {6} $ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="8d127-119">Suppose that the `qubits` register encodes a 3-qubit quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{6}$ in little-endian format.</span></span>
<span data-ttu-id="8d127-120">Это означает, что число состояний $ \кет {0} \екуив\кет {0} \кет {0} \кет {0} $ и $ \кет {6} \екуив\кет {0} \кет {1} \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="8d127-120">This means that the number states $\ket{0}\equiv\ket{0}\ket{0}\ket{0}$ and $\ket{6}\equiv\ket{0}\ket{1}\ket{1}$.</span></span> <span data-ttu-id="8d127-121">Затем выполняются следующие утверждения:</span><span class="sxs-lookup"><span data-stu-id="8d127-121">Then the following asserts succeed:</span></span>

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```