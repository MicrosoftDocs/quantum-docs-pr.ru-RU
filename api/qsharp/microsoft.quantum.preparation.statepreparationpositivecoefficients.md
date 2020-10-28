---
uid: Microsoft.Quantum.Preparation.StatePreparationPositiveCoefficients
title: Функция СтатепрепаратионпоситивекоеффиЦиентс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: StatePreparationPositiveCoefficients
qsharp.summary: >-
  Returns an operation that prepares the given quantum state.

  The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.

  The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}. \end{align} $$
ms.openlocfilehash: 39d961c71d231e7b51290f81c20c8c6b48c7e0b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732585"
---
# <a name="statepreparationpositivecoefficients-function"></a><span data-ttu-id="c6a9a-102">Функция СтатепрепаратионпоситивекоеффиЦиентс</span><span class="sxs-lookup"><span data-stu-id="c6a9a-102">StatePreparationPositiveCoefficients function</span></span>

<span data-ttu-id="c6a9a-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="c6a9a-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="c6a9a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6a9a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6a9a-105">Возвращает операцию, которая готовит заданное состояние такта.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-105">Returns an operation that prepares the given quantum state.</span></span>

<span data-ttu-id="c6a9a-106">Возвращаемая операция, $U $, подготавливает произвольное состояние такта $ \ alpha_j \же $0 из $n $-кубит вычислительного состояния $ \ket{0...0} $.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-106">The returned operation $U$ prepares an arbitrary quantum state $\ket{\psi}$ with positive coefficients $\alpha_j\ge 0$ from the $n$-qubit computational basis state $\ket{0...0}$.</span></span>

<span data-ttu-id="c6a9a-107">Действие U для вновь выделенной регистрации задается параметром $ $ \бегин{алигн} U \ket{0\cdots 0} = \кет{\пси} = \фрак{\ sum_ {j = 0} ^ {2 ^ n-1} \ alpha_j \кет{ж}}{\скрт{\ sum_ {j = 0} ^ {2 ^ n-1} | \ alpha_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-107">The action of U on a newly-allocated register is given by $$ \begin{align} U \ket{0\cdots 0} = \ket{\psi} = \frac{\sum_{j=0}^{2^n-1}\alpha_j \ket{j}}{\sqrt{\sum_{j=0}^{2^n-1}|\alpha_j|^2}}.</span></span>
<span data-ttu-id="c6a9a-108">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="c6a9a-108">\end{align} $$</span></span>

```qsharp
function StatePreparationPositiveCoefficients (coefficients : Double[]) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="c6a9a-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c6a9a-109">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="c6a9a-110">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c6a9a-110">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c6a9a-111">Массив до $2 ^ n $ коэффициенты $ \ alpha_j $.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-111">Array of up to $2^n$ coefficients $\alpha_j$.</span></span> <span data-ttu-id="c6a9a-112">Коэффициент $j $ TH индексирует числовое состояние $ \кет{ж} $, закодированное в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-112">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>



## <a name="output--littleendian--unit-adj--ctl"></a><span data-ttu-id="c6a9a-113">Выходные данные: [литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="c6a9a-113">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="c6a9a-114">Единая операция подготовки состояния $U $.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-114">A state-preparation unitary operation $U$.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a9a-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="c6a9a-115">Remarks</span></span>

<span data-ttu-id="c6a9a-116">Отрицательные коэффициенты ввода $ \ alpha_j < $0 будут рассматриваться как положительные со значением $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-116">Negative input coefficients $\alpha_j < 0$ will be treated as though positive with value $|\alpha_j|$.</span></span> <span data-ttu-id="c6a9a-117">`coefficients` будет дополнен элементами $ \ alpha_j = $0,0, если указано меньше $2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="c6a9a-117">`coefficients` will be padded with elements $\alpha_j = 0.0$ if fewer than $2^n$ are specified.</span></span>