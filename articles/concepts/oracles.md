---
title: Квантовые оракулы
description: Узнайте, как работать с и определять тактовые Oracle, операции с черной рамкой, которые используются в качестве входных данных для другого алгоритма.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
no-loc:
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
ms.openlocfilehash: 31e43940fc0607b15ccefcfae6be7122227b3d64
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630321"
---
# <a name="quantum-oracles"></a><span data-ttu-id="8a72e-103">Тактовые Oracle</span><span class="sxs-lookup"><span data-stu-id="8a72e-103">Quantum Oracles</span></span>

<span data-ttu-id="8a72e-104">$O Oracle $ — это "черная" операция, которая используется в качестве входных данных для другого алгоритма.</span><span class="sxs-lookup"><span data-stu-id="8a72e-104">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="8a72e-105">Часто такие операции определяются с помощью классической функции $f: \\ {0, 1 \\ } ^ n \то \\ {0, 1 \\ } ^ m $ , который принимает $n $ двоичные входные данные и создает $m $ разряд двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="8a72e-105">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="8a72e-106">Для этого рассмотрим определенный двоичный вход $x = (x_ {0 } , X_ {1 } , \дотс, X_ {n-1 } ) $.</span><span class="sxs-lookup"><span data-stu-id="8a72e-106">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="8a72e-107">Можно отметить кубит состояния как $ \кет { \век{КС } } = \кет{X_ {0 } } \отимес \кет{X_ {1 } } \отимес \кдотс \отимес \кет{X_ {n-1 } } $.</span><span class="sxs-lookup"><span data-stu-id="8a72e-107">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="8a72e-108">Мы можем сначала попытаться определить $O $ так, чтобы $O \ket {x } = \кет{ф (x)} $, но это потребует нескольких проблем.</span><span class="sxs-lookup"><span data-stu-id="8a72e-108">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="8a72e-109">Во-первых, $f $ может иметь разный размер входных и выходных данных ($n \не m $ ), поэтому применение $O $ изменит число Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="8a72e-109">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="8a72e-110">Во-вторых, даже если $n = m $ , функция может оказаться необратимой: если $f (x) = f (y) $ для некоторых $x \не y $ , то $O \ket {x } = o \ket {y } $, но $O ^ \дагжер o \ket {x } \не O ^ \дагжер o \ket {y } $.</span><span class="sxs-lookup"><span data-stu-id="8a72e-110">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="8a72e-111">Это означает, что мы не можем создать смежную операцию $O ^ \дагжер $ , и Oracle должны задать для них соседний объект.</span><span class="sxs-lookup"><span data-stu-id="8a72e-111">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="8a72e-112">Определение Oracle с учетом его воздействия на состояния вычислительных баз</span><span class="sxs-lookup"><span data-stu-id="8a72e-112">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="8a72e-113">Мы можем справиться с этими проблемами, добавив еще один регистр $m $ Кубитс для хранения нашего ответа.</span><span class="sxs-lookup"><span data-stu-id="8a72e-113">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="8a72e-114">Затем мы определим действие Oracle для всех вычислительных состояний: для всех $x \ин \\ {0, 1 \\ } ^ n $ и $y \ин \\ {0, 1 \\ } ^ m $ .</span><span class="sxs-lookup"><span data-stu-id="8a72e-114">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

<span data-ttu-id="8a72e-115">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-115">$$ \begin{align}</span></span>
    <span data-ttu-id="8a72e-116">O (\кет{КС } \отимес \кет{и } ) = \кет{КС } \отимес \кет{и \оплус f (x)}.</span><span class="sxs-lookup"><span data-stu-id="8a72e-116">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="8a72e-117">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-117">\end{align}</span></span>
$$

<span data-ttu-id="8a72e-118">Теперь $O = O ^ \дагжер $ by, поэтому мы разрешили обе предыдущие проблемы.</span><span class="sxs-lookup"><span data-stu-id="8a72e-118">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
> <span data-ttu-id="8a72e-119">Чтобы увидеть, что $O = O ^ {\дагжер } $, обратите внимание, что $O ^ 2 = \болдоне, $ начиная с $a \оплус b \оплус b = a $ для всех $a, b \ин \{ 0, 1 \} $.</span><span class="sxs-lookup"><span data-stu-id="8a72e-119">To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
> <span data-ttu-id="8a72e-120">В результате $O \кет{КС } \кет{и \оплус f (x)} = \кет{КС } \кет{и \оплус f (x) \оплус f (x)} = \кет{КС } \кет{и } $.</span><span class="sxs-lookup"><span data-stu-id="8a72e-120">As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="8a72e-121">Важно, что определение Oracle таким образом для каждого вычислительного состояния $ \кет{КС } \кет{и } $ также определяет, как $O $ действует для любого другого состояния.</span><span class="sxs-lookup"><span data-stu-id="8a72e-121">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="8a72e-122">Это происходит сразу же из того факта, что $O $ , как и все операции с тактовыми тактами, линейно в состоянии, в котором он работает.</span><span class="sxs-lookup"><span data-stu-id="8a72e-122">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="8a72e-123">Рассмотрим операцию Хадамард, например, определенную $H \ket{0 } = \кет { +} $ и $H \ket{1 } = \кет { -} $.</span><span class="sxs-lookup"><span data-stu-id="8a72e-123">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="8a72e-124">Если нам нужно понять, как $H $ действует на $ \кет { +} $, мы можем использовать этот $H $ линейный,</span><span class="sxs-lookup"><span data-stu-id="8a72e-124">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

<span data-ttu-id="8a72e-125">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-125">$$ \begin{align}</span></span>
<span data-ttu-id="8a72e-126">H \ket { +} & = \frac{1 } {\sqrt{2 } } H (\ket{0 } + \ket{1 } ) = \frac{1 } {\sqrt{2 } } (H \ket {0 } + H \ket {1 } ) \\ \\ & = \frac{1 } {\sqrt{2 } } (\кет { +} + \кет { -}) = \frac12 (\ket{0 } + \ket{1 } + \ket{0 } -\ket{1 } ) = \ket{0 } .</span><span class="sxs-lookup"><span data-stu-id="8a72e-126">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
<span data-ttu-id="8a72e-127">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-127">\end{align}</span></span>
$$

<span data-ttu-id="8a72e-128">В случае определения $O Oracle $ можно также использовать, что любое состояние $ \кет { \пси } $ on $n + m $ Кубитс можно записать как</span><span class="sxs-lookup"><span data-stu-id="8a72e-128">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

<span data-ttu-id="8a72e-129">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-129">$$ \begin{align}</span></span>
<span data-ttu-id="8a72e-130">\кет { \пси } & = \ sum_ {x \ин \\ {0, 1 \\ } ^ n, y \ин \\ {0, 1 \\ } ^ m } \алфа (x, y) \кет{КС } \кет{и}</span><span class="sxs-lookup"><span data-stu-id="8a72e-130">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
<span data-ttu-id="8a72e-131">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-131">\end{align}</span></span>
$$

<span data-ttu-id="8a72e-132">где $ \алфа: \\ {0, 1 \\ } ^ n \тимес \\ {0, 1 \\ } ^ m \то \масбб{к } $ представляет коэффициенты состояния $ \кет { \пси } $.</span><span class="sxs-lookup"><span data-stu-id="8a72e-132">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="8a72e-133">Таким образом, выражение</span><span class="sxs-lookup"><span data-stu-id="8a72e-133">Thus,</span></span>

<span data-ttu-id="8a72e-134">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-134">$$ \begin{align}</span></span>
<span data-ttu-id="8a72e-135">O \кет { \пси } & = O \ sum_ {x \ин \\ {0, 1 \\ } ^ n, y \ин \\ {0, 1 \\ } ^ m } \алфа (x, y) \кет{КС } \кет{и } \\ \\ & = \ sum_ {x \ин \\ {0, 1} \\ ^ n, y \ин \\ {0, 1 \\ } ^ m } \алфа (x, y) O \кет{КС } \кет{и } \\ \\ & = \ sum_ {x \ин \\ {0, 1 \\ } ^ n, y \ин \\ {0, 1 \\ } ^ m } \алфа (x, y) \кет{КС } \кет{и \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="8a72e-135">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="8a72e-136">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-136">\end{align}</span></span>
$$

## <a name="phase-oracles"></a><span data-ttu-id="8a72e-137">Этапы Oracle</span><span class="sxs-lookup"><span data-stu-id="8a72e-137">Phase oracles</span></span>
<span data-ttu-id="8a72e-138">Кроме того, можно закодировать $f $ в $O Oracle $ , применив _этап_ на основе входных данных для $O $ .</span><span class="sxs-lookup"><span data-stu-id="8a72e-138">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$.</span></span>
<span data-ttu-id="8a72e-139">Например, можно определить $O $ таким, что $ $ \бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-139">For instance, we might define $O$ such that $$ \begin{align}</span></span>
    <span data-ttu-id="8a72e-140">O \кет{КС } = (-1) ^ {f (x)} \кет{КС } .</span><span class="sxs-lookup"><span data-stu-id="8a72e-140">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
<span data-ttu-id="8a72e-141">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-141">\end{align}</span></span>
<span data-ttu-id="8a72e-142">$ $ Если стадия Oracle изначально работает над регистрацией в состоянии вычислительной базы $ \кет{КС } $, этот этап является глобальным и, следовательно, не является наблюдаемым.</span><span class="sxs-lookup"><span data-stu-id="8a72e-142">$$ If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="8a72e-143">Однако такой объект Oracle может быть очень мощным ресурсом, если он применяется к крайнему положению или управляемой операции.</span><span class="sxs-lookup"><span data-stu-id="8a72e-143">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="8a72e-144">Например, рассмотрим этап оркале $O _f $ для $f функции с одним кубит $ .</span><span class="sxs-lookup"><span data-stu-id="8a72e-144">For example, consider a phase orcale $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="8a72e-145">Затем $ $ \бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-145">Then, $$ \begin{align}</span></span>
    <span data-ttu-id="8a72e-146">O_f \кет { +} & = O_f (\ket{0 } + \ket{1 } )/\sqrt{2 } \\ \\ & = ((-1) ^ {f (0)} \ket{0 } + (-1) ^ {f (1)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} (\ket{0 } + (-1) ^ {f (1)-f (0)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \кет { +}.</span><span class="sxs-lookup"><span data-stu-id="8a72e-146">O_f \ket{+} & = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\ & = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
<span data-ttu-id="8a72e-147">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="8a72e-147">\end{align}</span></span>
$$

<span data-ttu-id="8a72e-148">В общем, оба представления Oracle можно расширить, чтобы представить классические функции, которые возвращают реальные числа, а не только один бит.</span><span class="sxs-lookup"><span data-stu-id="8a72e-148">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="8a72e-149">Выбор наилучшего способа реализации Oracle зависит сильно от того, как эта база данных Oracle будет использоваться в рамках данного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="8a72e-149">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="8a72e-150">Например, [алгоритм Deutsch-жозса](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) полагается на первую реализацию Oracle, тогда как [алгоритм Гровер](https://en.wikipedia.org/wiki/Grover's_algorithm) использует реализацию Oracle во втором случае.</span><span class="sxs-lookup"><span data-stu-id="8a72e-150">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="8a72e-151">Для получения дополнительных сведений мы рекомендуем обсуждение в [гилиéн *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="8a72e-151">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
