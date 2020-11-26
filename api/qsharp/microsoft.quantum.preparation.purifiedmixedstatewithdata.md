---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateWithData
title: Функция Пурифиедмикседстатевисдата
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateWithData
qsharp.summary: "Returns an operation that prepares a a purification of a given mixed\rstate, entangled with a register representing a given collection of data.\rA \"purified mixed state with data\" refers to a state of the form Σᵢ √\U0001D45Dᵢ |\U0001D456⟩ |\U0001D465ᵢ⟩ |garbageᵢ⟩,\rwhere each \U0001D465ᵢ is a bitstring encoding additional data associated with the register |\U0001D456⟩.\r\rSee https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion."
ms.openlocfilehash: c89ee8f5df58e5d6b154b67d2b39db208bc8a215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229959"
---
# <a name="purifiedmixedstatewithdata-function"></a><span data-ttu-id="28237-102">Функция Пурифиедмикседстатевисдата</span><span class="sxs-lookup"><span data-stu-id="28237-102">PurifiedMixedStateWithData function</span></span>

<span data-ttu-id="28237-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="28237-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="28237-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="28237-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="28237-105">Возвращает операцию, которая готовит пурификатион данного смешанного состояния, запутанными с регистром, представляющим данную коллекцию данных.</span><span class="sxs-lookup"><span data-stu-id="28237-105">Returns an operation that prepares a a purification of a given mixed state, entangled with a register representing a given collection of data.</span></span>
<span data-ttu-id="28237-106">"Пурифиед смешанное состояние с данными" относится к состоянию вида Σи √ PI | i ⟩ | XI ⟩ | гарбажеи ⟩, где каждое значение XI является битстринг кодировкой дополнительных данных, связанных с регистрацией | i ⟩.</span><span class="sxs-lookup"><span data-stu-id="28237-106">A "purified mixed state with data" refers to a state of the form Σᵢ √𝑝ᵢ |𝑖⟩ |𝑥ᵢ⟩ |garbageᵢ⟩, where each 𝑥ᵢ is a bitstring encoding additional data associated with the register |𝑖⟩.</span></span>

<span data-ttu-id="28237-107">Дополнительные https://arxiv.org/pdf/1805.03662.pdf?page=15 сведения см. в статье.</span><span class="sxs-lookup"><span data-stu-id="28237-107">See https://arxiv.org/pdf/1805.03662.pdf?page=15 for further discussion.</span></span>

```qsharp
function PurifiedMixedStateWithData (targetError : Double, coefficients : (Double, Bool[])[]) : Microsoft.Quantum.Preparation.MixedStatePreparation
```


## <a name="description"></a><span data-ttu-id="28237-108">Описание</span><span class="sxs-lookup"><span data-stu-id="28237-108">Description</span></span>

<span data-ttu-id="28237-109">Использует метод ПЗУ такта для представления заданной матрицы плотности, возвращая это представление в качестве операции подготовки состояния.</span><span class="sxs-lookup"><span data-stu-id="28237-109">Uses the Quantum ROM technique to represent a given density matrix, returning that representation as a state preparation operation.</span></span>

<span data-ttu-id="28237-110">В частности, при наличии списка коэффициентов "$N $" $ \ alpha_j $ и битстринг $ \век{КС}_j $, связанных с каждым из них, эта функция возвращает операцию, которая использует метод ПЗУ такта для подготовки приближения $ $ \бегин{алигн} \тилде\рхо = \сум_{j = 0} ^ {N-1} p_j \кет{ж}\бра{ж} \отимес \кет{\век{КС} _j} \bra{\vec{x}_j} \end{align} $ $ из смешанного состояния $ $ \begin{align} \rho = \sum_{j = 0} ^ {N-1} \ frac {| alpha_j |} {\ sum_k | \ alpha_k |} \кет{ж}\бра{ж} \отимес \кет{\век{КС} _j} \бра{\век{КС} _j}, \енд{алигн} $ $ где каждый $p _j $ является приближением к заданному коэффициенту $ \ alpha_j $ таким, что $ $ \бегин{алигн} \лефт | p_j-\фрак{| \ alpha_j |} {\ sum_k | \ alpha_k |} \ле \Фрак{\епсилон}{н} \енд{алигн} $ $ для каждого $j $.</span><span class="sxs-lookup"><span data-stu-id="28237-110">In particular, given a list of $N$ coefficients $\alpha_j$, and a bitstring $\vec{x}_j$ associated with each coefficient, this function returns an operation that uses the Quantum ROM technique to prepare an approximation $$ \begin{align} \tilde\rho = \sum_{j = 0}^{N - 1} p_j \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j} \end{align} $$ of the mixed state $$ \begin{align} \rho = \sum_{j = 0}^{N-1}\ frac{|alpha_j|}{\sum_k |\alpha_k|} \ket{j}\bra{j} \otimes \ket{\vec{x}_j}\bra{\vec{x}_j}, \end{align} $$ where each $p_j$ is an approximation to the given coefficient $\alpha_j$ such that $$ \begin{align} \left| p_j - \frac{ |\alpha_j| }{ \sum_k |\alpha_k| } \le \frac{\epsilon}{N} \end{align} $$ for each $j$.</span></span>

<span data-ttu-id="28237-111">Когда передается регистр индекса и регистр Кубитс мусора, первоначально находится в состоянии $ \кет {0} \ket{00\cdots 0}, возвращаемая операция готовит обе регистрации в пурификатион $ \тилде \рхо $, $ $ \бегин{алигн} \ sum_ {j = 0} ^ {N-1} \скрт{p_j} \кет{ж} \кет{\век{кс} _j} \кет{\текст{гарбаже} _j}, \end{align} $ $ например, при сбросе и отмене выделения для регистрации мусора нужная подготовка в рамках целевой ошибки $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="28237-111">When passed an index register and a register of garbage qubits, initially in the state $\ket{0} \ket{00\cdots 0}, the returned operation prepares both registers into the purification of $\tilde \rho$, $$ \begin{align} \sum_{j=0}^{N-1} \sqrt{p_j} \ket{j} \ket{\vec{x}_j} \ket{\text{garbage}_j}, \end{align} $$ such that resetting and deallocating the garbage register enacts the desired preparation to within the target error $\epsilon$.</span></span>

## <a name="input"></a><span data-ttu-id="28237-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="28237-112">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="28237-113">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="28237-113">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="28237-114">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="28237-114">The target error $\epsilon$.</span></span>


### <a name="coefficients--doublebool"></a><span data-ttu-id="28237-115">коэффициенты: ([Double](xref:microsoft.quantum.lang-ref.double),[bool](xref:microsoft.quantum.lang-ref.bool)[]) []</span><span class="sxs-lookup"><span data-stu-id="28237-115">coefficients : ([Double](xref:microsoft.quantum.lang-ref.double),[Bool](xref:microsoft.quantum.lang-ref.bool)[])[]</span></span>

<span data-ttu-id="28237-116">Массив коэффициентов $N $ с указанием вероятности базисных состояний, а также битстринг $ \век{КС} _j $, связанный с каждым подмножеством.</span><span class="sxs-lookup"><span data-stu-id="28237-116">Array of $N$ coefficients specifying the probability of basis states, along with the bitstring $\vec{x}_j$ associated with each coefficient.</span></span>
<span data-ttu-id="28237-117">Отрицательные числа $-\ alpha_j $ будут рассматриваться как положительные $ | \ alpha_j | $.</span><span class="sxs-lookup"><span data-stu-id="28237-117">Negative numbers $-\alpha_j$ will be treated as positive $|\alpha_j|$.</span></span>



## <a name="output--mixedstatepreparation"></a><span data-ttu-id="28237-118">Выходные данные: [микседстатепрепаратион](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span><span class="sxs-lookup"><span data-stu-id="28237-118">Output : [MixedStatePreparation](xref:Microsoft.Quantum.Preparation.MixedStatePreparation)</span></span>

<span data-ttu-id="28237-119">Операция, подготавливающая $ \тилде \рхо $ в качестве пурификатион к совместному индексу и регистрации мусора.</span><span class="sxs-lookup"><span data-stu-id="28237-119">An operation that prepares $\tilde \rho$ as a purification onto a joint index and garbage register.</span></span>

## <a name="remarks"></a><span data-ttu-id="28237-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28237-120">Remarks</span></span>

<span data-ttu-id="28237-121">Коэффициенты, предоставляемые для этой операции, нормализованы после 1-нормы, чтобы коэффициенты, которые всегда рассматриваются, описывают допустимое распределение вероятности по категориям.</span><span class="sxs-lookup"><span data-stu-id="28237-121">The coefficients provided to this operation are normalized following the 1-norm, such that the coefficients are always considered to describe a valid categorical probability distribution.</span></span>

## <a name="references"></a><span data-ttu-id="28237-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="28237-122">References</span></span>

- <span data-ttu-id="28237-123">Кодирование электронных спектра в тактовых каналах с помощью линейного T сложности Райан Баббуш, Крейг Гиднэй, Dominic W. Берри, (Nathan Виебе, Жаррод Астрид, Александру Палер, Остин Фаулер, Хартмут Невен https://arxiv.org/abs/1805.03662</span><span class="sxs-lookup"><span data-stu-id="28237-123">Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity Ryan Babbush, Craig Gidney, Dominic W. Berry, Nathan Wiebe, Jarrod McClean, Alexandru Paler, Austin Fowler, Hartmut Neven https://arxiv.org/abs/1805.03662</span></span>

## <a name="see-also"></a><span data-ttu-id="28237-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="28237-124">See Also</span></span>

- [<span data-ttu-id="28237-125">Microsoft. тактов. подготовка. Пурифиедмикседстате</span><span class="sxs-lookup"><span data-stu-id="28237-125">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)