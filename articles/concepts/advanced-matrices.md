---
title: Расширенные концепции матриц
description: Сведения о экспоненциальных экспонентах основе собственных векторов, еиженвалуес и Matrix, основных средствах, используемых для описания и моделирования тактов алгоритмов.
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- $$
- $$
- $$
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
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: 71923247121eae6a1d4e26d2664d8e547370ba3a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269462"
---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="c32bd-103">Дополнительные понятия матрицы</span><span class="sxs-lookup"><span data-stu-id="c32bd-103">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="c32bd-104">Теперь мы расширяем наши матрицы до [*еиженвалуес, основе собственных векторов*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) и [*экспоненциальных*](https://en.wikipedia.org/wiki/Matrix_exponential) элементов, которые формируют фундаментальный набор средств, необходимых для описания и реализации алгоритмов тактов.</span><span class="sxs-lookup"><span data-stu-id="c32bd-104">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="c32bd-105">Еиженвалуес и основе собственных векторов</span><span class="sxs-lookup"><span data-stu-id="c32bd-105">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="c32bd-106">Let $M $ быть квадратной матрицей и $v $ быть вектором, который не является вектором нулей (т. е. вектором со всеми записями, равными $0 $ ).</span><span class="sxs-lookup"><span data-stu-id="c32bd-106">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="c32bd-107">Мы говорим, что $v $ является [*еиженвектором*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) $M $ Если $MV = опс $ для некоторого числа $c $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-107">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="c32bd-108">Мы говорим, что $c $ — [*еиженвалуе*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) , соответствующий $vу еиженвектор $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-108">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="c32bd-109">В целом матрица $M $ может преобразовать вектор в любой другой вектор, но еиженвектор является специальным, так как он остается неизменным, за исключением умножения на число.</span><span class="sxs-lookup"><span data-stu-id="c32bd-109">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="c32bd-110">Обратите внимание, что если $v $ является еиженвектор с еиженвалуе $c $ , $AV $ также является еиженвектор (для любого ненулевого $a $ ) с тем же еиженвалуе.</span><span class="sxs-lookup"><span data-stu-id="c32bd-110">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="c32bd-111">Например, для матрицы идентификаторов каждый Векторный $v $ является еиженвектор с еиженвалуе $1 $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-111">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="c32bd-112">В качестве другого примера рассмотрим [*диагональную матрицу*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D, $ которая содержит ненулевые записи по диагонали:</span><span class="sxs-lookup"><span data-stu-id="c32bd-112">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

<span data-ttu-id="c32bd-113">\бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="c32bd-113">$$ \begin{bmatrix}</span></span>
<span data-ttu-id="c32bd-114">d_1 & 0 & 0 \\ \\ 0 & D_2 & 0 \\ \\ 0 & 0 & \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="c32bd-114">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="c32bd-115">Векторы</span><span class="sxs-lookup"><span data-stu-id="c32bd-115">The vectors</span></span>

<span data-ttu-id="c32bd-116">$ $ \бегин{ bmatrix } 1 \\ \\ 0 \\ \\ 0 \енд{ bmatrix } , \бегин{ bmatrix } 0 \\ \\ 1 \\ \\ 0 \end{bmatrix} и \бегин{ bmatrix } 0 \\ \\ 0 \\ \\ 1\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="c32bd-116">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="c32bd-117">основе собственных векторов этой матрицей с еиженвалуес $d _1 $ , $d _2 $ и $d _3 $ соответственно.</span><span class="sxs-lookup"><span data-stu-id="c32bd-117">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="c32bd-118">Если $d _1 $ , $d _2 $ и $d _3 $ являются разными числами, то эти векторы (и их кратные) являются единственным основе собственных векторов $D матрицы $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-118">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$.</span></span> <span data-ttu-id="c32bd-119">Как правило, для диагональной матрицы легко читать еиженвалуес и основе собственных векторов.</span><span class="sxs-lookup"><span data-stu-id="c32bd-119">In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="c32bd-120">Еиженвалуес — это все числа, отображаемые по диагонали, а их соответствующие основе собственных векторов — это векторы единиц с одной записью, равной $1, $ а оставшиеся записи равны $0 $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-120">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="c32bd-121">Обратите внимание, что в приведенном выше примере основе собственных векторов $D $ образуют базу для $3ных $ векторов.</span><span class="sxs-lookup"><span data-stu-id="c32bd-121">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="c32bd-122">Базис — это набор векторов, в которых любой вектор может быть записан в виде линейного сочетания.</span><span class="sxs-lookup"><span data-stu-id="c32bd-122">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="c32bd-123">Более явно, $v _1 $ , $v _2 $ и $v _3 $ формируют базу, если любой Векторный $v $ можно написать как $v = a_1 v_1 + a_2 v_2 + a_3 v_3 $ для некоторых чисел $a _1 $ , $a _2 $ и $a _3 $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-123">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="c32bd-124">Вспомним, что матрица Хермитиан (также называемая самостоятельным) является сложной квадратной матрицей, равной ее собственной сложной сопряженной, а единая матрица — сложная квадратная матрица, обратная величина которой равна комплексному сопряженному.</span><span class="sxs-lookup"><span data-stu-id="c32bd-124">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate, while a unitary matrix is a complex square matrix whose inverse is equal to its complex conjugate.</span></span>
<span data-ttu-id="c32bd-125">Для Хермитиан и единых матриц, которые, по сути, являются единственными матрицами, обнаруженными в тактовых вычислениях, существует общий результат, известный как [*Спектрал Теорема*](https://en.wikipedia.org/wiki/Spectral_theorem), который утверждает следующее: для любой хермитиан или $Mой матрицы $ существует единая $U $ , которая $M = u ^ \дагжер D $ для некоторых диагональных $D матрицы $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-125">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$.</span></span> <span data-ttu-id="c32bd-126">Более того, диагональными записями $D $ будет еиженвалуес $M $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-126">Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="c32bd-127">Мы уже узнали, как вычислить еиженвалуес и основе собственных векторов диагональной матрицы $D $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-127">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$.</span></span> <span data-ttu-id="c32bd-128">Используя этот теорема, мы понимаем, что если $v $ является еиженвектором $D $ с еиженвалуе $c $ , т. е. $DV = ОПС $ , $U ^ \дагжер v $ будет еиженвектор $M $ с еиженвалуе $c $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-128">Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="c32bd-129">Это вызвано тем, что</span><span class="sxs-lookup"><span data-stu-id="c32bd-129">This is because</span></span>

<span data-ttu-id="c32bd-130">$ $M (U ^ \дагжер v) = U ^ \дагжер D U (U ^ \дагжер v) = U ^ \дагжер D (U U ^ \дагжер) v = U ^ \дагжер D v = c U ^ \дагжер v. $ $</span><span class="sxs-lookup"><span data-stu-id="c32bd-130">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="c32bd-131">Экспоненты матрицы</span><span class="sxs-lookup"><span data-stu-id="c32bd-131">Matrix Exponentials</span></span>
<span data-ttu-id="c32bd-132">[*Экспоненциальное значение матрицы*](https://en.wikipedia.org/wiki/Matrix_exponential) также может быть определено точно в экспоненциальной функции.</span><span class="sxs-lookup"><span data-stu-id="c32bd-132">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="c32bd-133">Экспонента матрицы $A $ может быть выражена как</span><span class="sxs-lookup"><span data-stu-id="c32bd-133">The matrix exponential of a matrix $A$ can be expressed as</span></span>

<span data-ttu-id="c32bd-134">$ $ e ^ A = \болдоне + a + \фрак{а ^ 2 } {2!} + \Фрак{а ^ 3 } {3!} + \кдотс $ $</span><span class="sxs-lookup"><span data-stu-id="c32bd-134">$$ e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots $$</span></span>

<span data-ttu-id="c32bd-135">Это важно, так как эволюция с помощью механических данных в такте описывается единой матрицей формы $e ^ { } геосхема $ for хермитиан matrix $B $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-135">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.</span></span>  <span data-ttu-id="c32bd-136">По этой причине выполнение экспоненциальных вычислений является фундаментальной частью тактовой среды и, как и в Q #, предоставляет встроенные подпрограммы для описания этих операций.</span><span class="sxs-lookup"><span data-stu-id="c32bd-136">For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="c32bd-137">Существует много способов вычислить экспоненциальное значение матрицы на классическем компьютере, а в общем, в целом, приблизительно такой показатель, сопряжено с PERIL.</span><span class="sxs-lookup"><span data-stu-id="c32bd-137">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="c32bd-138">См [*. раздел Cleve Молер and Чарльз Van Loan. «Девятнадцать сомнительна способ вычислить экспоненту матрицы». SIAM проверка 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) для получения дополнительных сведений о связанных проблемах.</span><span class="sxs-lookup"><span data-stu-id="c32bd-138">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="c32bd-139">Самый простой способ понять, как вычислить экспоненту матрицы — это еиженвалуес и основе собственных векторов этой матрицы.</span><span class="sxs-lookup"><span data-stu-id="c32bd-139">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="c32bd-140">В частности, Спектрал теорема, о которых говорилось выше, говорит о том, что для каждой Хермитиан или единой матрицы $A $ существует единая матрица $U $ и диагональная матрица $D $ , которая $A = u ^ \дагжер D u $ .  Из-за свойств унитарити мы имели $A ^ 2 = U ^ \дагжер D ^ 2 U $ и аналогично любому $Pу Power, $ $A ^ p = u ^ \дагжер D ^ p U $ .  Если мы подставляем это в определение оператора экспоненциального оператора, мы получаем следующее:</span><span class="sxs-lookup"><span data-stu-id="c32bd-140">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

<span data-ttu-id="c32bd-141">$ $ e ^ A = U ^ \дагжер \лефт (\болдоне + D + \фрак{д ^ 2 } {2!} + \кдотс \ригхт) U = u ^ \дагжер \бегин{ bmatrix } \експ (D_ {11 } ) & 0 & \кдотс &0 \\\\ 0 & \експ (D_ {22 } ) & \кдотс & 0 \\\\ \вдотс & \вдотс & \ддотс & \вдотс \\\\ 0&0 & \кдотс & \exp (D_ {NN } ) \end{ bmatrix } U. $ $</span><span class="sxs-lookup"><span data-stu-id="c32bd-141">$$ e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="c32bd-142">Иными словами, при преобразовании в еиженбасис матрицы $A $ затем вычисление экспоненты матрицы эквивалентно вычислению обычной экспоненты еиженвалуес матрицы.</span><span class="sxs-lookup"><span data-stu-id="c32bd-142">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="c32bd-143">Так как многие операции в тактовых вычислениях предполагают выполнение экспоненциальных вычислений, этот прием еиженбасис матрицы, чтобы упростить выполнение экспоненциального оператора, часто встречается и является основанием для многих алгоритмов такта, таких как Троттер — Сузуки-методы моделирования тактов, описанные далее в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="c32bd-143">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="c32bd-144">Другое полезное свойство — если $B $ является единым и хермитиан, т. е. $B = b ^ {-1 } = b ^ \дагжер $ затем $B ^ 2 = \болдоне $ .</span><span class="sxs-lookup"><span data-stu-id="c32bd-144">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="c32bd-145">Применяя это правило к вышеуказанному расширению экспоненты матрицы и группированию $ значений $ \болдоне и $Bных $ терминов, можно увидеть, что для любого фактического значения $x $ удостоверения.</span><span class="sxs-lookup"><span data-stu-id="c32bd-145">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="c32bd-146">$ $e ^ {Ибкс } = \болдоне \кос (x) + иб\син (x) $ $</span><span class="sxs-lookup"><span data-stu-id="c32bd-146">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="c32bd-147">являющемся.</span><span class="sxs-lookup"><span data-stu-id="c32bd-147">holds.</span></span> <span data-ttu-id="c32bd-148">Этот прием особенно полезен, так как он позволяет попытаться узнать экспоненциальное значение матрицы действий, даже если измерение $B $ экспоненциально велико, для особого случая, когда $B $ является как единым, так и хермитиан.</span><span class="sxs-lookup"><span data-stu-id="c32bd-148">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
