---
<span data-ttu-id="6c385-101">Title: описание такта Oracle: Узнайте, как работать с тактовыми Oracle и определять тактовые генераторы, черные блочные операции, используемые в качестве входных данных для другого алгоритма.</span><span class="sxs-lookup"><span data-stu-id="6c385-101">title: Quantum oracles description: Learn how to work with and define quantum oracles, black box operations that are used as input to another algorithm.</span></span>
<span data-ttu-id="6c385-102">Автор: кгранаде UID: Microsoft. тактов. Основные сведения. oracles MS. author: чгранад MS. Дата: 07/11/2018 MS. Topic: статья No-Loc:</span><span class="sxs-lookup"><span data-stu-id="6c385-102">author: cgranade uid: microsoft.quantum.concepts.oracles ms.author: chgranad ms.date: 07/11/2018 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="6c385-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="6c385-103">"Q#"</span></span>
- <span data-ttu-id="6c385-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="6c385-104">"$$v"</span></span>
- <span data-ttu-id="6c385-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="6c385-105">"$$"</span></span>
- <span data-ttu-id="6c385-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="6c385-106">"$$"</span></span>
- <span data-ttu-id="6c385-107">"$"</span><span class="sxs-lookup"><span data-stu-id="6c385-107">"$"</span></span>
- <span data-ttu-id="6c385-108">"$"</span><span class="sxs-lookup"><span data-stu-id="6c385-108">"$"</span></span>
- <span data-ttu-id="6c385-109">"$"</span><span class="sxs-lookup"><span data-stu-id="6c385-109">"$"</span></span>
- <span data-ttu-id="6c385-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="6c385-110">"$$"</span></span>
- <span data-ttu-id="6c385-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="6c385-111">"\cdots"</span></span>
- <span data-ttu-id="6c385-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="6c385-112">"bmatrix"</span></span>
- <span data-ttu-id="6c385-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="6c385-113">"\ddots"</span></span>
- <span data-ttu-id="6c385-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="6c385-114">"\equiv"</span></span>
- <span data-ttu-id="6c385-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="6c385-115">"\sum"</span></span>
- <span data-ttu-id="6c385-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="6c385-116">"\begin"</span></span>
- <span data-ttu-id="6c385-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="6c385-117">"\end"</span></span>
- <span data-ttu-id="6c385-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="6c385-118">"\sqrt"</span></span>
- <span data-ttu-id="6c385-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="6c385-119">"\otimes"</span></span>
- <span data-ttu-id="6c385-120">"{"</span><span class="sxs-lookup"><span data-stu-id="6c385-120">"{"</span></span>
- <span data-ttu-id="6c385-121">"}"</span><span class="sxs-lookup"><span data-stu-id="6c385-121">"}"</span></span>
- <span data-ttu-id="6c385-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="6c385-122">"\text"</span></span>
- <span data-ttu-id="6c385-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="6c385-123">"\phi"</span></span>
- <span data-ttu-id="6c385-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="6c385-124">"\kappa"</span></span>
- <span data-ttu-id="6c385-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="6c385-125">"\psi"</span></span>
- <span data-ttu-id="6c385-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="6c385-126">"\alpha"</span></span>
- <span data-ttu-id="6c385-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="6c385-127">"\beta"</span></span>
- <span data-ttu-id="6c385-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="6c385-128">"\gamma"</span></span>
- <span data-ttu-id="6c385-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="6c385-129">"\delta"</span></span>
- <span data-ttu-id="6c385-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="6c385-130">"\omega"</span></span>
- <span data-ttu-id="6c385-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="6c385-131">"\bra"</span></span>
- <span data-ttu-id="6c385-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="6c385-132">"\ket"</span></span>
- <span data-ttu-id="6c385-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="6c385-133">"\boldone"</span></span>
- <span data-ttu-id="6c385-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="6c385-134">"\\\\"</span></span>
- <span data-ttu-id="6c385-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="6c385-135">"\\"</span></span>
- <span data-ttu-id="6c385-136">"="</span><span class="sxs-lookup"><span data-stu-id="6c385-136">"="</span></span>
- <span data-ttu-id="6c385-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="6c385-137">"\frac"</span></span>
- <span data-ttu-id="6c385-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="6c385-138">"\text"</span></span>
- <span data-ttu-id="6c385-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="6c385-139">"\mapsto"</span></span>
- <span data-ttu-id="6c385-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="6c385-140">"\dagger"</span></span>
- <span data-ttu-id="6c385-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="6c385-141">"\to"</span></span>
- <span data-ttu-id="6c385-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="6c385-142">"\begin{cases}"</span></span>
- <span data-ttu-id="6c385-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="6c385-143">"\end{cases}"</span></span>
- <span data-ttu-id="6c385-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="6c385-144">"\operatorname"</span></span>
- <span data-ttu-id="6c385-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="6c385-145">"\braket"</span></span>
- <span data-ttu-id="6c385-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="6c385-146">"\id"</span></span>
- <span data-ttu-id="6c385-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="6c385-147">"\expect"</span></span>
- <span data-ttu-id="6c385-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="6c385-148">"\defeq"</span></span>
- <span data-ttu-id="6c385-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="6c385-149">"\variance"</span></span>
- <span data-ttu-id="6c385-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="6c385-150">"\dd"</span></span>
- <span data-ttu-id="6c385-151">"&"</span><span class="sxs-lookup"><span data-stu-id="6c385-151">"&"</span></span>
- <span data-ttu-id="6c385-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="6c385-152">"\begin{align}"</span></span>
- <span data-ttu-id="6c385-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="6c385-153">"\end{align}"</span></span>
- <span data-ttu-id="6c385-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="6c385-154">"\Lambda"</span></span>
- <span data-ttu-id="6c385-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="6c385-155">"\lambda"</span></span>
- <span data-ttu-id="6c385-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="6c385-156">"\Omega"</span></span>
- <span data-ttu-id="6c385-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="6c385-157">"\mathrm"</span></span>
- <span data-ttu-id="6c385-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="6c385-158">"\left"</span></span>
- <span data-ttu-id="6c385-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="6c385-159">"\right"</span></span>
- <span data-ttu-id="6c385-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="6c385-160">"\qquad"</span></span>
- <span data-ttu-id="6c385-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="6c385-161">"\times"</span></span>
- <span data-ttu-id="6c385-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="6c385-162">"\big"</span></span>
- <span data-ttu-id="6c385-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="6c385-163">"\langle"</span></span>
- <span data-ttu-id="6c385-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="6c385-164">"\rangle"</span></span>
- <span data-ttu-id="6c385-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="6c385-165">"\bigg"</span></span>
- <span data-ttu-id="6c385-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="6c385-166">"\Big"</span></span>
- <span data-ttu-id="6c385-167">"|"</span><span class="sxs-lookup"><span data-stu-id="6c385-167">"|"</span></span>
- <span data-ttu-id="6c385-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="6c385-168">"\mathbb"</span></span>
- <span data-ttu-id="6c385-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="6c385-169">"\vec"</span></span>
- <span data-ttu-id="6c385-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="6c385-170">"\in"</span></span>
- <span data-ttu-id="6c385-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="6c385-171">"\texttt"</span></span>
- <span data-ttu-id="6c385-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="6c385-172">"\ne"</span></span>
- <span data-ttu-id="6c385-173">"<"</span><span class="sxs-lookup"><span data-stu-id="6c385-173">"<"</span></span>
- <span data-ttu-id="6c385-174">">"</span><span class="sxs-lookup"><span data-stu-id="6c385-174">">"</span></span>
- <span data-ttu-id="6c385-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="6c385-175">"\leq"</span></span>
- <span data-ttu-id="6c385-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="6c385-176">"\geq"</span></span>
- <span data-ttu-id="6c385-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="6c385-177">"~~"</span></span>
- <span data-ttu-id="6c385-178">"~"</span><span class="sxs-lookup"><span data-stu-id="6c385-178">"~"</span></span>
- <span data-ttu-id="6c385-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="6c385-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="6c385-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="6c385-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="6c385-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="6c385-181">"\_"</span></span>

---
# <a name="quantum-oracles"></a><span data-ttu-id="6c385-182">Тактовые Oracle</span><span class="sxs-lookup"><span data-stu-id="6c385-182">Quantum Oracles</span></span>

<span data-ttu-id="6c385-183">Oracle $ O $ — это «черная Box» операция, которая используется в качестве входных данных для другого алгоритма.</span><span class="sxs-lookup"><span data-stu-id="6c385-183">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="6c385-184">Часто такие операции определяются с помощью классической функции $ f: \\ { 0, 1 \\ } ^ n \to \\ { 0, 1 \\ } ^ m, $ которая принимает $ n- $ разрядный двоичный вход и создает $ $ двоичный выходной файл m-bit.</span><span class="sxs-lookup"><span data-stu-id="6c385-184">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="6c385-185">Для этого рассмотрим определенный двоичный вход $ x = (X_ { 0 } , X_ { 1 } , \дотс, X_ { n-1 } ) $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-185">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="6c385-186">Можно пометить кубит состояния как $ \ket { \vec { x } } = \ket { X_ { 0 } } \otimes \ket { X_ { 1 } } \otimes \cdots \otimes \ket { X_ { n-1 } } $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-186">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="6c385-187">Мы можем сначала попытаться определить $ o $ так, что $ o \ket { x } = \ket { f (x) } $ , но это потребует нескольких проблем.</span><span class="sxs-lookup"><span data-stu-id="6c385-187">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="6c385-188">$Во-первых, f $ может иметь разный размер входных и выходных данных ( $ n \ne m $ ), поэтому применение $ O $ приведет к изменению числа Кубитс в регистре.</span><span class="sxs-lookup"><span data-stu-id="6c385-188">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="6c385-189">Во-вторых, даже если $ n = m $ функция может оказаться необратимой: Если $ f (x) = f (y) $ для некоторых $ x \ne y $ , то $ o \ket { x } = o y, \ket { } $ но $ o ^ \dagger o \ket { x } \ne o ^ \dagger o \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-189">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="6c385-190">Это означает, что мы не сможем создать смежную операцию $ O ^ \dagger $ , и для Oracle необходимо задать для них смежное значение.</span><span class="sxs-lookup"><span data-stu-id="6c385-190">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="6c385-191">Определение Oracle с учетом его воздействия на состояния вычислительных баз</span><span class="sxs-lookup"><span data-stu-id="6c385-191">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="6c385-192">Мы можем справиться с этими проблемами, поставляя второй регистр $ m $ Кубитс для хранения нашего ответа.</span><span class="sxs-lookup"><span data-stu-id="6c385-192">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="6c385-193">Затем мы определим воздействие Oracle на все состояния вычислительных операций: для всех $ x \in \\ { 0, 1 \\ } ^ n $ и $ y \in \\ { 0, 1 \\ } ^ m $</span><span class="sxs-lookup"><span data-stu-id="6c385-193">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

$$
\begin{align}
    <span data-ttu-id="6c385-194">O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \оплус f (x) } .</span><span class="sxs-lookup"><span data-stu-id="6c385-194">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

<span data-ttu-id="6c385-195">Теперь $ = \dagger $ назначением "o o ^ by", мы разрешили обе предыдущие проблемы.</span><span class="sxs-lookup"><span data-stu-id="6c385-195">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
<span data-ttu-id="6c385-196">>Чтобы увидеть, что o $ = o ^ { \dagger } $ , обратите внимание, что $ o ^ 2 = \boldone $ с $ \оплус b \оплус = a $ для всех $ a, b \in \: :: un-Loc ({)::: 0, 1 \: :: No-Loc (})::: $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-196">> To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
<span data-ttu-id="6c385-197">>В результате $ O \ket { x } \ket { y \оплус f (x) } = \ket { x } \ket { y \оплус f (x) \оплус f (x) } = \ket { x } \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-197">> As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="6c385-198">Важно, что определение Oracle таким образом для каждого вычислительного состояния $ \ket { x } \ket { y } $ также определяет, как операция $ O $ действует для любого другого состояния.</span><span class="sxs-lookup"><span data-stu-id="6c385-198">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="6c385-199">Это происходит сразу же из того факта, что $ $ операция O, как и все операции над тактами, линейная в состоянии, в котором он работает.</span><span class="sxs-lookup"><span data-stu-id="6c385-199">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="6c385-200">Рассмотрим операцию хадамард, например, которая определяется в $ h \ket { 0 } = \ket { + } $ и $ h \ket { 1 } = \ket { - } $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-200">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="6c385-201">Если нам нужно понять, как $ $ работает h $ \ket { + } $ , мы можем использовать этот $ h $ линейный,</span><span class="sxs-lookup"><span data-stu-id="6c385-201">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

$$
\begin{align}
<span data-ttu-id="6c385-202">H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\</span><span class="sxs-lookup"><span data-stu-id="6c385-202">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\</span></span>
           <span data-ttu-id="6c385-203">&= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .</span><span class="sxs-lookup"><span data-stu-id="6c385-203">& = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
\end{align}
$$

<span data-ttu-id="6c385-204">В случае определения нашего Oracle $ O можно также $ использовать, чтобы любое состояние $ \ket { \psi } $ в $ n + m $ Кубитс можно было написать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6c385-204">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

$$
\begin{align}
<span data-ttu-id="6c385-205">\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}</span><span class="sxs-lookup"><span data-stu-id="6c385-205">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
\end{align}
$$

<span data-ttu-id="6c385-206">где $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C } $ — коэффициенты состояния $ \ket { \psi } $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-206">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="6c385-207">Таким образом, выражение</span><span class="sxs-lookup"><span data-stu-id="6c385-207">Thus,</span></span>

$$
\begin{align}
<span data-ttu-id="6c385-208">O \ket { \psi } & = o \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) O \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\</span><span class="sxs-lookup"><span data-stu-id="6c385-208">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\</span></span>
             <span data-ttu-id="6c385-209">&= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \оплус f (x) } .</span><span class="sxs-lookup"><span data-stu-id="6c385-209">& = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

## <a name="phase-oracles"></a><span data-ttu-id="6c385-210">Этапы Oracle</span><span class="sxs-lookup"><span data-stu-id="6c385-210">Phase oracles</span></span>
<span data-ttu-id="6c385-211">Кроме того, можно закодировать $ f $ в Oracle $ O $ , применив _этап_ на основе входных данных для $ O $ . Например, можно определить $ O $ таким, что $$</span><span class="sxs-lookup"><span data-stu-id="6c385-211">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$. For instance, we might define $O$ such that $$</span></span>
\begin{align}
    <span data-ttu-id="6c385-212">O \ket { x } = (-1) ^ { f (x) } \ket { x } .</span><span class="sxs-lookup"><span data-stu-id="6c385-212">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
\end{align}
$$
<span data-ttu-id="6c385-213">Если стадия Oracle изначально работает над регистром в вычислительном уровне $ \ket { x } $ , этот этап является глобальным и, следовательно, не является наблюдаемым.</span><span class="sxs-lookup"><span data-stu-id="6c385-213">If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="6c385-214">Однако такой объект Oracle может быть очень мощным ресурсом, если он применяется к крайнему положению или управляемой операции.</span><span class="sxs-lookup"><span data-stu-id="6c385-214">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="6c385-215">Например, рассмотрим фазу $ O_f Oracle $ для одной кубит функции $ f $ .</span><span class="sxs-lookup"><span data-stu-id="6c385-215">For example, consider a phase oracle $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="6c385-216">Этого $$</span><span class="sxs-lookup"><span data-stu-id="6c385-216">Then, $$</span></span>
\begin{align}
    <span data-ttu-id="6c385-217">O_f \ket{+}</span><span class="sxs-lookup"><span data-stu-id="6c385-217">O_f \ket{+}</span></span>
        <span data-ttu-id="6c385-218">&=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="6c385-218">& = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="6c385-219">&=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="6c385-219">& = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="6c385-220">&=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="6c385-220">& = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="6c385-221">&=(-1) ^ { f (0) } Z ^ { f (0)-f (1) } \ket { + } .</span><span class="sxs-lookup"><span data-stu-id="6c385-221">& = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
\end{align}
$$

<span data-ttu-id="6c385-222">В общем, оба представления Oracle можно расширить, чтобы представить классические функции, которые возвращают реальные числа, а не только один бит.</span><span class="sxs-lookup"><span data-stu-id="6c385-222">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="6c385-223">Выбор наилучшего способа реализации Oracle зависит сильно от того, как эта база данных Oracle будет использоваться в рамках данного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="6c385-223">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="6c385-224">Например, [алгоритм Deutsch-жозса](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) полагается на первую реализацию Oracle, тогда как [алгоритм Гровер](https://en.wikipedia.org/wiki/Grover's_algorithm) использует реализацию Oracle во втором случае.</span><span class="sxs-lookup"><span data-stu-id="6c385-224">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="6c385-225">Для получения дополнительных сведений мы рекомендуем обсуждение в [гилиéн *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="6c385-225">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
