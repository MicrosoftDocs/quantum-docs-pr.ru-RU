---
uid: Microsoft.Quantum.Diagnostics.AssertOperationsEqualReferenced
title: Операция Ассертоператионсекуалреференцед
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertOperationsEqualReferenced
qsharp.summary: >-
  Given two operations, asserts that they act identically for all input states.

  This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers. Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated. This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.
ms.openlocfilehash: 045f00a720e9f4d2e6993c66ace44a81e192ff30
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853464"
---
# <a name="assertoperationsequalreferenced-operation"></a><span data-ttu-id="adb92-102">Операция Ассертоператионсекуалреференцед</span><span class="sxs-lookup"><span data-stu-id="adb92-102">AssertOperationsEqualReferenced operation</span></span>

<span data-ttu-id="adb92-103">Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="adb92-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="adb92-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="adb92-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="adb92-105">Учитывая две операции, утверждает, что они действуют одинаково для всех входных состояний.</span><span class="sxs-lookup"><span data-stu-id="adb92-105">Given two operations, asserts that they act identically for all input states.</span></span>

<span data-ttu-id="adb92-106">Это утверждение реализуется с помощью Чои – Жамиоłковски исоморфисм, чтобы уменьшить утверждение до одного из утверждений состояния кубит для двух регистров запутанными.</span><span class="sxs-lookup"><span data-stu-id="adb92-106">This assertion is implemented by using the Choi–Jamiołkowski isomorphism to reduce the assertion to one of a qubit state assertion on two entangled registers.</span></span>
<span data-ttu-id="adb92-107">Таким образом, для этой операции требуется только один вызов каждой проверяемой операции, но в два раза требуется выделить не больше Кубитс.</span><span class="sxs-lookup"><span data-stu-id="adb92-107">Thus, this operation needs only a single call to each operation being tested, but requires twice as many qubits to be allocated.</span></span>
<span data-ttu-id="adb92-108">Это утверждение можно использовать, чтобы убедиться, что оптимизированная версия операции действует аналогично его упрощенной реализации, или что операция, которая работает с диапазоном нетактовых входных данных, соглашается с известными случаями.</span><span class="sxs-lookup"><span data-stu-id="adb92-108">This assertion can be used to ensure, for instance, that an optimized version of an operation acts identically to its naïve implementation, or that an operation which acts on a range of non-quantum inputs agrees with known cases.</span></span>

```qsharp
operation AssertOperationsEqualReferenced (nQubits : Int, actual : (Qubit[] => Unit), expected : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a><span data-ttu-id="adb92-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="adb92-109">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="adb92-110">Нкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="adb92-110">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="adb92-111">Число Кубитс, которые должны быть переданы каждой операции.</span><span class="sxs-lookup"><span data-stu-id="adb92-111">Number of qubits to pass to each operation.</span></span>


### <a name="actual--qubit--unit"></a><span data-ttu-id="adb92-112">фактически: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица](xref:microsoft.quantum.lang-ref.unit)></span><span class="sxs-lookup"><span data-stu-id="adb92-112">actual : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="adb92-113">Проверяемая операция.</span><span class="sxs-lookup"><span data-stu-id="adb92-113">Operation to be tested.</span></span>


### <a name="expected--qubit--unit--is-adj"></a><span data-ttu-id="adb92-114">ожидалось: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) ></span><span class="sxs-lookup"><span data-stu-id="adb92-114">expected : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="adb92-115">Операция, определяющая ожидаемое поведение для тестируемой операции.</span><span class="sxs-lookup"><span data-stu-id="adb92-115">Operation defining the expected behavior for the operation under test.</span></span>



## <a name="output--unit"></a><span data-ttu-id="adb92-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="adb92-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="adb92-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="adb92-117">Remarks</span></span>

<span data-ttu-id="adb92-118">Для выполнения этой операции необходимо, чтобы моделирование операции выполнялось как аджоинтабле, чтобы обратная операция могла выполняться только с регистром целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="adb92-118">This operation requires that the operation modeling the expected behavior is adjointable, so that the inverse can be performed on the target register alone.</span></span>
<span data-ttu-id="adb92-119">Формально можно указать операцию преобразования, которая ослабляет это требование, но операция перестановки не является физически реализабле для произвольных операций такта и, таким образом, не включается в этот параметр.</span><span class="sxs-lookup"><span data-stu-id="adb92-119">Formally, one can specify a transpose operation, which relaxes this requirement, but the transpose operation is not in general physically realizable for arbitrary quantum operations and thus is not included here as an option.</span></span>