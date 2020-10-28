---
uid: Microsoft.Quantum.Preparation.StatePreparationComplexCoefficients
title: Функция СтатепрепаратионкомплекскоеффиЦиентс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationComplexCoefficients
qsharp.summary: >-
  Returns an operation that prepares a specific quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}. \end{align} $$
ms.openlocfilehash: 02e3d2fcf21b5bb4ed1bf7aa931597f918a1d369
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732593"
---
# <a name="statepreparationcomplexcoefficients-function"></a><span data-ttu-id="8214c-102">Функция СтатепрепаратионкомплекскоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="8214c-102">StatePreparationComplexCoefficients function</span></span>

<span data-ttu-id="8214c-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="8214c-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="8214c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8214c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8214c-105">Возвращает операцию, которая готовит определенное состояние такта.</span><span class="sxs-lookup"><span data-stu-id="8214c-105">Returns an operation that prepares a specific quantum state.</span></span>

<span data-ttu-id="8214c-106">Возвращенная операция $U $ подготавливает произвольное состояние такта $ \кет{\пси} $ с сложными коэффициентами $r _j e ^ {i t_j} $ из $n $-кубит вычислительного состояния $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="8214c-106">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="8214c-107">Действие U для вновь выделенной регистрации задается параметром $ $ \бегин{алигн} У\кет {0... 0} = \кет{\пси} = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \кет{ж}}{\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="8214c-107">The action of U on a newly-allocated register is given by $$ \begin{align} U\ket{0...0}=\ket{\psi}=\frac{\sum_{j=0}^{2^n-1}r_j e^{i t_j}\ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|r_j|^2}}.</span></span>
<span data-ttu-id="8214c-108">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="8214c-108">\end{align} $$</span></span>

```qsharp
function StatePreparationComplexCoefficients (coefficients : Microsoft.Quantum.Math.ComplexPolar[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="8214c-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="8214c-109">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="8214c-110">коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="8214c-110">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="8214c-111">Массив до $2 ^ n $ сложных коэффициентов, представленных абсолютным значением и фазой $ (r_j, t_j) $.</span><span class="sxs-lookup"><span data-stu-id="8214c-111">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="8214c-112">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="8214c-112">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit-adj--ctl"></a><span data-ttu-id="8214c-113">Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="8214c-113">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="8214c-114">Единая операция подготовки состояния $U $.</span><span class="sxs-lookup"><span data-stu-id="8214c-114">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="8214c-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="8214c-115">Remarks</span></span>

<span data-ttu-id="8214c-116">Отрицательные коэффициенты ввода $r _j < $0 будут рассматриваться как положительные значения $ | r_j | $.</span><span class="sxs-lookup"><span data-stu-id="8214c-116">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="8214c-117">`coefficients` будет дополнен элементами $ (r_j, t_j) = (0,0, 0,0) $, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="8214c-117">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>