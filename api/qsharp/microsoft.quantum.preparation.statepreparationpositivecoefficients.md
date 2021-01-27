---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Функция СтатепрепаратионпоситивекоеффиЦиентс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  > [!WARNING]

  > StatePreparationPositiveCoefficients has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.


  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 081541d93bf853fa0de1573038dc00c296432281
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855843"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="a9bf6-102">Функция СтатепрепаратионпоситивекоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="a9bf6-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="a9bf6-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="a9bf6-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="a9bf6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a9bf6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="a9bf6-105">СтатепрепаратионпоситивекоеффиЦиентс является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-105">StatePreparationPositiveCoefficients has been deprecated.</span></span> <span data-ttu-id="a9bf6-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD>.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateD> instead.</span></span>

<span data-ttu-id="a9bf6-107">Возвращает операцию, которая готовит заданное состояние такта.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-107">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="a9bf6-108">Возвращаемая операция, $U $, подготавливает произвольное состояние такта $ \ alpha_j \же $0 из $n $-кубит вычислительного состояния $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-108">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="a9bf6-109">Действие U для вновь выделенной регистрации задается параметром $ $ \бегин{алигн} U \ket{0\cdots 0} = \кет{\пси} = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \кет{ж}}{\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-109">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="a9bf6-110">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="a9bf6-110">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="a9bf6-111">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a9bf6-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="a9bf6-112">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a9bf6-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a9bf6-113">Массив до $2 ^ n $ коэффициенты $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-113">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="a9bf6-114">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit--is-adj--ctl"></a><span data-ttu-id="a9bf6-115">Выходные данные [](xref:Microsoft.Quantum.Arithmetic.LittleEndian) : => [единица](xref:microsoft.quantum.lang-ref.unit) литтлиндиан — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="a9bf6-115">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a9bf6-116">Единая операция подготовки состояния $U $.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-116">A state-preparation unitary operation $U$.</span></span>

## <a name="example"></a><span data-ttu-id="a9bf6-117">Пример</span><span class="sxs-lookup"><span data-stu-id="a9bf6-117">Example</span></span>

<span data-ttu-id="a9bf6-118">Следующий фрагмент кода готовит состояние такта $ \кет{\пси} = \ sqrt {1/8} \ Сисакет {0} + \ sqrt {7/8} \ Сисакет {2} $ в регистре кубит `qubitsLE` .</span><span class="sxs-lookup"><span data-stu-id="a9bf6-118">The following snippet prepares the quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{2}$ in the qubit register `qubitsLE`.</span></span>

```qsharp
let amplitudes = [Sqrt(0.125), 0.0, Sqrt(0.875), 0.0];
let op = StatePreparationPositiveCoefficients(amplitudes);
using (qubits = Qubit[2]) {
    let qubitsLE = LittleEndian(qubits);
    op(qubitsLE);
}
```

## <a name="remarks"></a><span data-ttu-id="a9bf6-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="a9bf6-119">Remarks</span></span>

<span data-ttu-id="a9bf6-120">Отрицательные коэффициенты ввода $ \ alpha_j < $0 будут рассматриваться как положительные со значением $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-120">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="a9bf6-121">`coefficients` будет дополнен элементами $ \ alpha_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="a9bf6-121">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>