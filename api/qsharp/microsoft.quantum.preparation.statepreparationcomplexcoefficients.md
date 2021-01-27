---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: Функция СтатепрепаратионкомплекскоеффиЦиентс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationComplexCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: c16df0fe075b15cff745a6b7d5b79aac39c14d09
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856138"
---
# <a name="statepreparationcomplexcoefficients-function"></a><span data-ttu-id="80d1f-102">Функция СтатепрепаратионкомплекскоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="80d1f-102">StatePreparationComplexCoefficients function</span></span>

<span data-ttu-id="80d1f-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="80d1f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="80d1f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="80d1f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="80d1f-105">СтатепрепаратионкомплекскоеффиЦиентс является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="80d1f-105">StatePreparationComplexCoefficients has been deprecated.</span></span> <span data-ttu-id="80d1f-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP>.</span><span class="sxs-lookup"><span data-stu-id="80d1f-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="80d1f-107">Возвращает операцию, которая готовит определенное состояние такта.</span><span class="sxs-lookup"><span data-stu-id="80d1f-107">Returns an operation that prepares a specific quantum state.</span></span>

<span data-ttu-id="80d1f-108">Возвращенная операция $U $ подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительного состояния $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="80d1f-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="80d1f-109">Действие U для вновь выделенной регистрации задается параметром $ $ \бегин{алигн} У\кет {0... 0} = \кет{\пси} = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}}{\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="80d1f-109">The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}.</span></span>
<span data-ttu-id="80d1f-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="80d1f-110">\end{align} $$</span></span>

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="80d1f-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="80d1f-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="80d1f-112">коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="80d1f-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="80d1f-113">Массив до $2 ^ n $ сложных коэффициентов, представленных абсолютным значением и фазой $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="80d1f-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="80d1f-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="80d1f-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="80d1f-115">Выходные данные [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="80d1f-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="80d1f-116">Единая операция подготовки состояния $U $.</span><span class="sxs-lookup"><span data-stu-id="80d1f-116">A state-preparation unitary operation $U$.</span></span>

## <a name="example"></a><span data-ttu-id="80d1f-117">Пример</span><span class="sxs-lookup"><span data-stu-id="80d1f-117">Example</span></span>

<span data-ttu-id="80d1f-118">Следующий фрагмент подготавливает состояние такта $ \кет{\пси} = e ^ {i 0,1} \ sqrt {1/8} \ Сисакет {0} + \ sqrt {7/8} \ Сисакет {2} $ в регистре кубит `qubitsLE` .</span><span class="sxs-lookup"><span data-stu-id="80d1f-118">The following snippet prepares the quantum state $\ket{\psi}=e^{i 0.1}\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{2}$ in the qubit register `qubitsLE`.</span></span>

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let phases = [0.1, 0.0, 0.0, 0.0];
mutable complexNumbers = new ComplexPolar[4];
for (idx in 0..3) {
    set complexNumbers[idx] = ComplexPolar(amplitudes[idx], phases[idx]);
}
let op = StatePreparationComplexCoefficients(complexNumbers);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a><span data-ttu-id="80d1f-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="80d1f-119">Remarks</span></span>

<span data-ttu-id="80d1f-120">Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="80d1f-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="80d1f-121">`coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="80d1f-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>