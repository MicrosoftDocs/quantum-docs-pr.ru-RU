---
<span data-ttu-id="f450f-101">Title: Описание расширенных концепций матрицы Description: сведения о экспоненциальных понятиях основе собственных векторов, еиженвалуес и Matrix, основные инструменты, используемые для описания и моделирования тактов алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="f450f-101">title: Advanced matrix concepts description: Learn about eigenvectors, eigenvalues, and matrix exponentials, the fundamental tools used to describe and simulate quantum algorithms.</span></span>
<span data-ttu-id="f450f-102">Автор: Куантумвритер UID: Microsoft. тактов. Основные понятия. Matrix — расширенный MS. author: v-бенбра MS. Дата: 12/11/2017 MS. Topic: статья No-Loc:</span><span class="sxs-lookup"><span data-stu-id="f450f-102">author: QuantumWriter uid: microsoft.quantum.concepts.matrix-advanced ms.author: v-benbra ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="f450f-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="f450f-103">"Q#"</span></span>
- <span data-ttu-id="f450f-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="f450f-104">"$$v"</span></span>
- <span data-ttu-id="f450f-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="f450f-105">"$$"</span></span>
- <span data-ttu-id="f450f-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="f450f-106">"$$"</span></span>
- <span data-ttu-id="f450f-107">"$"</span><span class="sxs-lookup"><span data-stu-id="f450f-107">"$"</span></span>
- <span data-ttu-id="f450f-108">"$"</span><span class="sxs-lookup"><span data-stu-id="f450f-108">"$"</span></span>
- <span data-ttu-id="f450f-109">"$"</span><span class="sxs-lookup"><span data-stu-id="f450f-109">"$"</span></span>
- <span data-ttu-id="f450f-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="f450f-110">"$$"</span></span>
- <span data-ttu-id="f450f-111">"$$$"</span><span class="sxs-lookup"><span data-stu-id="f450f-111">"$$$"</span></span>
- <span data-ttu-id="f450f-112">"$$$"</span><span class="sxs-lookup"><span data-stu-id="f450f-112">"$$$"</span></span>
- <span data-ttu-id="f450f-113">"$$$"</span><span class="sxs-lookup"><span data-stu-id="f450f-113">"$$$"</span></span>
- <span data-ttu-id="f450f-114">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="f450f-114">"\cdots"</span></span>
- <span data-ttu-id="f450f-115">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="f450f-115">"bmatrix"</span></span>
- <span data-ttu-id="f450f-116">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="f450f-116">"\ddots"</span></span>
- <span data-ttu-id="f450f-117">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="f450f-117">"\equiv"</span></span>
- <span data-ttu-id="f450f-118">"\sum"</span><span class="sxs-lookup"><span data-stu-id="f450f-118">"\sum"</span></span>
- <span data-ttu-id="f450f-119">"\begin"</span><span class="sxs-lookup"><span data-stu-id="f450f-119">"\begin"</span></span>
- <span data-ttu-id="f450f-120">"\end"</span><span class="sxs-lookup"><span data-stu-id="f450f-120">"\end"</span></span>
- <span data-ttu-id="f450f-121">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="f450f-121">"\sqrt"</span></span>
- <span data-ttu-id="f450f-122">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="f450f-122">"\otimes"</span></span>
- <span data-ttu-id="f450f-123">"{"</span><span class="sxs-lookup"><span data-stu-id="f450f-123">"{"</span></span>
- <span data-ttu-id="f450f-124">"}"</span><span class="sxs-lookup"><span data-stu-id="f450f-124">"}"</span></span>
- <span data-ttu-id="f450f-125">"\text"</span><span class="sxs-lookup"><span data-stu-id="f450f-125">"\text"</span></span>
- <span data-ttu-id="f450f-126">"\phi"</span><span class="sxs-lookup"><span data-stu-id="f450f-126">"\phi"</span></span>
- <span data-ttu-id="f450f-127">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="f450f-127">"\kappa"</span></span>
- <span data-ttu-id="f450f-128">"\psi"</span><span class="sxs-lookup"><span data-stu-id="f450f-128">"\psi"</span></span>
- <span data-ttu-id="f450f-129">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="f450f-129">"\alpha"</span></span>
- <span data-ttu-id="f450f-130">"\beta"</span><span class="sxs-lookup"><span data-stu-id="f450f-130">"\beta"</span></span>
- <span data-ttu-id="f450f-131">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="f450f-131">"\gamma"</span></span>
- <span data-ttu-id="f450f-132">"\delta"</span><span class="sxs-lookup"><span data-stu-id="f450f-132">"\delta"</span></span>
- <span data-ttu-id="f450f-133">"\omega"</span><span class="sxs-lookup"><span data-stu-id="f450f-133">"\omega"</span></span>
- <span data-ttu-id="f450f-134">"\bra"</span><span class="sxs-lookup"><span data-stu-id="f450f-134">"\bra"</span></span>
- <span data-ttu-id="f450f-135">"\ket"</span><span class="sxs-lookup"><span data-stu-id="f450f-135">"\ket"</span></span>
- <span data-ttu-id="f450f-136">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="f450f-136">"\boldone"</span></span>
- <span data-ttu-id="f450f-137">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="f450f-137">"\\\\"</span></span>
- <span data-ttu-id="f450f-138">"\\"</span><span class="sxs-lookup"><span data-stu-id="f450f-138">"\\"</span></span>
- <span data-ttu-id="f450f-139">"="</span><span class="sxs-lookup"><span data-stu-id="f450f-139">"="</span></span>
- <span data-ttu-id="f450f-140">"\frac"</span><span class="sxs-lookup"><span data-stu-id="f450f-140">"\frac"</span></span>
- <span data-ttu-id="f450f-141">"\text"</span><span class="sxs-lookup"><span data-stu-id="f450f-141">"\text"</span></span>
- <span data-ttu-id="f450f-142">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="f450f-142">"\mapsto"</span></span>
- <span data-ttu-id="f450f-143">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="f450f-143">"\dagger"</span></span>
- <span data-ttu-id="f450f-144">"\to"</span><span class="sxs-lookup"><span data-stu-id="f450f-144">"\to"</span></span>
- <span data-ttu-id="f450f-145">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="f450f-145">"\begin{cases}"</span></span>
- <span data-ttu-id="f450f-146">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="f450f-146">"\end{cases}"</span></span>
- <span data-ttu-id="f450f-147">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="f450f-147">"\operatorname"</span></span>
- <span data-ttu-id="f450f-148">"\braket"</span><span class="sxs-lookup"><span data-stu-id="f450f-148">"\braket"</span></span>
- <span data-ttu-id="f450f-149">"\id"</span><span class="sxs-lookup"><span data-stu-id="f450f-149">"\id"</span></span>
- <span data-ttu-id="f450f-150">"\expect"</span><span class="sxs-lookup"><span data-stu-id="f450f-150">"\expect"</span></span>
- <span data-ttu-id="f450f-151">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="f450f-151">"\defeq"</span></span>
- <span data-ttu-id="f450f-152">"\variance"</span><span class="sxs-lookup"><span data-stu-id="f450f-152">"\variance"</span></span>
- <span data-ttu-id="f450f-153">"\dd"</span><span class="sxs-lookup"><span data-stu-id="f450f-153">"\dd"</span></span>
- <span data-ttu-id="f450f-154">"&"</span><span class="sxs-lookup"><span data-stu-id="f450f-154">"&"</span></span>
- <span data-ttu-id="f450f-155">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="f450f-155">"\begin{align}"</span></span>
- <span data-ttu-id="f450f-156">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="f450f-156">"\end{align}"</span></span>
- <span data-ttu-id="f450f-157">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="f450f-157">"\Lambda"</span></span>
- <span data-ttu-id="f450f-158">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="f450f-158">"\lambda"</span></span>
- <span data-ttu-id="f450f-159">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="f450f-159">"\Omega"</span></span>
- <span data-ttu-id="f450f-160">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="f450f-160">"\mathrm"</span></span>
- <span data-ttu-id="f450f-161">"\left"</span><span class="sxs-lookup"><span data-stu-id="f450f-161">"\left"</span></span>
- <span data-ttu-id="f450f-162">"\right"</span><span class="sxs-lookup"><span data-stu-id="f450f-162">"\right"</span></span>
- <span data-ttu-id="f450f-163">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="f450f-163">"\qquad"</span></span>
- <span data-ttu-id="f450f-164">"\times"</span><span class="sxs-lookup"><span data-stu-id="f450f-164">"\times"</span></span>
- <span data-ttu-id="f450f-165">"\big"</span><span class="sxs-lookup"><span data-stu-id="f450f-165">"\big"</span></span>
- <span data-ttu-id="f450f-166">"\langle"</span><span class="sxs-lookup"><span data-stu-id="f450f-166">"\langle"</span></span>
- <span data-ttu-id="f450f-167">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="f450f-167">"\rangle"</span></span>
- <span data-ttu-id="f450f-168">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="f450f-168">"\bigg"</span></span>
- <span data-ttu-id="f450f-169">"\Big"</span><span class="sxs-lookup"><span data-stu-id="f450f-169">"\Big"</span></span>
- <span data-ttu-id="f450f-170">"|"</span><span class="sxs-lookup"><span data-stu-id="f450f-170">"|"</span></span>
- <span data-ttu-id="f450f-171">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="f450f-171">"\mathbb"</span></span>
- <span data-ttu-id="f450f-172">"\vec"</span><span class="sxs-lookup"><span data-stu-id="f450f-172">"\vec"</span></span>
- <span data-ttu-id="f450f-173">"\in"</span><span class="sxs-lookup"><span data-stu-id="f450f-173">"\in"</span></span>
- <span data-ttu-id="f450f-174">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="f450f-174">"\texttt"</span></span>
- <span data-ttu-id="f450f-175">"\ne"</span><span class="sxs-lookup"><span data-stu-id="f450f-175">"\ne"</span></span>
- <span data-ttu-id="f450f-176">"<"</span><span class="sxs-lookup"><span data-stu-id="f450f-176">"<"</span></span>
- <span data-ttu-id="f450f-177">">"</span><span class="sxs-lookup"><span data-stu-id="f450f-177">">"</span></span>
- <span data-ttu-id="f450f-178">"\leq"</span><span class="sxs-lookup"><span data-stu-id="f450f-178">"\leq"</span></span>
- <span data-ttu-id="f450f-179">"\geq"</span><span class="sxs-lookup"><span data-stu-id="f450f-179">"\geq"</span></span>
- <span data-ttu-id="f450f-180">"~~"</span><span class="sxs-lookup"><span data-stu-id="f450f-180">"~~"</span></span>
- <span data-ttu-id="f450f-181">"~"</span><span class="sxs-lookup"><span data-stu-id="f450f-181">"~"</span></span>
- <span data-ttu-id="f450f-182">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="f450f-182">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="f450f-183">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="f450f-183">"\end{bmatrix}"</span></span>
- <span data-ttu-id="f450f-184">"\_"</span><span class="sxs-lookup"><span data-stu-id="f450f-184">"\_"</span></span>

---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="f450f-185">Дополнительные понятия матрицы</span><span class="sxs-lookup"><span data-stu-id="f450f-185">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="f450f-186">Теперь мы расширяем наши матрицы до [*еиженвалуес, основе собственных векторов*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) и [*экспоненциальных*](https://en.wikipedia.org/wiki/Matrix_exponential) элементов, которые формируют фундаментальный набор средств, необходимых для описания и реализации алгоритмов тактов.</span><span class="sxs-lookup"><span data-stu-id="f450f-186">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="f450f-187">Еиженвалуес и основе собственных векторов</span><span class="sxs-lookup"><span data-stu-id="f450f-187">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="f450f-188">Пусть $ M является $ квадратной матрицей, а $ v $ — вектором, который не является вектором нулей (т. е. вектором со всеми записями, равными $ 0 $ ).</span><span class="sxs-lookup"><span data-stu-id="f450f-188">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="f450f-189">Мы говорим $ о том, что v $ — это [*еиженвектор*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) из  $ M, $ Если $ = ОПС MV $ для некоторого числа $ c $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-189">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="f450f-190">Мы говорим, что $ c $ — это [*еиженвалуе*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) , соответствующий еиженвектор $ v $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-190">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="f450f-191">Как правило, матрица $ M $ может преобразовать вектор в любой другой вектор, но еиженвектор является специальным, так как он остается неизменным, за исключением умножения на число.</span><span class="sxs-lookup"><span data-stu-id="f450f-191">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="f450f-192">Обратите внимание, что если $ v $ — еиженвектор с еиженвалуе $ c $ , то $ AV $ также является еиженвектор (для любого ненулевого $ a $ ) с тем же еиженвалуе.</span><span class="sxs-lookup"><span data-stu-id="f450f-192">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="f450f-193">Например, для матрицы идентификаторов каждый вектор $ v $ является еиженвектор с еиженвалуе $ 1 $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-193">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="f450f-194">В качестве другого примера рассмотрим [*диагональную матрицу*](https://en.wikipedia.org/wiki/Diagonal_matrix) $ D, $ которая имеет ненулевые записи по диагонали:</span><span class="sxs-lookup"><span data-stu-id="f450f-194">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

$$
\begin{bmatrix}
<span data-ttu-id="f450f-195">d_1 0 0 0 d_2 0 0 0 & & \\\\ & & \\\\ & & D_3 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="f450f-195">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="f450f-196">Векторы</span><span class="sxs-lookup"><span data-stu-id="f450f-196">The vectors</span></span>

<span data-ttu-id="f450f-197">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \end{bmatrix} и \begin{bmatrix} 0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="f450f-197">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="f450f-198">основе собственных векторов этой матрицей с еиженвалуес  $ D_1 $ , $ D_2 $ и $ D_3 $ соответственно.</span><span class="sxs-lookup"><span data-stu-id="f450f-198">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="f450f-199">Если $ D_1 $ , $ D_2 $ и $ D_3 $ являются разными числами, то эти векторы (и их кратные) являются единственным основе собственных векторов матрицы $ d $ . Как правило, для диагональной матрицы легко читать еиженвалуес и основе собственных векторов.</span><span class="sxs-lookup"><span data-stu-id="f450f-199">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$. In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="f450f-200">Еиженвалуес — это все числа, отображаемые по диагонали, а их соответствующие основе собственных векторов — это векторы единиц с одной записью, равной $ 1, $ а оставшиеся записи — $ 0 $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-200">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="f450f-201">Обратите внимание, что в приведенном выше примере основе собственных векторов $ D $ образуют базу для $ трехмерных $ векторов.</span><span class="sxs-lookup"><span data-stu-id="f450f-201">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="f450f-202">Базис — это набор векторов, в которых любой вектор может быть записан в виде линейного сочетания.</span><span class="sxs-lookup"><span data-stu-id="f450f-202">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="f450f-203">Более явно, $ v_1 $ , $ v_2 $ и $ v_3 $ формируют базу, если любой вектор $ v $ может быть написан как $ v = A_1 v_1 + a_2 v_2 + a_3 v_3 $ для некоторых чисел $ A_1 $ , $ A_2 $ и $ a_3 $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-203">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="f450f-204">Вспомним, что матрица Хермитиан (также называемая самостоятельным) является сложной квадратной матрицей, равной ее собственной комплексной трансобъектно-сопряженной таблицей, а единая матрица — сложная квадратная матрица, обратная равенства которой равно его соседнему или сложному сопряжению.</span><span class="sxs-lookup"><span data-stu-id="f450f-204">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate transpose, while a unitary matrix is a complex square matrix whose inverse is equal to its adjoint or complex conjugate transpose.</span></span>
<span data-ttu-id="f450f-205">Для Хермитиан и единых матриц, которые, по сути, являются единственными матрицами, обнаруженными в тактовых вычислениях, существует общий результат, известный как [*Спектрал Теорема*](https://en.wikipedia.org/wiki/Spectral_theorem), который утверждает следующее: для любой хермитиан или единой матрицы $ m $ существует единая $ u, $ такая, что $ m = u ^ \dagger d u $ для некоторой диагональной матрицы $ D $ . Более того, диагональными записями $ D $ будет еиженвалуес $ M $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-205">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$. Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="f450f-206">Мы уже узнали, как вычислить еиженвалуес и основе собственных векторов по диагонали матрицы $ D $ . Используя этот теорема, мы понимаем, что если $ v $ — это еиженвектор $ D $ с еиженвалуе $ c $ , т. е. $ DV = ОПС $ , то $ U ^ \dagger v $ будет еиженвектор $ м $ с еиженвалуе $ c $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-206">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$. Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="f450f-207">Это вызвано тем, что</span><span class="sxs-lookup"><span data-stu-id="f450f-207">This is because</span></span>

<span data-ttu-id="f450f-208">$$M (U ^ \dagger v) = u ^ \dagger d u (u ^ \dagger v) = U ^ \dagger d (u u ^ \dagger ) v = u ^ \dagger d v = c u ^ \dagger v.$$</span><span class="sxs-lookup"><span data-stu-id="f450f-208">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="f450f-209">Экспоненты матрицы</span><span class="sxs-lookup"><span data-stu-id="f450f-209">Matrix Exponentials</span></span>
<span data-ttu-id="f450f-210">[*Экспоненциальное значение матрицы*](https://en.wikipedia.org/wiki/Matrix_exponential) также может быть определено точно в экспоненциальной функции.</span><span class="sxs-lookup"><span data-stu-id="f450f-210">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="f450f-211">Экспонента матрицы $ a $ может быть выражена как</span><span class="sxs-lookup"><span data-stu-id="f450f-211">The matrix exponential of a matrix $A$ can be expressed as</span></span>

$$
<span data-ttu-id="f450f-212">e ^ A = \boldone + a + a \frac { ^ 2 } { 2! } + \frac { ^ 3 } { 3!}+\cdots</span><span class="sxs-lookup"><span data-stu-id="f450f-212">e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots</span></span>
$$

<span data-ttu-id="f450f-213">Это важно, так как эволюция на механической тактовой частоты описывается единой матрицей вида $ e ^ { } $ геохермитиан Matrix $ B $ .  По этой причине выполнение экспоненциальных вычислений является фундаментальной частью тактовой среды и, как таковая, Q# предоставляет встроенные подпрограммы для описания этих операций.</span><span class="sxs-lookup"><span data-stu-id="f450f-213">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.  For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="f450f-214">Существует много способов вычислить экспоненциальное значение матрицы на классическем компьютере, а в общем, в целом, приблизительно такой показатель, сопряжено с PERIL.</span><span class="sxs-lookup"><span data-stu-id="f450f-214">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="f450f-215">См [*. раздел Cleve Молер and Чарльз Van Loan. «Девятнадцать сомнительна способ вычислить экспоненту матрицы». SIAM проверка 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) для получения дополнительных сведений о связанных проблемах.</span><span class="sxs-lookup"><span data-stu-id="f450f-215">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="f450f-216">Самый простой способ понять, как вычислить экспоненту матрицы — это еиженвалуес и основе собственных векторов этой матрицы.</span><span class="sxs-lookup"><span data-stu-id="f450f-216">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="f450f-217">В частности, Спектрал теорема, о которых говорилось выше, говорит о том, что для каждой Хермитиан или единой матрицы $ A $ существует единая матрица $ U $ и диагональная матрица $ D $ , такая $ как = u ^ \dagger d u $ .  Из-за свойств унитарити мы добавили $ ^ 2 = u ^ \dagger D ^ 2 u $ и аналогично любому Power $ p $ $ A ^ p = u ^ \dagger D ^ p u $ .  Если мы подставляем это в определение оператора экспоненциального оператора, мы получаем следующее:</span><span class="sxs-lookup"><span data-stu-id="f450f-217">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

$$
<span data-ttu-id="f450f-218">e ^ A = U ^ \dagger \left ( \boldone + d + \frac { d ^ 2 } { 2! } + \cdots \right ) U = u ^ \dagger \begin{bmatrix} \експ (D_ { 11 } ) & 0 & \cdots & 0 \\\\ 0 & \експ (D_ { 22 } ) & \cdots & 0 \\\\ \вдотс & \вдотс & \ddots & \вдотс \\\\ 0 & 0 & \cdots & \експ (D_ { nn } ) \end{bmatrix} U.$$</span><span class="sxs-lookup"><span data-stu-id="f450f-218">e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="f450f-219">Иными словами, если преобразовать в еиженбасис матрицы $ , то $ вычисление экспоненты матрицы эквивалентно вычислению обычной экспоненты еиженвалуес матрицы.</span><span class="sxs-lookup"><span data-stu-id="f450f-219">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="f450f-220">Так как многие операции в тактовых вычислениях предполагают выполнение экспоненциальных вычислений, этот прием еиженбасис матрицы, чтобы упростить выполнение экспоненциального оператора, часто встречается и является основанием для многих алгоритмов такта, таких как Троттер — Сузуки-методы моделирования тактов, описанные далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="f450f-220">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="f450f-221">Другое полезное свойство равно, если $ b $ является как единым, так и хермитиан, т. е. $ b = b ^ { -1 } = B ^ \dagger $ then $ b ^ 2 = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="f450f-221">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="f450f-222">Применяя это правило к вышеуказанному расширению экспоненты матрицы и группируя $ \boldone $ термины и в $ $ вместе с ними, можно увидеть, что для любого действительного значения $ x $ удостоверения</span><span class="sxs-lookup"><span data-stu-id="f450f-222">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="f450f-223">$$e ^ { ибкс } = \boldone \кос (x) + иб\син (x)$$</span><span class="sxs-lookup"><span data-stu-id="f450f-223">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="f450f-224">являющемся.</span><span class="sxs-lookup"><span data-stu-id="f450f-224">holds.</span></span> <span data-ttu-id="f450f-225">Этот прием особенно полезен, так как он позволяет узнать экспоненциальное значение матрицы действий, даже если измерение $ b $ является экспоненциально большим, в случае если $ b $ является как единым, так и хермитиан.</span><span class="sxs-lookup"><span data-stu-id="f450f-225">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
