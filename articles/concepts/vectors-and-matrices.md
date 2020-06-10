---
title: Векторы и матрицы в квантовых вычислениях
description: Изучите основы работы с векторами и матрицами.
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
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
ms.openlocfilehash: 6c09531cd8bee8f5efb472c95c575daed04d3040
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630205"
---
# <a name="vectors-and-matrices"></a><span data-ttu-id="db718-103">Векторы и матрицы</span><span class="sxs-lookup"><span data-stu-id="db718-103">Vectors and Matrices</span></span>

<span data-ttu-id="db718-104">Некоторые навыки работы с векторами и матрицами необходимы для понимания тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="db718-104">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="db718-105">Мы предоставляем краткое введение ниже, и заинтересованные читатели рекомендуют читать стандартную ссылку на линейную перерезку *, например Странг, G. (1993). Введение в линейную перерезку (Vol. 3). Веллеслэй, MA: Веллеслэй-Кембриджского нажмите* или онлайновую ссылку, например [линейную перерезку](http://joshua.smcvt.edu/linearalgebra/).</span><span class="sxs-lookup"><span data-stu-id="db718-105">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="db718-106">Вектор столбца (или просто [*вектор*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $ измерения (или размера) $n — это $ коллекция $n $ комплексных чисел $ (v_1, v_2, \лдотс, v_n) $ упорядочена в виде столбца:</span><span class="sxs-lookup"><span data-stu-id="db718-106">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="db718-107">$ $v = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-107">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="db718-108">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-108">v_1\\\\</span></span>
<span data-ttu-id="db718-109">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-109">v_2\\\\</span></span>
<span data-ttu-id="db718-110">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-110">\vdots\\\\</span></span>
<span data-ttu-id="db718-111">v_n \енд{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="db718-111">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="db718-112">Норма векторного $v $ определяется как $ \скрт { \сум \_ i | v \_ i | ^ 2 } $.</span><span class="sxs-lookup"><span data-stu-id="db718-112">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="db718-113">Говорят, что вектор является нормой единицы (или, Кроме того, он называется [*вектором*](https://en.wikipedia.org/wiki/Unit_vector)объекта), если его нормой является $1 $ .</span><span class="sxs-lookup"><span data-stu-id="db718-113">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="db718-114">[*Смежная часть векторного*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v $ обозначается $v ^ \дагжер $ и определяется как следующий вектор строки, где $ \* $ обозначает комплексно сопряженный,</span><span class="sxs-lookup"><span data-stu-id="db718-114">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="db718-115">$ $ \бегин{ bmatrix } v_1 \\ \\ \вдотс \\ \\ v_n \енд{ bmatrix } ^ \дагжер = \бегин{ bmatrix } v_1 ^ \* & \кдотс & v_n ^ \* \енд{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="db718-115">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="db718-116">Наиболее распространенным способом умножения двух векторов является [*внутренний продукт*](https://en.wikipedia.org/wiki/Inner_product_space), который также называется «точкой».</span><span class="sxs-lookup"><span data-stu-id="db718-116">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="db718-117">Внутренний продукт предоставляет проекцию одного вектора на другой и не имеет ценности в описании того, как выразить один вектор как сумму других простых векторов.</span><span class="sxs-lookup"><span data-stu-id="db718-117">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="db718-118">Внутренний продукт между $u $ и $v $ , обозначенный как $ \лефт \langle u, v \right \rangle $ определяется как</span><span class="sxs-lookup"><span data-stu-id="db718-118">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

<span data-ttu-id="db718-119">$ $ \лангле u, v \rangle = u ^ \дагжер v = u \_ 1 ^ { \* } v_1 + \кдотс + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="db718-119">$$ \langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="db718-120">Эта нотация также позволяет записать норму $v вектора в $ виде $ \скрт { \лангле v, v \rangle } $.</span><span class="sxs-lookup"><span data-stu-id="db718-120">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="db718-121">Можно умножить вектор на число $c, $ чтобы сформировать новый вектор, записи которого умножаются на $c $ .</span><span class="sxs-lookup"><span data-stu-id="db718-121">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="db718-122">Можно также добавить два вектора $u $ и $v, $ чтобы сформировать новый вектор, записи которого являются суммой записей $u $ и $v $ .</span><span class="sxs-lookup"><span data-stu-id="db718-122">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="db718-123">Эти операции показаны ниже.</span><span class="sxs-lookup"><span data-stu-id="db718-123">These operations are depicted below:</span></span>

<span data-ttu-id="db718-124">$ $ \Масрм{ИФ } ~ u = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-124">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="db718-125">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-125">u_1\\\\</span></span>
<span data-ttu-id="db718-126">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-126">u_2\\\\</span></span>
<span data-ttu-id="db718-127">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-127">\vdots\\\\</span></span>
<span data-ttu-id="db718-128">u_n \енд{ bmatrix } ~ \масрм{Анд } ~ v = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-128">u_n \end{bmatrix}~\mathrm{and}~ v =\begin{bmatrix}</span></span>
    <span data-ttu-id="db718-129">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-129">v_1\\\\</span></span>
    <span data-ttu-id="db718-130">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-130">v_2\\\\</span></span>
    <span data-ttu-id="db718-131">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-131">\vdots\\\\</span></span>
    <span data-ttu-id="db718-132">v_n \енд{ bmatrix } , ~ \масрм{Сен } ~ Au + BV = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-132">v_n \end{bmatrix},~\mathrm{then}~ au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="db718-133">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-133">au_1+bv_1\\\\</span></span>
<span data-ttu-id="db718-134">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-134">au_2+bv_2\\\\</span></span>
<span data-ttu-id="db718-135">\вдотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-135">\vdots\\\\</span></span>
<span data-ttu-id="db718-136">au_n + bv_n \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="db718-136">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="db718-137">[*Матрица*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) размера $m \тимес n $ — это коллекция $MN $ комплексных чисел, упорядоченных в $m $ строках и $n $ столбцах, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="db718-137">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="db718-138">$ $M = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-138">$$M = \begin{bmatrix}</span></span>
<span data-ttu-id="db718-139">M_ {11 } ~ ~ M_ {12 } ~ ~ \кдотс ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \кдотс ~ ~ M_ {2N } \\ \\ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-139">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="db718-140">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \кдотс ~ ~ M_ {MN } \\ \\ \енд{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="db718-140">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\ \end{bmatrix}.$$</span></span>

<span data-ttu-id="db718-141">Обратите внимание, что вектор $n измерения $ — это просто матрица размера $n \тимес 1 $ .</span><span class="sxs-lookup"><span data-stu-id="db718-141">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="db718-142">Как и в случае с векторами, можно умножить матрицу на число $c $ , чтобы получить новую матрицу, в которой каждая запись умножается на $c $ , и мы можем добавить две матрицы одного размера, чтобы создать новую матрицу, записи которой являются суммой соответствующих записей двух матриц.</span><span class="sxs-lookup"><span data-stu-id="db718-142">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="db718-143">Умножение и продукты тензорные</span><span class="sxs-lookup"><span data-stu-id="db718-143">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="db718-144">Можно также умножить две матрицы $M $ измерения $m \times n $ и $N $ измерения $n \тимес p, $ чтобы получить новую матрицу $P $ измерения $m \тимес p $ следующим образом:</span><span class="sxs-lookup"><span data-stu-id="db718-144">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

<span data-ttu-id="db718-145">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="db718-145">\begin{align}</span></span>
<span data-ttu-id="db718-146">& \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-146">&\begin{bmatrix}</span></span>
    <span data-ttu-id="db718-147">M_ {11 } ~ ~ M_ {12 } ~ ~ \кдотс ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \кдотс ~ ~ M_ {2N } \\ \\ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-147">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
    <span data-ttu-id="db718-148">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \кдотс ~ ~ M_ {MN}</span><span class="sxs-lookup"><span data-stu-id="db718-148">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
<span data-ttu-id="db718-149">концеbmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-149">\end{bmatrix}</span></span>
<span data-ttu-id="db718-150">началеbmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-150">\begin{bmatrix}</span></span>
<span data-ttu-id="db718-151">N_ {11 } ~ ~ N_ {12 } ~ ~ \кдотс ~ ~ N_ {1p } \\ \\ N_ {21 } ~ ~ N_ {22 } ~ ~ \кдотс ~ ~ N_ {2P } \\ \\ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-151">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\ N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="db718-152">N_ {N1 } ~ ~ N_ {N2 } ~ ~ \кдотс ~ ~ N_ {NP}</span><span class="sxs-lookup"><span data-stu-id="db718-152">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
<span data-ttu-id="db718-153">\енд{ bmatrix } = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-153">\end{bmatrix}=\begin{bmatrix}</span></span>
<span data-ttu-id="db718-154">P_ {11 } ~ ~ P_ {12 } ~ ~ \кдотс ~ ~ P_ {1p } \\ \\ P_ {21 } ~ ~ P_ {22 } ~ ~ \кдотс ~ ~ P_ {2P } \\ \\ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-154">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\ P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="db718-155">P_ {M1 } ~ ~ P_ {m2 } ~ ~ \кдотс ~ ~ P_ {MP}</span><span class="sxs-lookup"><span data-stu-id="db718-155">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
<span data-ttu-id="db718-156">концеbmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-156">\end{bmatrix}</span></span>
<span data-ttu-id="db718-157">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="db718-157">\end{align}</span></span>

<span data-ttu-id="db718-158">где записи $P $ $P _ {ОК } = \ sum_j M_ {иж} N_ {ЖК } $.</span><span class="sxs-lookup"><span data-stu-id="db718-158">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="db718-159">Например, запись $P _ {11 } $ является внутренним произведением первой строки $M $ с первым столбцом $N $ .</span><span class="sxs-lookup"><span data-stu-id="db718-159">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$.</span></span> <span data-ttu-id="db718-160">Обратите внимание, что поскольку вектор является просто особым случаем матрицы, это определение расширяется на умножение векторных матриц.</span><span class="sxs-lookup"><span data-stu-id="db718-160">Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="db718-161">Все матрицы, которые мы будем рассматривать, представляют собой квадратные матрицы, где число строк и столбцов равно, или векторы, которые соответствуют только $1 $ столбцам.</span><span class="sxs-lookup"><span data-stu-id="db718-161">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="db718-162">Одна из специальных квадратных матриц — это [*матрица идентификаторов*](https://en.wikipedia.org/wiki/Identity_matrix), обозначенная как $ \болдоне $ , которая содержит все его диагональные элементы, равные $1, $ а остальные элементы $ — $0:</span><span class="sxs-lookup"><span data-stu-id="db718-162">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

<span data-ttu-id="db718-163">$ $ \болдоне = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-163">$$\boldone=\begin{bmatrix}</span></span>
<span data-ttu-id="db718-164">1 ~ ~ 0 ~ ~ \кдотс ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-164">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="db718-165">0 ~ ~ 1 ~ ~ \кдотс ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-165">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="db718-166">~ ~ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-166">~~ \ddots\\\\</span></span>
<span data-ttu-id="db718-167">0 ~ ~ 0 ~ ~ \кдотс ~ ~ 1 \енд{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="db718-167">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="db718-168">Для квадратной матрицы $A $ мы говорим матрицу $B $ является [*обратным*](https://en.wikipedia.org/wiki/Invertible_matrix) , если $AB = Ба = \болдоне $ .</span><span class="sxs-lookup"><span data-stu-id="db718-168">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="db718-169">Обратная часть матрицы не должна существовать, но, если она существует, она является уникальной и обзначит ее $A ^ {-1 } $.</span><span class="sxs-lookup"><span data-stu-id="db718-169">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="db718-170">Для любой $M матрицы $ , прилегающий или сопряженный с $M $ является матрицей $N $ , которая $N _ {ИЖ } = M_ {ji } ^ \* $.</span><span class="sxs-lookup"><span data-stu-id="db718-170">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="db718-171">Смежная часть $M $ обычно обозначается $M ^ \дагжер $ .</span><span class="sxs-lookup"><span data-stu-id="db718-171">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="db718-172">Мы говорим, что матрица $U $ является [*единой*](https://en.wikipedia.org/wiki/Unitary_matrix) , если $UU ^ \дагжер = U ^ \дагжер u = \болдоне $ или эквивалентно $U ^ {-1 } = u ^ \дагжер $ .</span><span class="sxs-lookup"><span data-stu-id="db718-172">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="db718-173">Возможно, наиболее важным свойством единой матрицы является то, что они сохраняют норму вектора.</span><span class="sxs-lookup"><span data-stu-id="db718-173">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="db718-174">Это происходит из-за того, что</span><span class="sxs-lookup"><span data-stu-id="db718-174">This happens because</span></span> 

<span data-ttu-id="db718-175">$ $ \лангле v, v \рангле = v ^ \дагжер v = v ^ \дагжер U ^ {-1 } U v = v ^ \Дагжер u ^ \Дагжер u v = \Лангле U v, U v \rangle . $ $</span><span class="sxs-lookup"><span data-stu-id="db718-175">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="db718-176">$M матрицы $ говорят, что это [*хермитиан*](https://en.wikipedia.org/wiki/Hermitian_matrix) , если $M = M ^ \дагжер $ .</span><span class="sxs-lookup"><span data-stu-id="db718-176">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="db718-177">Наконец, [*продукт тензорные*](https://en.wikipedia.org/wiki/Tensor_product) (или кронеккер продукт) из двух матриц $M $ размера $m \times n $ и $N $ размера $p \тимес q $ — это более крупная матрица $P = M \otimes n $ из размера $mp \тимес НК $ и получена из $M $ и $N следующим образом $ :</span><span class="sxs-lookup"><span data-stu-id="db718-177">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

<span data-ttu-id="db718-178">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="db718-178">\begin{align}</span></span>
    <span data-ttu-id="db718-179">M \отимес N &= \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-179">M \otimes N &= \begin{bmatrix}</span></span>
        <span data-ttu-id="db718-180">M_ {11 } ~ ~ \кдотс ~ ~ M_ {1N } \\ \\ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-180">M_{11} ~~ \cdots ~~ M_{1n} \\\\ \ddots\\\\</span></span>
        <span data-ttu-id="db718-181">M_ {M1 } ~ ~ \кдотс ~ ~ M_ {MN}</span><span class="sxs-lookup"><span data-stu-id="db718-181">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    <span data-ttu-id="db718-182">концеbmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-182">\end{bmatrix}</span></span>
    <span data-ttu-id="db718-183">\отимес \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-183">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="db718-184">N_ {11 } ~ ~ \кдотс ~ ~ N_ {1Q } \\ \\ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-184">N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="db718-185">N_ {P1 } ~ ~ \кдотс ~ ~ N_ {PQ}</span><span class="sxs-lookup"><span data-stu-id="db718-185">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    <span data-ttu-id="db718-186">\енд{ bmatrix } \\ \\ &= \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-186">\end{bmatrix}\\\\ &= \begin{bmatrix}</span></span>
        <span data-ttu-id="db718-187">M_ {11 } \бегин{ bmatrix } N_ {11 } ~ ~ \кдотс ~ ~ N_ {1Q } \\ \\ \ддотс \\\\ N_ {P1 } ~ ~ \кдотс ~ ~ N_ {PQ } \енд{ bmatrix } ~ ~ \кдотс ~ ~ M_ {1N } \бегин{ bmatrix } N_ {11 } ~ ~ \кдотс ~ ~ N_ {1Q } \\ \\ \ддотс \\\\ N_ {P1 } ~ ~ \кдотс ~ ~ N_ {PQ } \енд{ bmatrix } \\ \\ \ддотс\\\\</span><span class="sxs-lookup"><span data-stu-id="db718-187">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="db718-188">M_ {M1 } \бегин{ bmatrix } N_ {11 } ~ ~ \кдотс ~ ~ N_ {1Q } \\ \\ \ддотс \\\\ N_ {P1 } ~ ~ \кдотс ~ ~ N_ {PQ } \енд{ bmatrix } ~ ~ \кдотс ~ ~ M_ {MN } \бегин{ bmatrix } N_ {11 } ~ ~ \кдотс ~ ~ N_ {1Q } \\ \\ \ддотс \\\\ N_ {P1 } ~ ~ \кдотс ~ ~ N_ {PQ } \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-188">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="db718-189">\енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="db718-189">\end{bmatrix}.</span></span>
<span data-ttu-id="db718-190">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="db718-190">\end{align}</span></span>

<span data-ttu-id="db718-191">Это лучше продемонстрировать с помощью некоторых примеров:</span><span class="sxs-lookup"><span data-stu-id="db718-191">This is better demonstrated with some examples:</span></span>

<span data-ttu-id="db718-192">\бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-192">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="db718-193">a \\ \\ b \енд{ bmatrix } \отимес \бегин{ bmatrix } c \\ \\ d \\ \\ e \енд{ bmatrix } = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-193">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix}</span></span>
        <span data-ttu-id="db718-194">a \бегин{ bmatrix } c \\ \\ d \\ \\ e \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-194">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="db718-195">\\\\[1,5 EM] b \бегин{ bmatrix } c \\ \\ d \\ \\ e \end {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-195">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    <span data-ttu-id="db718-196">концеbmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-196">\end{bmatrix}</span></span>
    <span data-ttu-id="db718-197">= \бегин{ bmatrix } a c \\ \\ a d \\ \\ e \\ \\ b c \\ \\ b d \\ \\ \endbmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-197">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="db718-198">и</span><span class="sxs-lookup"><span data-stu-id="db718-198">and</span></span>

<span data-ttu-id="db718-199">\бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-199">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="db718-200">a \ b \\ \\ c \ d \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-200">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    <span data-ttu-id="db718-201">\отимес \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-201">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="db718-202">e \ f \\ \\ g \ h \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-202">e\ f\\\\g\ h \end{bmatrix}</span></span>
     <span data-ttu-id="db718-203">= \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-203">= \begin{bmatrix}</span></span>
    <span data-ttu-id="db718-204">a \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-204">a\begin{bmatrix}</span></span>
    <span data-ttu-id="db718-205">e \ f \\\\ g \ h \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-205">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="db718-206">b \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-206">b\begin{bmatrix}</span></span>
    <span data-ttu-id="db718-207">e \ f \\\\ g \ h \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-207">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="db718-208">\\\\[1em] c \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-208">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="db718-209">e \ f \\\\ g \ h \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-209">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="db718-210">г \begin {bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-210">d\begin{bmatrix}</span></span>
    <span data-ttu-id="db718-211">e \ f \\\\ g \ h \енд{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-211">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="db718-212">концеbmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-212">\end{bmatrix}</span></span>
    <span data-ttu-id="db718-213">= \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="db718-213">= \begin{bmatrix}</span></span>
    <span data-ttu-id="db718-214">AE \ AF \ будьте \ BF \\ \\ AG \ AH \ BG \ BH \\ \\ CE \ CF \ de \ DF \\ \\ CG \ CH \ группа рассылки \ DH \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="db718-214">ae\ af\ be\ bf \\\\ ag\ ah\ bg\ bh \\\\ ce\ cf\ de\ df \\\\ cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="db718-215">Последнее полезное соглашение об обозначении, окружающее продукты тензорные, заключается в том, что для любого векторного $v $ или $M матрицы $ $v ^ {\отимес n } $ или $M ^ {\отимес n } $ является короткой рукой для $ повторяющегося тензорныеного продукта $n.</span><span class="sxs-lookup"><span data-stu-id="db718-215">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="db718-216">Пример:</span><span class="sxs-lookup"><span data-stu-id="db718-216">For example:</span></span>

<span data-ttu-id="db718-217">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="db718-217">\begin{align}</span></span>
<span data-ttu-id="db718-218">& \бегин{ bmatrix } 1 \\ \\ 0 \енд{ bmatrix } ^ {\отимес 1 } = \бегин{ bmatrix } 1 \\ \\ 0 \енд{ bmatrix } , \ккуад \begin { bmatrix } 1 \\ \\ 0 \енд{ bmatrix } ^ {\отимес 2 } = \бегин{ bmatrix } 1 \\ \\ 0 0 \\ \\ \\ \\ 0 \енд{ bmatrix } , \ккуад \begin { bmatrix } 1 \\ \\ -1 \енд{ bmatrix } ^ {\отимес 2 } = \begin{ bmatrix } 1 \\ \\ -1 \\ \\ -1 \\ \\ 1 \end{ bmatrix } , \\ \\ & \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } , \qquad \begin { bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 0 &0&0&1 \\ \\ 0 &0&1&0 \\ \\ 0 &1&0&0 \\\\ 1 &0&0&0 \end { bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="db718-218">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\ &\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}    0& 1 \\\\ 1& 0  \end{bmatrix},  \qquad\begin{bmatrix} 0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
<span data-ttu-id="db718-219">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="db718-219">\end{align}</span></span>
