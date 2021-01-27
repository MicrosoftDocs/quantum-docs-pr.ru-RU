---
<span data-ttu-id="92317-101">Title: векторы и матрицы в описании тактовых вычислений: Изучите основы работы с векторами и матрицами.</span><span class="sxs-lookup"><span data-stu-id="92317-101">title: Vectors and matrices in quantum computing description: Learn the basics of how to work with vectors and matrices.</span></span>
<span data-ttu-id="92317-102">Автор: Куантумвритер UID: Microsoft. тактов. Основные понятия. векторы MS. author: v-бенбра MS. Дата: 12/11/2017 МС. раздел: концептуальный No-Loc:</span><span class="sxs-lookup"><span data-stu-id="92317-102">author: QuantumWriter uid: microsoft.quantum.concepts.vectors ms.author: v-benbra ms.date: 12/11/2017 ms.topic: conceptual no-loc:</span></span>
- <span data-ttu-id="92317-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="92317-103">"Q#"</span></span>
- <span data-ttu-id="92317-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="92317-104">"$$v"</span></span>
- <span data-ttu-id="92317-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="92317-105">"$$"</span></span>
- <span data-ttu-id="92317-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="92317-106">"$$"</span></span>
- <span data-ttu-id="92317-107">"$"</span><span class="sxs-lookup"><span data-stu-id="92317-107">"$"</span></span>
- <span data-ttu-id="92317-108">"$"</span><span class="sxs-lookup"><span data-stu-id="92317-108">"$"</span></span>
- <span data-ttu-id="92317-109">"$"</span><span class="sxs-lookup"><span data-stu-id="92317-109">"$"</span></span>
- <span data-ttu-id="92317-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="92317-110">"$$"</span></span>
- <span data-ttu-id="92317-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="92317-111">"\cdots"</span></span>
- <span data-ttu-id="92317-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="92317-112">"bmatrix"</span></span>
- <span data-ttu-id="92317-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="92317-113">"\ddots"</span></span>
- <span data-ttu-id="92317-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="92317-114">"\equiv"</span></span>
- <span data-ttu-id="92317-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="92317-115">"\sum"</span></span>
- <span data-ttu-id="92317-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="92317-116">"\begin"</span></span>
- <span data-ttu-id="92317-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="92317-117">"\end"</span></span>
- <span data-ttu-id="92317-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="92317-118">"\sqrt"</span></span>
- <span data-ttu-id="92317-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="92317-119">"\otimes"</span></span>
- <span data-ttu-id="92317-120">"{"</span><span class="sxs-lookup"><span data-stu-id="92317-120">"{"</span></span>
- <span data-ttu-id="92317-121">"}"</span><span class="sxs-lookup"><span data-stu-id="92317-121">"}"</span></span>
- <span data-ttu-id="92317-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="92317-122">"\text"</span></span>
- <span data-ttu-id="92317-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="92317-123">"\phi"</span></span>
- <span data-ttu-id="92317-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="92317-124">"\kappa"</span></span>
- <span data-ttu-id="92317-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="92317-125">"\psi"</span></span>
- <span data-ttu-id="92317-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="92317-126">"\alpha"</span></span>
- <span data-ttu-id="92317-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="92317-127">"\beta"</span></span>
- <span data-ttu-id="92317-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="92317-128">"\gamma"</span></span>
- <span data-ttu-id="92317-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="92317-129">"\delta"</span></span>
- <span data-ttu-id="92317-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="92317-130">"\omega"</span></span>
- <span data-ttu-id="92317-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="92317-131">"\bra"</span></span>
- <span data-ttu-id="92317-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="92317-132">"\ket"</span></span>
- <span data-ttu-id="92317-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="92317-133">"\boldone"</span></span>
- <span data-ttu-id="92317-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="92317-134">"\\\\"</span></span>
- <span data-ttu-id="92317-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="92317-135">"\\"</span></span>
- <span data-ttu-id="92317-136">"="</span><span class="sxs-lookup"><span data-stu-id="92317-136">"="</span></span>
- <span data-ttu-id="92317-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="92317-137">"\frac"</span></span>
- <span data-ttu-id="92317-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="92317-138">"\text"</span></span>
- <span data-ttu-id="92317-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="92317-139">"\mapsto"</span></span>
- <span data-ttu-id="92317-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="92317-140">"\dagger"</span></span>
- <span data-ttu-id="92317-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="92317-141">"\to"</span></span>
- <span data-ttu-id="92317-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="92317-142">"\begin{cases}"</span></span>
- <span data-ttu-id="92317-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="92317-143">"\end{cases}"</span></span>
- <span data-ttu-id="92317-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="92317-144">"\operatorname"</span></span>
- <span data-ttu-id="92317-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="92317-145">"\braket"</span></span>
- <span data-ttu-id="92317-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="92317-146">"\id"</span></span>
- <span data-ttu-id="92317-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="92317-147">"\expect"</span></span>
- <span data-ttu-id="92317-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="92317-148">"\defeq"</span></span>
- <span data-ttu-id="92317-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="92317-149">"\variance"</span></span>
- <span data-ttu-id="92317-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="92317-150">"\dd"</span></span>
- <span data-ttu-id="92317-151">"&"</span><span class="sxs-lookup"><span data-stu-id="92317-151">"&"</span></span>
- <span data-ttu-id="92317-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="92317-152">"\begin{align}"</span></span>
- <span data-ttu-id="92317-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="92317-153">"\end{align}"</span></span>
- <span data-ttu-id="92317-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="92317-154">"\Lambda"</span></span>
- <span data-ttu-id="92317-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="92317-155">"\lambda"</span></span>
- <span data-ttu-id="92317-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="92317-156">"\Omega"</span></span>
- <span data-ttu-id="92317-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="92317-157">"\mathrm"</span></span>
- <span data-ttu-id="92317-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="92317-158">"\left"</span></span>
- <span data-ttu-id="92317-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="92317-159">"\right"</span></span>
- <span data-ttu-id="92317-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="92317-160">"\qquad"</span></span>
- <span data-ttu-id="92317-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="92317-161">"\times"</span></span>
- <span data-ttu-id="92317-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="92317-162">"\big"</span></span>
- <span data-ttu-id="92317-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="92317-163">"\langle"</span></span>
- <span data-ttu-id="92317-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="92317-164">"\rangle"</span></span>
- <span data-ttu-id="92317-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="92317-165">"\bigg"</span></span>
- <span data-ttu-id="92317-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="92317-166">"\Big"</span></span>
- <span data-ttu-id="92317-167">"|"</span><span class="sxs-lookup"><span data-stu-id="92317-167">"|"</span></span>
- <span data-ttu-id="92317-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="92317-168">"\mathbb"</span></span>
- <span data-ttu-id="92317-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="92317-169">"\vec"</span></span>
- <span data-ttu-id="92317-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="92317-170">"\in"</span></span>
- <span data-ttu-id="92317-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="92317-171">"\texttt"</span></span>
- <span data-ttu-id="92317-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="92317-172">"\ne"</span></span>
- <span data-ttu-id="92317-173">"<"</span><span class="sxs-lookup"><span data-stu-id="92317-173">"<"</span></span>
- <span data-ttu-id="92317-174">">"</span><span class="sxs-lookup"><span data-stu-id="92317-174">">"</span></span>
- <span data-ttu-id="92317-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="92317-175">"\leq"</span></span>
- <span data-ttu-id="92317-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="92317-176">"\geq"</span></span>
- <span data-ttu-id="92317-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="92317-177">"~~"</span></span>
- <span data-ttu-id="92317-178">"~"</span><span class="sxs-lookup"><span data-stu-id="92317-178">"~"</span></span>
- <span data-ttu-id="92317-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="92317-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="92317-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="92317-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="92317-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="92317-181">"\_"</span></span>

---

# <a name="vectors-and-matrices"></a><span data-ttu-id="92317-182">Векторы и матрицы</span><span class="sxs-lookup"><span data-stu-id="92317-182">Vectors and Matrices</span></span>

<span data-ttu-id="92317-183">Некоторые навыки работы с векторами и матрицами необходимы для понимания тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="92317-183">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="92317-184">Мы предоставляем краткое введение ниже, и заинтересованные читатели рекомендуют читать стандартную ссылку на линейную перерезку *, например Странг, G. (1993). Введение в линейную перерезку (Vol. 3). Веллеслэй, MA: Wellesley-Cambridge Press* или Интернет-ссылка, например [Линейная](http://joshua.smcvt.edu/linearalgebra/)переслать.</span><span class="sxs-lookup"><span data-stu-id="92317-184">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="92317-185">Вектор столбца (или просто [*вектор*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ $ версии измерения (или размера) $ n $ представляет собой набор из $ n $ комплексных чисел $ (v_1, v_2, \лдотс, v_n), $ упорядоченных в виде столбца.</span><span class="sxs-lookup"><span data-stu-id="92317-185">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="92317-186">$$v =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-186">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="92317-187">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-187">v_1\\\\</span></span>
<span data-ttu-id="92317-188">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-188">v_2\\\\</span></span>
<span data-ttu-id="92317-189">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-189">\vdots\\\\</span></span>
<span data-ttu-id="92317-190">v_n \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="92317-190">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="92317-191">Норма вектора $ v $ определяется как $ \sqrt { \sum \_ i | v \_ i | ^ 2 } $ .</span><span class="sxs-lookup"><span data-stu-id="92317-191">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="92317-192">Говорят, что вектор является нормой единицы (или же он называется [*вектором*](https://en.wikipedia.org/wiki/Unit_vector)), если его значение равно $ 1 $ .</span><span class="sxs-lookup"><span data-stu-id="92317-192">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="92317-193">[*Смежная часть вектора*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ v $ обозначается $ v ^ \dagger $ и определяется как следующий вектор строки $ \* $ , где обозначает комплексно сопряженный,</span><span class="sxs-lookup"><span data-stu-id="92317-193">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="92317-194">$$\begin{bmatrix}v_1 \\\\ \вдотс \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} v_1 ^ \* & \cdots & v_n ^ \*\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="92317-194">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="92317-195">Наиболее распространенным способом умножения двух векторов является [*внутренний продукт*](https://en.wikipedia.org/wiki/Inner_product_space), который также называется «точкой».</span><span class="sxs-lookup"><span data-stu-id="92317-195">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="92317-196">Внутренний продукт предоставляет проекцию одного вектора на другой и не имеет ценности в описании того, как выразить один вектор как сумму других простых векторов.</span><span class="sxs-lookup"><span data-stu-id="92317-196">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="92317-197">Внутренний продукт между $ u $ и $ v $ , обозначенным $ \left \langle u, v, \right \rangle $ определяется как</span><span class="sxs-lookup"><span data-stu-id="92317-197">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

$$
<span data-ttu-id="92317-198">\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="92317-198">\langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="92317-199">Эта нотация также позволяет записать норму вектора $ v $ как $ \sqrt { \langle v, v \rangle } $ .</span><span class="sxs-lookup"><span data-stu-id="92317-199">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="92317-200">Можно умножить вектор на число $ c, $ чтобы сформировать новый вектор, записи которого умножаются на $ c $ .</span><span class="sxs-lookup"><span data-stu-id="92317-200">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="92317-201">Можно также добавить два вектора $ u $ и v $ , $ чтобы сформировать новый вектор, записи которого являются суммой записей $ u $ и $ v $ .</span><span class="sxs-lookup"><span data-stu-id="92317-201">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="92317-202">Эти операции показаны ниже.</span><span class="sxs-lookup"><span data-stu-id="92317-202">These operations are depicted below:</span></span>

<span data-ttu-id="92317-203">$$\mathrm{Если } ~ u=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-203">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="92317-204">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-204">u_1\\\\</span></span>
<span data-ttu-id="92317-205">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-205">u_2\\\\</span></span>
<span data-ttu-id="92317-206">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-206">\vdots\\\\</span></span>
<span data-ttu-id="92317-207">u_n \end{bmatrix} ~ \mathrm { и}~</span><span class="sxs-lookup"><span data-stu-id="92317-207">u_n \end{bmatrix}~\mathrm{and}~</span></span>
<span data-ttu-id="92317-208">3,3 =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-208">v =\begin{bmatrix}</span></span>
    <span data-ttu-id="92317-209">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-209">v_1\\\\</span></span>
    <span data-ttu-id="92317-210">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-210">v_2\\\\</span></span>
    <span data-ttu-id="92317-211">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-211">\vdots\\\\</span></span>
    <span data-ttu-id="92317-212">v_n \end{bmatrix} , ~ \mathrm { затем}~</span><span class="sxs-lookup"><span data-stu-id="92317-212">v_n \end{bmatrix},~\mathrm{then}~</span></span>
<span data-ttu-id="92317-213">Au + BV =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-213">au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="92317-214">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-214">au_1+bv_1\\\\</span></span>
<span data-ttu-id="92317-215">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-215">au_2+bv_2\\\\</span></span>
<span data-ttu-id="92317-216">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-216">\vdots\\\\</span></span>
<span data-ttu-id="92317-217">au_n + bv_n \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="92317-217">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="92317-218">[*Матрица*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) размером $ m \times n $ представляет собой коллекцию $ $ комплексных чисел MN, упорядоченных в $ m $ строках и $ n $ столбцов, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="92317-218">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="92317-219">$$Пн =</span><span class="sxs-lookup"><span data-stu-id="92317-219">$$M =</span></span> 
\begin{bmatrix}
<span data-ttu-id="92317-220">M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-220">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
<span data-ttu-id="92317-221">M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2N}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-221">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="92317-222">M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-222">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\</span></span>
<span data-ttu-id="92317-223">\end{bmatrix}.$$</span><span class="sxs-lookup"><span data-stu-id="92317-223">\end{bmatrix}.$$</span></span>

<span data-ttu-id="92317-224">Обратите внимание, что вектор измерения $ n $ — это просто матрица размера $ n \times 1 $ .</span><span class="sxs-lookup"><span data-stu-id="92317-224">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="92317-225">Как и в случае с векторами, можно умножить матрицу на число $ c $ , чтобы получить новую матрицу, в которой каждая запись умножается на $ c $ , и мы можем добавить две матрицы одного размера, чтобы создать новую матрицу, записи которой являются суммой соответствующих записей двух матриц.</span><span class="sxs-lookup"><span data-stu-id="92317-225">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="92317-226">Умножение и продукты тензорные</span><span class="sxs-lookup"><span data-stu-id="92317-226">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="92317-227">Можно также умножить две матрицы $ m $ $ на Dimension m \times $ и $ n $ измерения $ n p, \times $ чтобы получить новую матрицу $ p $ измерения $ m \times p $ , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="92317-227">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

\begin{align}
&\begin{bmatrix}
    <span data-ttu-id="92317-228">M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-228">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
    <span data-ttu-id="92317-229">M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2N}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-229">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
    \ddots\\\\
    <span data-ttu-id="92317-230">M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { MN}</span><span class="sxs-lookup"><span data-stu-id="92317-230">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
\end{bmatrix}
\begin{bmatrix}
<span data-ttu-id="92317-231">N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1p}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-231">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\</span></span>
<span data-ttu-id="92317-232">N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2P}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-232">N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="92317-233">N_ { N1 } ~~ N_ { N2 } ~~ \cdots ~~ N_ { NP}</span><span class="sxs-lookup"><span data-stu-id="92317-233">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
\end{bmatrix}=\begin{bmatrix}
<span data-ttu-id="92317-234">P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1p}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-234">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\</span></span>
<span data-ttu-id="92317-235">P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2P}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-235">P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="92317-236">P_ { M1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { MP}</span><span class="sxs-lookup"><span data-stu-id="92317-236">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
\end{bmatrix}
\end{align}

<span data-ttu-id="92317-237">где записи $ P $ — $ P_ { ОК } = \sum _j M_ { ИЖ } N_ { ЖК } $ .</span><span class="sxs-lookup"><span data-stu-id="92317-237">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="92317-238">Например, запись $ P_ { 11 } $ — это внутреннее произведение первой строки $ M $ с первым столбцом $ N $ . Обратите внимание, что поскольку вектор является просто особым случаем матрицы, это определение расширяется на умножение векторных матриц.</span><span class="sxs-lookup"><span data-stu-id="92317-238">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$. Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="92317-239">Все матрицы, которые мы будем рассматривать, представляют собой квадратные матрицы, где число строк и столбцов равно, или векторы, которые соответствуют только $ одному $ столбцу.</span><span class="sxs-lookup"><span data-stu-id="92317-239">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="92317-240">Одна особая квадратная матрица — это [*единичная матрица*](https://en.wikipedia.org/wiki/Identity_matrix), помеченная $ \boldone $ , в которой все его диагональные элементы равны $ 1 $ , а остальные элементы равны $ 0 $ :</span><span class="sxs-lookup"><span data-stu-id="92317-240">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

$$\boldone=\begin{bmatrix}
<span data-ttu-id="92317-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="92317-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="92317-243">~~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-243">~~ \ddots\\\\</span></span>
<span data-ttu-id="92317-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$</span><span class="sxs-lookup"><span data-stu-id="92317-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="92317-245">Для квадратной матрицы $ a $ мы говорим, что матрица $ B $ является [*обратной*](https://en.wikipedia.org/wiki/Invertible_matrix) , если $ AB = Ба = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="92317-245">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="92317-246">Обратная часть матрицы не должна существовать, но, если она существует, она уникальна и обстоится $ как ^ { -1 } $ .</span><span class="sxs-lookup"><span data-stu-id="92317-246">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="92317-247">Для любой матрицы $ m $ прилегающий или сопряженный с $ m $ является матрицей $ N $ , такой, что $ N_ { ИЖ } = M_ { ji } ^ \* $ .</span><span class="sxs-lookup"><span data-stu-id="92317-247">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="92317-248">Смежная часть $ M $ обычно обозначается как $ m ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="92317-248">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="92317-249">Мы говорим, что матрица $ U $ является [*единой*](https://en.wikipedia.org/wiki/Unitary_matrix) $ , если УУ ^ u \dagger = ^ \dagger u = \boldone $ или аналогичным, $ u ^ { -1 } = u ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="92317-249">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="92317-250">Возможно, наиболее важным свойством единой матрицы является то, что они сохраняют норму вектора.</span><span class="sxs-lookup"><span data-stu-id="92317-250">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="92317-251">Это происходит из-за того, что</span><span class="sxs-lookup"><span data-stu-id="92317-251">This happens because</span></span> 

<span data-ttu-id="92317-252">$$\langlev, v v \rangle = ^ \dagger v ^ = u ^ \dagger { -1 } U v = v ^ \dagger u ^ u v \dagger = \langle , u v \rangle .$$</span><span class="sxs-lookup"><span data-stu-id="92317-252">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="92317-253">Матрица $ m $ называется [*хермитиан*](https://en.wikipedia.org/wiki/Hermitian_matrix) , если $ m = m ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="92317-253">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="92317-254">Наконец, [*продукт тензорные*](https://en.wikipedia.org/wiki/Tensor_product) (или кронеккер продукт) двух матриц $ M $ размером $ m \times n $ и $ n $ из размера $ p \times q $ — это более крупная матрица $ p = M n с \otimes $ размером $ MP \times НК $ , и она получается из $ M $ и $ n $ следующим образом:</span><span class="sxs-lookup"><span data-stu-id="92317-254">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

\begin{align}
    <span data-ttu-id="92317-255">M \otimes N &=</span><span class="sxs-lookup"><span data-stu-id="92317-255">M \otimes N &=</span></span>
    \begin{bmatrix}
        <span data-ttu-id="92317-256">M_ { 11 } ~~ \cdots ~~ M_ { 1N }\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-256">M_{11} ~~ \cdots ~~ M_{1n} \\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="92317-257">M_ { M1 } ~~ \cdots ~~ M_ { MN  }</span><span class="sxs-lookup"><span data-stu-id="92317-257">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        <span data-ttu-id="92317-258">N_ { 11 } ~~ \cdots ~~ N_ { 1Q  }\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-258">N_{11}  ~~ \cdots ~~ N_{1q}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="92317-259">N_ { P1 } ~~ \cdots ~~ N_ { PQ}</span><span class="sxs-lookup"><span data-stu-id="92317-259">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        <span data-ttu-id="92317-260">M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="92317-260">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="92317-261">M_ { 1N } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-261">M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="92317-262">M_ { M1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="92317-262">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="92317-263">M_ { MN } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-263">M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="92317-264">\end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="92317-264">\end{bmatrix}.</span></span>
\end{align}

<span data-ttu-id="92317-265">Это лучше продемонстрировать с помощью некоторых примеров:</span><span class="sxs-lookup"><span data-stu-id="92317-265">This is better demonstrated with some examples:</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="92317-266">a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ е \end{bmatrix}=</span><span class="sxs-lookup"><span data-stu-id="92317-266">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} =</span></span>
    \begin{bmatrix}
        <span data-ttu-id="92317-267">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-267">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="92317-268">\\\\[1,5 EM] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-268">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    \end{bmatrix}
    <span data-ttu-id="92317-269">=a б a b \begin{bmatrix} \\\\ \\\\ \\\\ c \\\\ б \\\\\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-269">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="92317-270">и</span><span class="sxs-lookup"><span data-stu-id="92317-270">and</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="92317-271">a \ b \\\\ c \ d \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-271">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    \otimes 
    \begin{bmatrix}
        <span data-ttu-id="92317-272">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-272">e\ f\\\\g\ h \end{bmatrix}</span></span>
     =
    \begin{bmatrix}
    <span data-ttu-id="92317-273">конкретного\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-273">a\begin{bmatrix}</span></span>
    <span data-ttu-id="92317-274">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-274">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="92317-275">&\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-275">b\begin{bmatrix}</span></span>
    <span data-ttu-id="92317-276">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-276">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="92317-277">\\\\[1em] c\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-277">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="92317-278">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-278">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="92317-279">четырехмерного\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-279">d\begin{bmatrix}</span></span>
    <span data-ttu-id="92317-280">e \ f \\\\ g \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="92317-280">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    \end{bmatrix}
    =
    \begin{bmatrix}
    <span data-ttu-id="92317-281">AE \ AF \ BF \\\\</span><span class="sxs-lookup"><span data-stu-id="92317-281">ae\ af\ be\ bf \\\\</span></span>
    <span data-ttu-id="92317-282">AG \ AH \ BG \ BH \\\\</span><span class="sxs-lookup"><span data-stu-id="92317-282">ag\ ah\ bg\ bh \\\\</span></span>
    <span data-ttu-id="92317-283">CE \ CF \ de \ DF \\\\</span><span class="sxs-lookup"><span data-stu-id="92317-283">ce\ cf\ de\ df \\\\</span></span>
    <span data-ttu-id="92317-284">CG \ CH \ \end{bmatrix} , DH.</span><span class="sxs-lookup"><span data-stu-id="92317-284">cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="92317-285">Последнее полезное соглашение об обозначении, окружающее продукты тензорные, заключается в том, что для любой векторной $ v $ или матрицы $ m $ , $ v ^ { \otimes n } $ или $ m ^ { \otimes n } $ это короткий рукой для $ $ повторяющегося тензорные продукта n.</span><span class="sxs-lookup"><span data-stu-id="92317-285">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="92317-286">Пример:</span><span class="sxs-lookup"><span data-stu-id="92317-286">For example:</span></span>

\begin{align}
<span data-ttu-id="92317-287">&\begin{bmatrix}1 \\\\ 0 1 \end{bmatrix} ^ { \otimes } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1-1 \\\\ \\\\ 1 \end{bmatrix} ,\\\\</span><span class="sxs-lookup"><span data-stu-id="92317-287">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\</span></span>
  <span data-ttu-id="92317-288">&\begin{bmatrix}0 1 1 0 1 0 1 1 0 & \\\\ & \end{bmatrix} ^ { \otimes } = \begin{bmatrix} & \\\\ & \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & & & \\\\ & & & \\\\ & & & \\\\ & & & \end{bmatrix} 0 0 1 0 0 1 0 0 1 0 0 1 0 0.</span><span class="sxs-lookup"><span data-stu-id="92317-288">&\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}  0& 1 \\\\ 1& 0    \end{bmatrix},    \qquad\begin{bmatrix}   0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
\end{align}
