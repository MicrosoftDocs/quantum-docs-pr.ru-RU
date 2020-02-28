---
title: Квантовые оракулы
description: Узнайте, как работать с и определять тактовые Oracle, операции с черной рамкой, которые используются в качестве входных данных для другого алгоритма.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
ms.openlocfilehash: 1d1d0b0903db8e994166c3e8a5798f70742a1c7e
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904933"
---
# <a name="quantum-oracles"></a><span data-ttu-id="27bda-103">Тактовые Oracle</span><span class="sxs-lookup"><span data-stu-id="27bda-103">Quantum Oracles</span></span>

<span data-ttu-id="27bda-104">Oracle $O $ — это «черная Box» операция, которая используется в качестве входных данных для другого алгоритма.</span><span class="sxs-lookup"><span data-stu-id="27bda-104">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="27bda-105">Часто такие операции определяются с помощью классической функции $f: \\{0, 1\\} ^ n \то \\{0, 1\\} ^ m $, который принимает $n $-разрядный двоичный ввод и создает $m $-разрядный двоичный вывод.</span><span class="sxs-lookup"><span data-stu-id="27bda-105">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="27bda-106">Для этого рассмотрите определенные двоичные входные данные $x = (x_{0}, x_{1}, \дотс, x_ {n-1}) $.</span><span class="sxs-lookup"><span data-stu-id="27bda-106">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="27bda-107">Можно отметить кубит состояния как $ \кет{\век{КС}} = \кет{x_{0}} \отимес \кет{x_{1}} \отимес \кдотс \отимес \кет{x_ {n-1}} $.</span><span class="sxs-lookup"><span data-stu-id="27bda-107">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="27bda-108">Мы можем сначала попытаться определить $O $, чтобы $O \кет{КС} = \кет{ф (x)} $, но это несколько проблем.</span><span class="sxs-lookup"><span data-stu-id="27bda-108">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="27bda-109">Во-первых, $f $ может иметь другой размер входных и выходных данных ($n \не m $), поэтому применение $O $ изменит число Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="27bda-109">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="27bda-110">Во-вторых, даже если $n = m $, функция может оказаться необратимой: если $f (x) = f (y) $ для некоторых $x \не y $, то $O \кет{КС} = О\кет {y} $, но $O ^ \дагжер О\кет {x} \не O ^ \дагжер О\кет {y} $.</span><span class="sxs-lookup"><span data-stu-id="27bda-110">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="27bda-111">Это означает, что мы не сможем создать смежную операцию $O ^ \дагжер $, и Oracle должны задать для них соседний объект.</span><span class="sxs-lookup"><span data-stu-id="27bda-111">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="27bda-112">Определение Oracle с учетом его воздействия на состояния вычислительных баз</span><span class="sxs-lookup"><span data-stu-id="27bda-112">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="27bda-113">Мы можем справиться с этими проблемами, поставляя второй регистр $m $ Кубитс для хранения нашего ответа.</span><span class="sxs-lookup"><span data-stu-id="27bda-113">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="27bda-114">Затем мы определим действие Oracle для всех вычислительных состояний: для всех $x \ин \\{0, 1\\} ^ n $ и $y \ин \\{0, 1\\} ^ m $,</span><span class="sxs-lookup"><span data-stu-id="27bda-114">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

<span data-ttu-id="27bda-115">$ $ \бегин{алигн} O (\кет{КС} \отимес \кет{и}) = \кет{КС} \отимес \кет{и \оплус f (x)}.</span><span class="sxs-lookup"><span data-stu-id="27bda-115">$$ \begin{align} O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="27bda-116">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="27bda-116">\end{align} $$</span></span>

<span data-ttu-id="27bda-117">Теперь $O = O ^ \дагжер $ by, поэтому мы разрешили обе предыдущие проблемы.</span><span class="sxs-lookup"><span data-stu-id="27bda-117">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
> <span data-ttu-id="27bda-118">Чтобы увидеть, что $O = O ^ {\дагжер} $, обратите внимание, что $O ^ 2 = \болдоне $ с $a \оплус b \оплус b = a $ для всех $a, b \ин \{0, 1\}$.</span><span class="sxs-lookup"><span data-stu-id="27bda-118">To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
> <span data-ttu-id="27bda-119">В результате $O \кет{КС} \кет{и \оплус f (x)} = \кет{КС} \кет{и \оплус f (x) \оплус f (x)} = \кет{КС} \кет{и} $.</span><span class="sxs-lookup"><span data-stu-id="27bda-119">As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="27bda-120">Важно, что определение Oracle таким образом для каждого вычислительного состояния $ \кет{КС}\кет{и} $ также определяет, как $O $ действует для любого другого состояния.</span><span class="sxs-lookup"><span data-stu-id="27bda-120">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="27bda-121">Это происходит сразу же из того факта, что $O $, как и все операции с тактами, линейное в состоянии, в котором он работает.</span><span class="sxs-lookup"><span data-stu-id="27bda-121">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="27bda-122">Рассмотрим операцию Хадамард, например, определенную с помощью $H \кет{0} = \кет{+} $ и $H \кет{1} = \кет{-}$.</span><span class="sxs-lookup"><span data-stu-id="27bda-122">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="27bda-123">Если нам нужно понять, как $H $ действует на $ \кет{+} $, мы можем использовать эту $H $ является линейной,</span><span class="sxs-lookup"><span data-stu-id="27bda-123">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

<span data-ttu-id="27bda-124">$ $ \бегин{алигн} Х\кет {+} & = \фрак{1}{\скрт{2}} H (\кет{0} + \кет{1}) = \фрак{1}{\скрт{2}} (Х\кет{0} + Х\кет{1}) \\\\ & = \фрак{1}{\скрт{2}} (\кет{+} + \кет{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0}-\ket{1}) = \ket{0}.</span><span class="sxs-lookup"><span data-stu-id="27bda-124">$$ \begin{align} H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
<span data-ttu-id="27bda-125">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="27bda-125">\end{align} $$</span></span>

<span data-ttu-id="27bda-126">В случае определения Oracle $O $ можно также использовать, что любое состояние $ \кет{\пси} $ on $n + m $ Кубитс можно записать как</span><span class="sxs-lookup"><span data-stu-id="27bda-126">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

<span data-ttu-id="27bda-127">$ $ \бегин{алигн} \кет{\пси} & = \ sum_ {x \ин \\{0, 1\\} ^ n, y \ин \\{0, 1\\} ^ m} \алфа (x, y) \кет{КС} \кет{и} \енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="27bda-127">$$ \begin{align} \ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \end{align} $$</span></span>

<span data-ttu-id="27bda-128">где $ \алфа: \\{0, 1\\} ^ n \тимес \\{0, 1\\} ^ m \то \Масбб{к} $ представляет коэффициенты состояния $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="27bda-128">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="27bda-129">Следовательно</span><span class="sxs-lookup"><span data-stu-id="27bda-129">Thus,</span></span>

<span data-ttu-id="27bda-130">$ $ \бегин{алигн} O \кет{\пси} & = O \ sum_ {x \ин \\{0, 1\\} ^ n, y \ин \\{0, 1\\} ^ m} \алфа (x, y) \кет{КС} \кет{и} \\\\ & = \ sum_ {x \ин \\{0, 1\\} ^ n, y \ин \\{0, 1\\} ^ m} \алфа (x, y) O \кет{КС} \кет{и} \\\\ & = \ sum_ {x \in \\{0, 1\\} ^ n , y \ин \\{0, 1\\} ^ m} \алфа (x, y) \кет{КС} \кет{и \оплус f (x)}.</span><span class="sxs-lookup"><span data-stu-id="27bda-130">$$ \begin{align} O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="27bda-131">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="27bda-131">\end{align} $$</span></span>

## <a name="phase-oracles"></a><span data-ttu-id="27bda-132">Этапы Oracle</span><span class="sxs-lookup"><span data-stu-id="27bda-132">Phase oracles</span></span>
<span data-ttu-id="27bda-133">Кроме того, можно закодировать $f $ в Oracle $O $, применив _этап_ на основе входных данных для $O $.</span><span class="sxs-lookup"><span data-stu-id="27bda-133">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$.</span></span>
<span data-ttu-id="27bda-134">Например, можно определить $O $ таким, что $ $ \бегин{алигн} O \кет{КС} = (-1) ^ {f (x)} \кет{КС}.</span><span class="sxs-lookup"><span data-stu-id="27bda-134">For instance, we might define $O$ such that $$ \begin{align} O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
<span data-ttu-id="27bda-135">\енд{алигн} $ $ Если стадия Oracle изначально работает над регистрацией в состоянии вычислительной базы $ \кет{КС} $, этот этап является глобальным и, следовательно, не является наблюдаемым.</span><span class="sxs-lookup"><span data-stu-id="27bda-135">\end{align} $$ If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="27bda-136">Однако такой объект Oracle может быть очень мощным ресурсом, если он применяется к крайнему положению или управляемой операции.</span><span class="sxs-lookup"><span data-stu-id="27bda-136">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="27bda-137">Например, рассмотрим этап оркале $O _f $ для одной функции кубит $f $.</span><span class="sxs-lookup"><span data-stu-id="27bda-137">For example, consider a phase orcale $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="27bda-138">Затем $ $ \бегин{алигн} O_f \кет{+} & = O_f (\кет{0} + \кет{1})/\скрт{2} \\\\ & = ((-1) ^ {f (0)} \кет{0} + (-1) ^ {f (1)} \кет{1})/\скрт{2} \\\\ & = (-1) ^ {f (0)} (\кет{0} + (-1) ^ {f (1)-f (0)} \кет{1})/\скрт{2} \\\\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \кет{+}.</span><span class="sxs-lookup"><span data-stu-id="27bda-138">Then, $$ \begin{align} O_f \ket{+} & = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\ & = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
<span data-ttu-id="27bda-139">\енд{алигн} $ $</span><span class="sxs-lookup"><span data-stu-id="27bda-139">\end{align} $$</span></span>

<span data-ttu-id="27bda-140">В общем, оба представления Oracle можно расширить, чтобы представить классические функции, которые возвращают реальные числа, а не только один бит.</span><span class="sxs-lookup"><span data-stu-id="27bda-140">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="27bda-141">Выбор наилучшего способа реализации Oracle зависит сильно от того, как эта база данных Oracle будет использоваться в рамках данного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="27bda-141">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="27bda-142">Например, [алгоритм Deutsch-жозса](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) полагается на первую реализацию Oracle, тогда как [алгоритм Гровер](https://en.wikipedia.org/wiki/Grover's_algorithm) использует реализацию Oracle во втором случае.</span><span class="sxs-lookup"><span data-stu-id="27bda-142">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="27bda-143">Для получения дополнительных сведений мы рекомендуем обсуждение в [гилиéн *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="27bda-143">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
