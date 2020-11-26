---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Операция Ассертоператионсекуалреференцед
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: 59c0fa72c9ca8f3bc512b6ed674fd73babc57f84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202317"
---
# <a name="assertoperationsequalreferenced-operation"></a><span data-ttu-id="79225-102">Операция Ассертоператионсекуалреференцед</span><span class="sxs-lookup"><span data-stu-id="79225-102">AssertOperationsEqualReferenced operation</span></span>

<span data-ttu-id="79225-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="79225-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="79225-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="79225-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="79225-105">Учитывая две операции, утверждает, что они действуют одинаково для всех входных состояний.</span><span class="sxs-lookup"><span data-stu-id="79225-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="79225-106">Это утверждение реализуется с помощью Чои – Жамиоłковски исоморфисм, чтобы уменьшить утверждение до одного из утверждений состояния кубит для двух регистров запутанными.</span><span class="sxs-lookup"><span data-stu-id="79225-106">This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers.</span></span>
<span data-ttu-id="79225-107">Таким образом, для этой операции требуется только один вызов каждой проверяемой операции, но в два раза требуется выделить не больше Кубитс.</span><span class="sxs-lookup"><span data-stu-id="79225-107">Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated.</span></span>
<span data-ttu-id="79225-108">Это утверждение можно использовать, чтобы убедиться, что оптимизированная версия операции действует аналогично его упрощенной реализации, или что операция, которая работает с диапазоном нетактовых входных данных, соглашается с известными случаями.</span><span class="sxs-lookup"><span data-stu-id="79225-108">This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.</span></span>

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="79225-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="79225-109">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="79225-110">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="79225-110">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="79225-111">Число Кубитс, которые должны быть переданы каждой операции.</span><span class="sxs-lookup"><span data-stu-id="79225-111">Number of qubits to pass to each operation.</span></span>


### <a name="actual--qubit--unit"></a><span data-ttu-id="79225-112">фактически: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="79225-112">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="79225-113">Проверяемая операция.</span><span class="sxs-lookup"><span data-stu-id="79225-113">Operation to be tested.</span></span>


### <a name="expected--qubit--unit--is-adj"></a><span data-ttu-id="79225-114">ожидалось: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="79225-114">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="79225-115">Операция, определяющая ожидаемое поведение для тестируемой операции.</span><span class="sxs-lookup"><span data-stu-id="79225-115">Operation defining the expected behavior for the operation under test.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79225-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79225-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="79225-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79225-117">Remarks</span></span>

<span data-ttu-id="79225-118">Для выполнения этой операции необходимо, чтобы моделирование операции выполнялось как аджоинтабле, чтобы обратная операция могла выполняться только с регистром целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="79225-118">This operation requires that the operation modeling the expected behavior is adjointable, so that the inverse can be performed on the target register alone.</span></span>
<span data-ttu-id="79225-119">Формально можно указать операцию преобразования, которая ослабляет это требование, но операция перестановки не является физически реализабле для произвольных операций такта и, таким образом, не включается в этот параметр.</span><span class="sxs-lookup"><span data-stu-id="79225-119">Formally, one can specify a transpose operation, which relaxes this requirement, but the transpose operation is not in general physically realizable for arbitrary quantum operations and thus is not included here as an option.</span></span>