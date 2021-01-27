---
uid: Microsoft.Quantum.Preparation.PurifiedMixedState
title: Функция Пурифиедмикседстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedState
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed state.\rA \"purified mixed state\" refers to states of the form |ψ⟩ = Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |garbageᵢ⟩ specified by a vector of\rcoefficients {\U0001D45Dᵢ}. States of this form can be reduced to mixed states ρ ≔ \U0001D45Dᵢ |\U0001D456⟩⟨\U0001D456| by tracing over the \"garbage\"\rregister (that is, a mixed state that is diagonal in the computational basis).\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: 594a1d9fa674e457ab88072ade4198283b677af6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854308"
---
# <a name="purifiedmixedstate-function"></a><span data-ttu-id="4b8ba-102">Функция Пурифиедмикседстате</span><span class="sxs-lookup"><span data-stu-id="4b8ba-102">PurifiedMixedState function</span></span>

<span data-ttu-id="4b8ba-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="4b8ba-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="4b8ba-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4b8ba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4b8ba-105">Возвращает операцию, которая готовит пурификатион данного смешанного состояния.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-105">Returns an operation that prepares a a purification of a given mixed state.</span></span>
<span data-ttu-id="4b8ba-106">"Пурифиед смешанное состояние" относится к состояниям вида | ψ ⟩ = Σи √ PI | i ⟩ | гарбажеи ⟩, указанным вектором коэффициентов {PI}.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-106">A "purified mixed state" refers to states of the form |ψ⟩ = Σᵢ √𝑝ᵢ |𝑖⟩ |garbageᵢ⟩ specified by a vector of coefficients {𝑝ᵢ}.</span></span> <span data-ttu-id="4b8ba-107">Состояния этой формы можно сократить до смешанных состояний p ≔ PI | i ⟩ ⟨ i | Трассировка по регистру «мусора» (то есть смешанному состоянию, который является диагональным по диагонали).</span><span class="sxs-lookup"><span data-stu-id="4b8ba-107">States of this form can be reduced to mixed states ρ ≔ 𝑝ᵢ |𝑖⟩⟨𝑖| by tracing over the "garbage" register (that is, a mixed state that is diagonal in the computational basis).</span></span>

<span data-ttu-id="4b8ba-108">Дополнительные https://arxiv.org/pdf/1805.03662.pdf?page=15 сведения см. в статье.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-108">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedState (targetError : Double, coefficients : Double[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="4b8ba-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4b8ba-109">Description</span></span>

<span data-ttu-id="4b8ba-110">Использует метод ПЗУ такта для представления заданной матрицы плотности, возвращая это представление в качестве операции подготовки состояния.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-110">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="4b8ba-111">В частности, при наличии списка коэффициентов $N $ $ \ alpha_j $ эта функция возвращает операцию, которая использует метод ПЗУ такта для подготовки приближения $ $ \бегин{алигн} \тилде\рхо = \ sum_ {j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} \енд{алигн} $ $ смешанного состояния $ $ \бегин{алигн} \рхо = \ sum_ {j = 0} ^ {N-1} \ фрак {| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж}, \енд{алигн} $ $, где каждый $p _j $ является приближением к заданному коэффициенту $ \ alpha_j $ таким, что $ $ \бегин{алигн} \лефт | p_j-\фрак{| \ alpha_j |} {\ sum_k | \ alpha_k |} \ле \Фрак{\епсилон}{н} \енд{алигн} $ $ для каждого $j $.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-111">In particular, given a list of $N$ coefficients $\alpha_j$, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="4b8ba-112">При передаче регистра индекса и регистрации кубитса мусора изначально в состоянии $ \кет {0} \ket{00\cdots 0} возвращаемая операция готовит оба регистра в пурификатион $ \тилде \рхо $, $ $ \бегин{алигн} \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж}\кет{\текст{гарбаже} _j}, \end{align} $ $, что сброс и освобождение регистрации мусора приводит к тому, что нужная подготовка в рамках целевой ошибки $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-112">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j}\ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="4b8ba-113">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4b8ba-113">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="4b8ba-114">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4b8ba-114">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="4b8ba-115">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-115">The target error $\epsilon$.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="4b8ba-116">коэффициенты: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="4b8ba-116">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="4b8ba-117">Массив коэффициентов $N $ с указанием вероятности базисных состояний.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-117">Array of $N$ coefficients specifying the probability of basis states.</span></span>
<span data-ttu-id="4b8ba-118">Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-118">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="4b8ba-119">Выходные данные: [микседстатепрепаратион](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="4b8ba-119">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="4b8ba-120">Операция, подготавливающая $ \тилде \рхо $ в качестве пурификатион к совместному индексу и регистрации мусора.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-120">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="example"></a><span data-ttu-id="4b8ba-121">Пример</span><span class="sxs-lookup"><span data-stu-id="4b8ba-121">Example</span></span>

<span data-ttu-id="4b8ba-122">Следующий фрагмент кода подготавливает пурификатион из $3 $-кубит State $ \рхо = \ sum_ {j = 0} ^ {4} \фрак{| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} $, где $ \век\алфа = (1.0, 2,0, 3,0, 4,0, 5,0) $, а целевая ошибка — $10 ^ {-3} $:</span><span class="sxs-lookup"><span data-stu-id="4b8ba-122">The following code snippet prepares an purification of the $3$-qubit state $\rho=\sum_{j=0}^{4}\frac{|alpha_j|}{\sum_k |\alpha_k|}\ket{j}\bra{j}$, where $\vec\alpha=(1.0, 2.0, 3.0, 4.0, 5.0)$, and the target error is $10^{-3}$:</span></span>

```qsharp
let coefficients = [1.0, 2.0, 3.0, 4.0, 5.0];
let targetError = 1e-3;
let purifiedState = PurifiedMixedState(targetError, coefficients);
using (indexRegister = Qubit[purifiedState::Requirements::NIndexQubits]) {
    using (garbageRegister = Qubit[purifiedState::Requirements::NGarbageQubits]) {
        purifiedState::Prepare(LittleEndian(indexRegister), new Qubit[0], garbageRegister);
    }
}
```

## <a name="remarks"></a><span data-ttu-id="4b8ba-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="4b8ba-123">Remarks</span></span>

<span data-ttu-id="4b8ba-124">Коэффициенты, предоставляемые для этой операции, нормализованы после 1-нормы, чтобы коэффициенты, которые всегда рассматриваются, описывают допустимое распределение вероятности по категориям.</span><span class="sxs-lookup"><span data-stu-id="4b8ba-124">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="4b8ba-125">Ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8ba-125">References</span></span>

- <span data-ttu-id="4b8ba-126">Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="4b8ba-126">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="4b8ba-127">См. также:</span><span class="sxs-lookup"><span data-stu-id="4b8ba-127">See Also</span></span>

- [<span data-ttu-id="4b8ba-128">Microsoft. тактов. подготовка. Пурифиедмикседстатевисдата</span><span class="sxs-lookup"><span data-stu-id="4b8ba-128">Microsoft.Quantum.Preparation.PurifiedMixedStateWithData</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedStateWithData)