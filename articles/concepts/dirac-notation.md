---
title: Обозначения Дирака
description: Сведения об использовании нотации Дирак для представления тактовых состояний и имитации операций такта.
author: QuantumWriter
uid: microsoft.quantum.concepts.dirac
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
ms.openlocfilehash: f9dddfa25e9fd1e3d8aaf92b2e3b17c96ed8b72a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269512"
---
# <a name="dirac-notation"></a><span data-ttu-id="41ebc-103">Нотация Дирак</span><span class="sxs-lookup"><span data-stu-id="41ebc-103">Dirac Notation</span></span>

<span data-ttu-id="41ebc-104">Хотя нотация векторов столбцов является повсеместной в линейной перерезке, она часто бывает очень громоздкими в тактовых вычислениях, особенно при работе с несколькими Кубитс.</span><span class="sxs-lookup"><span data-stu-id="41ebc-104">While column vector notation is ubiquitous in linear algebra, it is often cumbersome in quantum computing especially when dealing with multiple qubits.</span></span>  <span data-ttu-id="41ebc-105">Например, если определить $ \пси как $ вектор, явно не ясно, является ли $ \пси $ строкой или вектором столбца.</span><span class="sxs-lookup"><span data-stu-id="41ebc-105">For example, when we define $\psi$ to be a vector it is not explicitly clear whether $\psi$ is a row or a column vector.</span></span>  <span data-ttu-id="41ebc-106">Таким образом, если $ \фи $ и $ \пси $ являются векторами, то не менее ясно, если значение $ \фи \пси $ определено, так как формы $ \фи $ и $ \пси $ могут быть неясными в контексте.</span><span class="sxs-lookup"><span data-stu-id="41ebc-106">Thus if $\phi$ and $\psi$ are vectors then it is equally unclear if $\phi \psi$ is even defined because the shapes of $\phi$ and $\psi$ may be unclear in the context.</span></span>  <span data-ttu-id="41ebc-107">Помимо неоднозначности в фигурах векторов, выражения с простыми векторами с использованием линейной алгебраические нотации, представленной ранее, могут быть очень громоздкими.</span><span class="sxs-lookup"><span data-stu-id="41ebc-107">Beyond the ambiguity about the shapes of vectors, expressing even simple vectors using the linear algebraic notation introduced earlier can be very cumbersome.</span></span> <span data-ttu-id="41ebc-108">Например, если нам нужно описать $ состояние $n-кубит, где каждый кубит принимает значение $0, то это $ будет формально выражаться в состоянии</span><span class="sxs-lookup"><span data-stu-id="41ebc-108">For example, if we wish to describe an $n$-qubit state where each qubit takes the value $0$ then we would formally express the state as</span></span> 

<span data-ttu-id="41ebc-109">$ $ \бегин{ bmatrix } 1 \\ \\ 0 \енд{ bmatrix } \отимес \кдотс \отимес \begin { bmatrix } 1 \\ \\ 0 \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-109">$$\begin{bmatrix}1 \\\\  0 \end{bmatrix}\otimes \cdots \otimes\begin{bmatrix}1 \\\\  0 \end{bmatrix}.</span></span> $$  

<span data-ttu-id="41ebc-110">Конечно, оценка этого продукта тензорные непрактична, поскольку вектор находится в экспоненциально больших пространствах, поэтому Эта нотация фактически является лучшим описанием состояния, которое может быть предоставлено с помощью предыдущей нотации.</span><span class="sxs-lookup"><span data-stu-id="41ebc-110">Of course evaluating this tensor product is impractical because the vector lies in an exponentially large space and so this notation is in fact the best description of the state that can be given using the previous notation.</span></span>  

<span data-ttu-id="41ebc-111">[*Нотация Дирак*](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation) решает эти проблемы, предоставляя новый язык для удовлетворения точных потребностей механизма такта.</span><span class="sxs-lookup"><span data-stu-id="41ebc-111">[*Dirac notation*](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation) solves these issues by presenting a new language to fit the precise needs of quantum mechanics.</span></span>  <span data-ttu-id="41ebc-112">По этой причине мы рекомендуем читателям не просматривать примеры в этом разделе в качестве жесткого рецепта того, как описать состояния такта, а не Рекомендуйте читателю просматривать их в качестве предложений, которые можно использовать для краткого выражения тактовых идей.</span><span class="sxs-lookup"><span data-stu-id="41ebc-112">For this reason, we recommend the reader not view the examples in this section as a rigid prescription of how to describe quantum states, but rather encourage the reader to view these as suggestions that can be used to concisely express quantum ideas.</span></span>

<span data-ttu-id="41ebc-113">Существует два типа векторов в нотации Дирак: вектор *неверное* и вектор *Сисакет* , так что они именуются, так как при объединении они образуют *двусторонний или внутренний* продукт.</span><span class="sxs-lookup"><span data-stu-id="41ebc-113">There are two types of vectors in Dirac notation: the *bra* vector and the *ket* vector, so named because when put together they form a *braket* or inner product.</span></span>  <span data-ttu-id="41ebc-114">Если $ \пси $ является вектором столбцов, то его можно записать в нотации Дирак как $ \кет { \пси } $, где $ \кет { \кдот } $ означает, что это вектор столбцов единиц, т. е. вектор *Сисакет* .</span><span class="sxs-lookup"><span data-stu-id="41ebc-114">If $\psi$ is a column vector then we can write it in Dirac notation as $\ket{\psi}$, where the $\ket{\cdot}$ denotes that it is a unit column vector, i.e., a *ket* vector.</span></span>  <span data-ttu-id="41ebc-115">Аналогичным образом, вектор строки $ \пси ^ \дагжер $ выражается как $ \бра { \пси } $.</span><span class="sxs-lookup"><span data-stu-id="41ebc-115">Similarly, the row vector $\psi^\dagger$ is expressed as $\bra{\psi}$.</span></span> <span data-ttu-id="41ebc-116">Иными словами, $ \пси ^ \дагжер $ получается путем применения сложного конжугатион с пошаговым вводом к элементам перестановки $ \пси $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-116">In other words, $\psi^\dagger$ is obtained by applying entry-wise complex conjugation to the elements of the transpose of $\psi$.</span></span> <span data-ttu-id="41ebc-117">Нотация неверное-Сисакет напрямую подразумевает, что $ \бракет { \пси | \пси } $ является внутренним произведением вектора $ \пси $ с самим собой, что определяется определением $1 $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-117">The bra-ket notation directly implies that $\braket{\psi|\psi}$ is the inner product of vector $\psi$ with itself, which is by definition $1$.</span></span>  

<span data-ttu-id="41ebc-118">Более того, если $ \пси $ и $ \фи $ являются векторами состояния такта, их внутренний продукт — $ \бракет { \фи | \пси $. это } означает, что вероятность измерения состояния $ \кет { \пси } $ равна $ \кет { \фи } $ — $ | \бракет { \фи | \пси } | ^ 2 $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-118">More generally, if $\psi$ and $\phi$ are quantum state vectors their inner product is $\braket{\phi|\psi}$ which implies that the probability of measuring the state $\ket{\psi}$ to be $\ket{\phi}$ is $|\braket{\phi|\psi}|^2$.</span></span>  

<span data-ttu-id="41ebc-119">Приведенное ниже соглашение используется для описания состояний тактов, которые задают значения 0 и One (однокубитные вычислительные состояния):</span><span class="sxs-lookup"><span data-stu-id="41ebc-119">The following convention is used to describe the quantum states that encode the values of zero and one (the single-qubit computational basis states):</span></span>

<span data-ttu-id="41ebc-120">$ $ \бегин{ bmatrix } 1 \\ \\ 0 \енд{ bmatrix } = \ket{0 } , \ккуад \бегин{ bmatrix } 0 \\ \\ 1 \енд{ bmatrix } = \ket{1 } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-120">$$ \begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \ket{0},\qquad \begin{bmatrix} 0 \\\\  1 \end{bmatrix} = \ket{1}.</span></span>
$$

### <a name="example-representing-the-hadamard-operation-with-dirac-notation"></a><span data-ttu-id="41ebc-121">Пример. представление операции Хадамард с нотацией Дирак</span><span class="sxs-lookup"><span data-stu-id="41ebc-121">Example: representing the Hadamard operation with Dirac notation</span></span>

<span data-ttu-id="41ebc-122">Следующая нотация часто используется для описания состояний, которые появляющиеся результатом применения вентиля Хадамард к $ \ket{0 } $ и $ \ket{1 } $ (что соответствует векторам единиц в направлениях $ + x $ и $-x в $ БЛОЧ Sphere):</span><span class="sxs-lookup"><span data-stu-id="41ebc-122">The following notation is often used to describe the states that result from applying the Hadamard gate to $\ket{0}$ and $\ket{1}$ (which correspond to the unit vectors in the $+x$ and $-x$ directions on the Bloch sphere):</span></span>

<span data-ttu-id="41ebc-123">$ $ \frac{1 } {\sqrt{2 } } \бегин{ bmatrix } 1 \\ \\ 1 \енд{ bmatrix } = H \ket {0 } = \кет { +}, \ккуад \frac{1 } {\sqrt{2 } } \бегин{ bmatrix } 1 \\ \\ -1 \енд{ bmatrix } = H \ket {1 } = \кет { -}.</span><span class="sxs-lookup"><span data-stu-id="41ebc-123">$$ \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  1 \end{bmatrix}=H\ket{0} = \ket{+},\qquad \frac{1}{\sqrt{2}}\begin{bmatrix} 1 \\\\  -1 \end{bmatrix} =H\ket{1} = \ket{-} .</span></span>
$$

<span data-ttu-id="41ebc-124">Эти состояния также можно расширить с помощью нотации Дирак как суммы $ \ket{0 } $ и $ \ket{1 } $:</span><span class="sxs-lookup"><span data-stu-id="41ebc-124">These states can also be expanded using Dirac notation as sums of $\ket{0}$ and $\ket{1}$:</span></span>

<span data-ttu-id="41ebc-125">$ $ \кет { +} = \frac{1 } {\sqrt{2 } } (\ket{0 } + \ket{1 } ), \ккуад \кет { -} = \frac{1 } {\sqrt{2 } } (\ket{0 } -\ket{1 } ).</span><span class="sxs-lookup"><span data-stu-id="41ebc-125">$$ \ket{+} = \frac{1}{\sqrt{2}}(\ket{0} + \ket{1}),\qquad \ket{-} = \frac{1}{\sqrt{2}}(\ket{0} - \ket{1}).</span></span>
$$

### <a name="computational-basis-vectors"></a><span data-ttu-id="41ebc-126">Векторы вычислительных операций</span><span class="sxs-lookup"><span data-stu-id="41ebc-126">Computational basis vectors</span></span>
<span data-ttu-id="41ebc-127">Это показывает, почему эти состояния часто называются *вычислительными*. Каждое состояние такта всегда может выражаться в виде сумм базисных векторов вычислений, а такие суммы легко выражаются с помощью нотации Дирак.</span><span class="sxs-lookup"><span data-stu-id="41ebc-127">This demonstrates why these states are often called a *computational basis*: every quantum state can always be expressed as sums of computational basis vectors and such sums are easily expressed using Dirac notation.</span></span>  <span data-ttu-id="41ebc-128">Обратное также значение true в том, что состояния $ \кет { +} $ и $ \кет { -} $ также формируют базу для состояний тактов.</span><span class="sxs-lookup"><span data-stu-id="41ebc-128">The converse is also true in that the states $\ket{+}$ and $\ket{-}$ also form a basis for quantum states.</span></span>  <span data-ttu-id="41ebc-129">Это видно из того факта, что</span><span class="sxs-lookup"><span data-stu-id="41ebc-129">You can see this from the fact that</span></span>

<span data-ttu-id="41ebc-130">$ $ \ket{0 } = \frac{1 } {\sqrt{2 } } (\кет { +} + \кет { -}), \ккуад \ket{1 } = \frac{1 } {\sqrt{2 } } (\кет { +}-\кет { -}).</span><span class="sxs-lookup"><span data-stu-id="41ebc-130">$$ \ket{0} = \frac{1}{\sqrt{2}}(\ket{+} + \ket{-}),\qquad \ket{1} = \frac{1}{\sqrt{2}}(\ket{+} - \ket{-}).</span></span>
$$

<span data-ttu-id="41ebc-131">В качестве примера нотации Дирак рассмотрите «\braket{0 | 1 } $», который является внутренним продуктом между $0 $ и $1 $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-131">As an example of Dirac notation, consider the braket $\braket{0 | 1}$, which is the inner product between $0$ and $1$.</span></span>  <span data-ttu-id="41ebc-132">Его можно записать как</span><span class="sxs-lookup"><span data-stu-id="41ebc-132">It can be written as</span></span> 

<span data-ttu-id="41ebc-133">$ $ \braket{0 | 1 } = \бегин{ bmatrix } 1 & 0 \енд{ bmatrix } \бегин{ bmatrix } 0 \\\\ 1 \end{bmatrix} = 0. $ $</span><span class="sxs-lookup"><span data-stu-id="41ebc-133">$$\braket{0 | 1}=\begin{bmatrix} 1 & 0 \end{bmatrix}\begin{bmatrix}0\\\\ 1\end{bmatrix}=0.$$</span></span>

<span data-ttu-id="41ebc-134">Это говорит о том, что $ \ket{0 } $ и $ \ket{1 } $ являются ортогональными векторами, то есть $ \braket{0 | 1 } = \braket{1 | 0 } = 0 $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-134">This says that $\ket{0}$ and $\ket{1}$ are orthogonal vectors, meaning that $\braket{0 | 1} = \braket{1 | 0} =0$.</span></span>  <span data-ttu-id="41ebc-135">Также по определению $ \braket{0 | 0 } = \braket{1 | 1 } = 1 $ , что означает, что два вычислительных вектора также могут называться *орсонормал*.</span><span class="sxs-lookup"><span data-stu-id="41ebc-135">Also by definition $\braket{0 | 0} = \braket{1 | 1}=1$, which means that the two computational basis vectors can also be called *orthonormal*.</span></span>
<span data-ttu-id="41ebc-136">Эти свойства орсонормал будут полезны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="41ebc-136">These orthonormal properties will be useful in the following example.</span></span> <span data-ttu-id="41ebc-137">Если у нас есть состояние $ \кет { \пси } = {\frac{3 } {5 } } \ket{1 } + {\frac{4 } {5 } } \ket{0 } $, так как $ \braket{1 | 0 } = 0 $ вероятность измерения $1 $ составляет</span><span class="sxs-lookup"><span data-stu-id="41ebc-137">If we have a state $\ket{\psi} = {\frac{3}{5}} \ket{1} + {\frac{4}{5}} \ket{0}$ then because $\braket{1 | 0} =0$ the probability of measuring $1$  is</span></span>  

<span data-ttu-id="41ebc-138">$ $ \биг | \braket{1 | \пси } \биг | ^ 2 = \лефт | \frac{3 } {5 } \braket{1 | 1 } + \frac{4 } {5 } \braket{1 | 0 } \ригхт | ^ 2 = \frac{9 } {25 } . $ $</span><span class="sxs-lookup"><span data-stu-id="41ebc-138">$$\big|\braket{1 | \psi}\big|^2= \left|\frac{3}{5}\braket{1 | 1} +\frac{4}{5}\braket{1 | 0}\right|^2=\frac{9}{25}.$$</span></span> 

### <a name="tensor-product-notation"></a><span data-ttu-id="41ebc-139">Запись продукта тензорные</span><span class="sxs-lookup"><span data-stu-id="41ebc-139">Tensor product notation</span></span>
<span data-ttu-id="41ebc-140">Нотация Дирак также включает в себя неявную структуру продуктов тензорные.</span><span class="sxs-lookup"><span data-stu-id="41ebc-140">Dirac notation also includes an implicit tensor product structure within it.</span></span>  <span data-ttu-id="41ebc-141">Это важно, поскольку в тактовых вычислениях вектор состояния, описанный двумя некоррелированными тактовыми регистрами, является тензорные продуктами двух векторов состояния.</span><span class="sxs-lookup"><span data-stu-id="41ebc-141">This is important because in quantum computing, the state vector described by two uncorrelated quantum registers is the tensor products of the two state vectors.</span></span>  <span data-ttu-id="41ebc-142">Чтобы объяснить тактовую информацию, необходимо кратко описать структуру продукта тензорные или ее отсутствие.</span><span class="sxs-lookup"><span data-stu-id="41ebc-142">Concisely describing the tensor product structure, or lack thereof, is vital if you want to explain a quantum computation.</span></span>  <span data-ttu-id="41ebc-143">Структура продукта тензорные подразумевает, что мы можем написать $ \пси \отимес \фи $ для любых двух векторов состояния такта $ \фи $ и $ \пси $ как $ \кет { \пси } \кет { \фи } $, иногда явно написанных как $ \кет \пси \отимес \кет { } { \фи } $, однако по правилам написания $ \отимес $ в между векторами не требуется.</span><span class="sxs-lookup"><span data-stu-id="41ebc-143">The tensor product structure implies that we can write $\psi \otimes \phi$ for any two quantum state vectors $\phi$ and $\psi$ as $\ket{\psi} \ket{\phi}$, sometimes explicitly written as $\ket{\psi} \otimes \ket{\phi}$, however by convention writing $\otimes$ in between the vectors is unnecessary.</span></span>  <span data-ttu-id="41ebc-144">Например, состояние с двумя Кубитс, инициализированными в нулевом состоянии, присваивается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="41ebc-144">For example, the state with two qubits initialized to the zero state is given by</span></span>

<span data-ttu-id="41ebc-145">$ $ \бегин{ bmatrix } 1 \\ \\ 0 0 \\ \\ \\ \\ \енд{ bmatrix } = \бегин{ bmatrix } 1 \\ \\ 0 \енд{ bmatrix } \отимес \бегин{ bmatrix } 1 \\ \\ 0 \енд{ bmatrix } = \ket{0 } \отимес \ket{0 } = \ket{0 } \ket{0 } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-145">$$ \begin{bmatrix} 1 \\\\  0 \\\\  0 \\\\  0 \end{bmatrix}= \begin{bmatrix} 1 \\\\  0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\  0 \end{bmatrix} = \ket{0} \otimes \ket{0}= \ket{0} \ket{0}.</span></span>
$$

<span data-ttu-id="41ebc-146">Аналогично, состояние $ \кет{п } $ для integer $p $ представляет состояние такта, которое кодирует в двоичном представлении целого числа $p $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-146">Similarly,  the state $\ket{p}$ for integer $p$ represents a quantum state that encodes in binary representation the integer $p$.</span></span>  <span data-ttu-id="41ebc-147">Например, если нам нужно выразить число $5, $ используя неподписанную двоичную кодировку, мы могли бы выразить это как</span><span class="sxs-lookup"><span data-stu-id="41ebc-147">For example, if we wish to express the number $5$ using an unsigned binary encoding we could equally express it as</span></span>

<span data-ttu-id="41ebc-148">$ $ \ket{1 } \ket{0 } \ket{1 } = \ket{101 } = \ket{5 } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-148">$$ \ket{1}\ket{0}\ket{1} = \ket{101} = \ket{5}.</span></span>
$$

<span data-ttu-id="41ebc-149">В этой нотации $ \ket{0 } $ не требуется ссылаться на состояние с одним кубит, а *кубит регистр* , в котором хранится двоичная кодировка $0 $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-149">Within this notation $\ket{0}$ need not refer to a single-qubit state but rather a *qubit register* storing a binary encoding of $0$.</span></span>  <span data-ttu-id="41ebc-150">Различия между этими двумя нотациями обычно понятны из контекста.</span><span class="sxs-lookup"><span data-stu-id="41ebc-150">The differences between these two notations is usually clear from the context.</span></span>  <span data-ttu-id="41ebc-151">Это соглашение полезно для упрощения первого примера, который может быть написан одним из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="41ebc-151">This convention is useful for simplifying the first example which can be written in any of the following ways:</span></span>

<span data-ttu-id="41ebc-152">$ $ \бегин{ bmatrix } 1 \\ \\ 0 \енд{ bmatrix } \отимес \кдотс \отимес \begin { bmatrix } 1 \\ \\ 0 \енд{ bmatrix } = \ket{0 } \отимес \кдотс \отимес \ket{0 } = | 0 \cdots 0 \rangle = \ket{0 } ^ {\отимес n } = \ket{0 } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-152">$$ \begin{bmatrix}1 \\\\  0 \end{bmatrix}\otimes \cdots \otimes\begin{bmatrix}1 \\\\  0 \end{bmatrix} = \ket{0} \otimes \cdots \otimes \ket{0}= |0\cdots 0\rangle = \ket{0}^{\otimes n} = \ket{0}.</span></span>
$$

### <a name="example-describing-superposition-with-dirac-notation"></a><span data-ttu-id="41ebc-153">Пример. Описание Дирак с помощью нотации</span><span class="sxs-lookup"><span data-stu-id="41ebc-153">Example: Describing superposition with Dirac notation</span></span>
<span data-ttu-id="41ebc-154">Еще один пример того, как можно использовать нотацию Дирак для описания состояния такта, рассмотрим следующие эквивалентные способы записи состояния такта, которое является равным преположением в каждой возможной битовой строке длины $n$</span><span class="sxs-lookup"><span data-stu-id="41ebc-154">As another example of how you can use Dirac notation to describe a quantum state, consider the following equivalent ways of writing a quantum state that is an equal superposition over every possible bit string of length $n$</span></span>

<span data-ttu-id="41ebc-155">$ $ H ^ {\отимес n } \ket{0 } = \frac{1 } {2 ^ {n/2 } } \ sum_ {j = 0 } ^ {2 ^ n-1 } \кет{ж } = \кет { +} ^ {\отимес n } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-155">$$ H^{\otimes n} \ket{0} = \frac{1}{2^{n/2}} \sum_{j=0}^{2^n-1} \ket{j} = \ket{+}^{\otimes n}.</span></span>
$$

<span data-ttu-id="41ebc-156">Здесь может возникнуть вопрос, почему сумма проходит от $0 $ до $2 ^ {n } -1 $ для $n $ бит.</span><span class="sxs-lookup"><span data-stu-id="41ebc-156">Here you may wonder why the sum goes from $0$ to $2^{n}-1$ for $n$ bits.</span></span>  <span data-ttu-id="41ebc-157">Прежде всего, обратите внимание на то, что существует $2 ^ {n } $ различных конфигураций, которые $ могут потребоваться для $n BITS.</span><span class="sxs-lookup"><span data-stu-id="41ebc-157">First note that there are $2^{n}$ different configurations that $n$ bits can take.</span></span>  <span data-ttu-id="41ebc-158">Это можно увидеть, отметив, что один бит может принимать $2 $ значений, но два бита могут принимать $ значения $4 и т. д.</span><span class="sxs-lookup"><span data-stu-id="41ebc-158">You can see this by noting that one bit can take $2$ values but two bits can take $4$ values and so forth.</span></span> <span data-ttu-id="41ebc-159">Как правило, это означает, что существует $2 ^ n $ различных возможных битовых строк, но наибольшее значение, закодированное в любом из них $1 \cdots 1 = 2 ^ n-1 $ и, следовательно, является верхним пределом суммы.</span><span class="sxs-lookup"><span data-stu-id="41ebc-159">In general, this means that there are $2^n$ different possible bit strings but the largest value encoded in any of them $1\cdots 1=2^n-1$ and hence it is the upper limit for the sum.</span></span>
<span data-ttu-id="41ebc-160">Обратите внимание, что в этом примере мы не использовали $ \кет { +} ^ {\отимес n } = \кет { +} $ в аналогии с $ \ket{0 } ^ {\отимес n } = \ket{0 $, } так как это соглашение об нотации обычно резервируется для вычислительного состояния с каждым кубит, инициализированным нулем.</span><span class="sxs-lookup"><span data-stu-id="41ebc-160">As a side note, in this example we did not use $\ket{+}^{\otimes n}=\ket{+}$ in analogy to $\ket{0}^{\otimes n} = \ket{0}$ because this notational convention is usually reserved for the computational basis state with every qubit initialized to zero.</span></span>  <span data-ttu-id="41ebc-161">Хотя такое соглашение будет разумным в этом случае, оно не будет использоваться в литературе для обработки тактов.</span><span class="sxs-lookup"><span data-stu-id="41ebc-161">While such a convention would be sensible in this case, it is not employed in the quantum computing literature.</span></span>

### <a name="expressing-linearity-with-dirac-notation"></a><span data-ttu-id="41ebc-162">Выражать линейность с помощью нотации Дирак</span><span class="sxs-lookup"><span data-stu-id="41ebc-162">Expressing linearity with Dirac notation</span></span>
<span data-ttu-id="41ebc-163">Еще одна удобная функция нотации Дирак — это тот факт, что он линейный.</span><span class="sxs-lookup"><span data-stu-id="41ebc-163">Another nice feature of Dirac notation is the fact that it is linear.</span></span>  <span data-ttu-id="41ebc-164">Если мы хотим писать для любых четырех векторов состояния такта,</span><span class="sxs-lookup"><span data-stu-id="41ebc-164">If we wish to write for any four quantum state vectors,</span></span> 

<span data-ttu-id="41ebc-165">$ $ (\алфа \кет { \пси } + \бета \ket { \фи } ) \отимес (\гамма \кет { \чи } + \делта \кет { \омега } ) = \алфа \gamma \кет { \пси } \кет { \chi } + \alpha \delta \ket { \psi } \ket { \omega } + \beta \gamma \ket { \Phi } \ket { \chi } \beta \delta \ket { \Phi } \ket { \omega } . $ $</span><span class="sxs-lookup"><span data-stu-id="41ebc-165">$$(\alpha \ket{\psi} +\beta\ket{\phi})\otimes (\gamma \ket{\chi} + \delta \ket{\omega})= \alpha\gamma \ket{\psi}\ket{\chi} + \alpha\delta \ket{\psi}\ket{\omega}+\beta\gamma\ket{\phi}\ket{\chi}+\beta\delta\ket{\phi}\ket{\omega}.$$</span></span>

<span data-ttu-id="41ebc-166">Это означает, что вы можете распределить нотацию продукта тензорные в нотации Дирак, чтобы взять тензорные продукты между векторами состояния, которые будут выглядеть так же, как обычное умножение.</span><span class="sxs-lookup"><span data-stu-id="41ebc-166">That is to say, you can distribute the tensor product notation in Dirac notation so that taking tensor products between state vectors ends up looking just like ordinary multiplication.</span></span>

<span data-ttu-id="41ebc-167">Векторы неверное соответствуют тому же соглашению, что и векторы Сисакет.</span><span class="sxs-lookup"><span data-stu-id="41ebc-167">Bra vectors follow a similar convention to ket vectors.</span></span>  <span data-ttu-id="41ebc-168">Например, вектор $ \бра { \пси } \бра { \фи } $ эквивалентен вектору состояния $ \пси ^ \дагжер \отимес \фи ^ \дагжер = (\пси \otimes \фи) ^ \дагжер $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-168">For example, the vector $\bra{\psi}\bra{\phi}$ is equivalent to the state vector $\psi^\dagger \otimes \phi^\dagger=(\psi\otimes \phi)^\dagger$.</span></span> <span data-ttu-id="41ebc-169">Если Сисакет Vector $ \кет { \пси } $ имеет значение $ \алфа \ket{0 } + \бета \ket{1 } $, то векторная версия неверное Vector — $ \бра { \пси } = \кет { \пси } ^ \дагжер = (\bra{0 } \алфа ^ \* + \bra{1 } \бета ^ \*) $.</span><span class="sxs-lookup"><span data-stu-id="41ebc-169">If the ket vector $\ket{\psi}$ is $\alpha \ket{0} + \beta \ket{1}$ then the bra vector version of the vector is $\bra{\psi}=\ket{\psi}^\dagger = (\bra{0}\alpha^\* +\bra{1}\beta^\*)$.</span></span>

<span data-ttu-id="41ebc-170">В качестве примера представьте себе, что мы хотим рассчитать вероятность измерения состояния $ \кет { \пси } = \frac{3 } {5 } \ket{1 } + \frac{4 } {5 } \ket{0 } $ с помощью тактовой программы для измерения состояний как $ \кет { +} $ или $ \кет { -} $.</span><span class="sxs-lookup"><span data-stu-id="41ebc-170">As an example, imagine that we wish to calculate the probability of measuring the state $\ket{\psi} = \frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}$ using a quantum program for measuring states to be either $\ket{+}$ or $\ket{-}$.</span></span> <span data-ttu-id="41ebc-171">Затем вероятность того, что устройство выводит состояние $ \кет { -} $</span><span class="sxs-lookup"><span data-stu-id="41ebc-171">Then the probability that the device would output that the state is $\ket{-}$ is</span></span> 

<span data-ttu-id="41ebc-172">$ $ | \бракет { -| \пси } | ^ 2 = \лефт | \frac{1 } {\sqrt{2 } } (\bra{0 } -\bra{1 } ) (\frac{3 } {5 } \ket{1 } + \frac{4 } {5 } \ket{0 } ) \ригхт | ^ 2 = \лефт | -\frac{3 } {5 \sqrt {2 } } + \frac{4 } {5 \sqrt {2 } } \ригхт | ^ 2 = \frac{1 } {50 } . $ $</span><span class="sxs-lookup"><span data-stu-id="41ebc-172">$$|\braket{- | \psi}|^2= \left|\frac{1}{\sqrt{2}}(\bra{0} - \bra{1})(\frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}) \right|^2=\left|-\frac{3}{5\sqrt{2}} + \frac{4}{5\sqrt{2}}\right|^2=\frac{1}{50}.$$</span></span>

<span data-ttu-id="41ebc-173">Тот факт, что отрицательный знак отображается в вычислении вероятности, является проявлением тактовых помех, которые являются одним из механизмов, с помощью которых тактовые вычисления получают преимущества по сравнению с классическими вычислениями.</span><span class="sxs-lookup"><span data-stu-id="41ebc-173">The fact that the negative sign appears in the calculation of the probability is a manifestation of quantum interference, which is one of the mechanisms by which quantum computing gains advantages over classical computing.</span></span>

## <a name="ketbra-or-outer-product"></a><span data-ttu-id="41ebc-174">кетбра или внешний продукт</span><span class="sxs-lookup"><span data-stu-id="41ebc-174">ketbra or outer product</span></span>
<span data-ttu-id="41ebc-175">Последним элементом, который стоит обсудить в нотации Дирак, является *кетбра* или внешний продукт.</span><span class="sxs-lookup"><span data-stu-id="41ebc-175">The final item worth discussing in Dirac notation is the *ketbra* or outer product.</span></span>  <span data-ttu-id="41ebc-176">Внешний продукт представлен в нотациях Дирак как $ \кет { \пси } \бра { \фи } $ и иногда называется кетбрас, так как Брас и КЕТС встречаются в обратном порядке как Бракетс.</span><span class="sxs-lookup"><span data-stu-id="41ebc-176">The outer product is represented within Dirac notations as $\ket{\psi} \bra{\phi}$, and sometimes called ketbras because the bras and kets occur in the opposite order as brakets.</span></span>  <span data-ttu-id="41ebc-177">Внешний продукт определяется посредством умножения матрицы как $ \кет { \пси } \бра { \фи } = \пси \фи ^ \дагжер $ для векторов состояния такта $ \пси $ и $ \фи $ .</span><span class="sxs-lookup"><span data-stu-id="41ebc-177">The outer product is defined via matrix multiplication as $\ket{\psi} \bra{\phi} = \psi \phi^\dagger$ for quantum state vectors $\psi$ and $\phi$.</span></span>  <span data-ttu-id="41ebc-178">Самый простой и, вероятно, наиболее распространенный пример этой нотации:</span><span class="sxs-lookup"><span data-stu-id="41ebc-178">The simplest, and arguably most common example of this notation, is</span></span>

<span data-ttu-id="41ebc-179">$ $ \ket{0 } \bra{0 } = \бегин{ bmatrix } 1 \\\\ 0 \енд{ bmatrix } \бегин{ bmatrix } 1&0 \енд{ bmatrix } = \бегин{ bmatrix } 1 &0 \\\\ 0 &0 \end{bmatrix} \ккуад \ket{1 } \bra{1 } = \бегин{ bmatrix } 0 \\\\ 1 \енд{ bmatrix } \бегин{ bmatrix } 0&1 \енд{ bmatrix } = \бегин{ bmatrix } 0 &0 \\\\ 0 &1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="41ebc-179">$$ \ket{0} \bra{0} = \begin{bmatrix}1\\\\ 0 \end{bmatrix}\begin{bmatrix}1&0 \end{bmatrix}= \begin{bmatrix}1 &0\\\\ 0 &0\end{bmatrix} \qquad \ket{1} \bra{1} = \begin{bmatrix}0\\\\ 1 \end{bmatrix}\begin{bmatrix}0&1 \end{bmatrix}= \begin{bmatrix}0 &0\\\\ 0 &1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="41ebc-180">Кетбрас часто называются проекторами, так как они проецирует состояние такта в фиксированное значение.</span><span class="sxs-lookup"><span data-stu-id="41ebc-180">Ketbras are often called projectors because they project a quantum state onto a fixed value.</span></span>  <span data-ttu-id="41ebc-181">Так как эти операции не являются едиными (и даже не сохраняют нормы вектора), они должны быть не удивительно, что тактовый компьютер не может детерминированно применять проектор.</span><span class="sxs-lookup"><span data-stu-id="41ebc-181">Since these operations are not unitary (and do not even preserve the norm of a vector), it should come as no surprise that a quantum computer cannot deterministically apply a projector.</span></span>  <span data-ttu-id="41ebc-182">Однако Проекторы представляют собой прекрасную задачу, описывающую действие, которое измерение имеет в состоянии такта.</span><span class="sxs-lookup"><span data-stu-id="41ebc-182">However projectors do a beautiful job of describing the action that measurement has on a quantum state.</span></span>  <span data-ttu-id="41ebc-183">Например, если измерение State $ \кет { \пси } $ должно быть $0, то результатом такого $ преобразования является то, что его состояние является результатом измерения.</span><span class="sxs-lookup"><span data-stu-id="41ebc-183">For example, if we measure a state $\ket{\psi}$ to be $0$ then the resulting transformation that the state experiences as a result of the measurement is</span></span>

  <span data-ttu-id="41ebc-184">$ $ \кет { \пси } \ригхтарров \фрак { (\ket{0 } \bra{0 } ) \кет { \пси } } {| \braket{0 | \пси } |} = \ket{0 } , $ $</span><span class="sxs-lookup"><span data-stu-id="41ebc-184">$$\ket{\psi} \rightarrow \frac{(\ket{0} \bra{0})\ket{\psi}}{|\braket{0 | \psi}|}= \ket{0},$$</span></span>

<span data-ttu-id="41ebc-185">как и в случае, если необходимо измерить состояние и найти его как $ \ket{0 } $.</span><span class="sxs-lookup"><span data-stu-id="41ebc-185">as one expects if you were to measure the state and find it to be $\ket{0}$.</span></span>  <span data-ttu-id="41ebc-186">Чтобы повторно выполнить итерацию, такие Проекторы не могут быть применены к состоянию на компьютере-такте детерминированно.</span><span class="sxs-lookup"><span data-stu-id="41ebc-186">To reiterate, such projectors cannot be applied on a state in a quantum computer deterministically.</span></span>  <span data-ttu-id="41ebc-187">Вместо этого они могут быть применены случайным образом, при этом результат $ \ket{0 } $ появлялся с фиксированной вероятностью.</span><span class="sxs-lookup"><span data-stu-id="41ebc-187">Instead, they can at best be applied randomly with the result $\ket{0}$ appearing with some fixed probability.</span></span>  <span data-ttu-id="41ebc-188">Вероятность того, что такое измерение будет продолжено, можно записать как значение ожидания для тактовой репроектора в состоянии.</span><span class="sxs-lookup"><span data-stu-id="41ebc-188">The probability of such a measurement succeeding can be written as the expectation value of the quantum projector in the state</span></span>

<span data-ttu-id="41ebc-189">$ $ \бра { \пси } (\ket{0 } \bra{0 } ) \кет { \пси } = | \бракет { \пси | 0 } | ^ 2, $ $</span><span class="sxs-lookup"><span data-stu-id="41ebc-189">$$ \bra{\psi} (\ket{0} \bra{0})\ket{\psi} = |\braket{\psi | 0}|^2, $$</span></span>

<span data-ttu-id="41ebc-190">Это показывает, что Проекторы просто предоставляют новый способ представления процесса измерения.</span><span class="sxs-lookup"><span data-stu-id="41ebc-190">which illustrates that projectors simply give a new way of expressing the measurement process.</span></span>

<span data-ttu-id="41ebc-191">Если вместо этого мы рекомендуем измерять первый кубит состояния кубит до $1, $ мы можем также описать этот процесс, используя проекторы и нотацию Дирак:</span><span class="sxs-lookup"><span data-stu-id="41ebc-191">If instead we consider measuring the first qubit of a multi-qubit state to be $1$ then we can also describe this process conveniently using projectors and Dirac notation:</span></span>

<span data-ttu-id="41ebc-192">$ $ P (\текст{Фирст кубит = 1 } ) = \бра { \пси } \лефт (\ket{1 } \bra{1 } \отимес \болдоне ^ {\отимес n-1 } \ригхт) \кет { \пси } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-192">$$ P(\text{first qubit = 1})= \bra{\psi}\left(\ket{1}\bra{1}\otimes \boldone^{\otimes n-1}\right) \ket{\psi}.</span></span>
$$

<span data-ttu-id="41ebc-193">Здесь матрица идентификаторов можно легко написать в нотации Дирак.</span><span class="sxs-lookup"><span data-stu-id="41ebc-193">Here the identity matrix can be conveniently written in Dirac notation as</span></span>

<span data-ttu-id="41ebc-194">$ $ \болдоне = \ket{0 } \bra{0 } + \ket{1 } \bra{1 } = \бегин{ bmatrix } 1&0 \\\\ 0&1 \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-194">$$ \boldone = \ket{0} \bra{0}+\ket{1} \bra{1}= \begin{bmatrix}1&0\\\\ 0&1 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="41ebc-195">В случае с двумя Кубитс проектор можно расширить, как</span><span class="sxs-lookup"><span data-stu-id="41ebc-195">For the case where there are two-qubits the projector can be expanded as</span></span> 

<span data-ttu-id="41ebc-196">$ $ \ket{1 } \bra{1 } \отимес \ид = \ket{1 } \bra{1 } \отимес (\ket{0 } \bra{0 } + \ket{1 } \bra{1 } ) = \ket{10 } \bra{10 } + \ket{11 } \bra{11 } .</span><span class="sxs-lookup"><span data-stu-id="41ebc-196">$$ \ket{1} \bra{1} \otimes \id = \ket{1}\bra{1} \otimes (\ket{0} \bra{0}+\ket{1} \bra{1})= \ket{10}\bra{10} + \ket{11}\bra{11}.</span></span>
$$

<span data-ttu-id="41ebc-197">Затем можно увидеть, что это согласуется с обсуждением вероятностей измерений для состояний мултикубит, использующих нотацию вектора столбцов:</span><span class="sxs-lookup"><span data-stu-id="41ebc-197">We can then see that this is consistent with the discussion about measurement likelihoods for multiqubit states using column-vector notation:</span></span>

<span data-ttu-id="41ebc-198">$ $ P (\текст{Фирст кубит = 1 } ) = \пси ^ \дагжер (e \_ {10} e \_ {10 } ^ \дагжер + e \_ {11} e \_ {11 } ^ \дагжер) \пси = | e \_ {10 } ^ \дагжер \пси | ^ 2 + | e \_ {11 } ^ \дагжер \пси | ^ 2, $ $</span><span class="sxs-lookup"><span data-stu-id="41ebc-198">$$ P(\text{first qubit = 1})= \psi^\dagger (e\_{10}e\_{10}^\dagger + e\_{11}e\_{11}^\dagger)\psi = |e\_{10}^\dagger \psi|^2 + |e\_{11}^\dagger \psi|^2, $$</span></span>

<span data-ttu-id="41ebc-199">который соответствует обсуждению кубит измерения.</span><span class="sxs-lookup"><span data-stu-id="41ebc-199">which matches the multi-qubit measurement discussion.</span></span>  <span data-ttu-id="41ebc-200">Тем не менее, обобщение этого результата в кубит случае немного более проста для выражения с использованием нотации Дирак, чем нотация вектора столбцов, и полностью эквивалентно предыдущему излечения.</span><span class="sxs-lookup"><span data-stu-id="41ebc-200">The generalization of this result to the multi-qubit case, however, is slightly more straightforward to express using Dirac notation than column-vector notation, and is entirely equivalent to the previous treatment.</span></span>

## <a name="density-operators"></a><span data-ttu-id="41ebc-201">Операторы плотности</span><span class="sxs-lookup"><span data-stu-id="41ebc-201">Density operators</span></span>

<span data-ttu-id="41ebc-202">Еще один полезный оператор для выражения с использованием нотации Дирак — это *оператор плотности*, иногда также называемый *оператором State*.</span><span class="sxs-lookup"><span data-stu-id="41ebc-202">Another useful operator to express using Dirac notation is a *density operator*, sometimes also known as a *state operator*.</span></span>
<span data-ttu-id="41ebc-203">Оператор плотности для вектора состояния такта имеет вид $ \рхо = \кет { \пси } \бра { \пси } $.</span><span class="sxs-lookup"><span data-stu-id="41ebc-203">A density operator for a quantum state vector takes the form $\rho = \ket{\psi} \bra{\psi}$.</span></span>
<span data-ttu-id="41ebc-204">Эта концепция, представляющая состояние как матрица, а не вектор, зачастую удобна, поскольку она предоставляет удобный способ представления вычислений вероятности, а также позволяет описать как статистическую неопределенность, так и неопределенность такта в одном и том же формальном процессе.</span><span class="sxs-lookup"><span data-stu-id="41ebc-204">This concept of representing the state as a matrix, rather than a vector, is often convenient because it gives a convenient way of representing probability calculations, and also allows one to describe both statistical uncertainty as well as quantum uncertainty within the same formalism.</span></span>
<span data-ttu-id="41ebc-205">Общие операторы состояния такта, а не векторы, являются повсеместными в некоторых областях тактовых вычислений, но не являются обязательными для понимания основ поля.</span><span class="sxs-lookup"><span data-stu-id="41ebc-205">General quantum state operators, rather than vectors, are ubiquitous in some areas of quantum computing but are not necessary to understand the basics of the field.</span></span>
<span data-ttu-id="41ebc-206">Для заинтересованного читателя рекомендуется ознакомиться с одной из справочных книг, предоставленных в, [для получения дополнительных сведений](xref:microsoft.quantum.more-information).</span><span class="sxs-lookup"><span data-stu-id="41ebc-206">For the interested reader, we recommend reading one of the reference books provided in [For more information](xref:microsoft.quantum.more-information).</span></span>

## <a name="q-gate-sequences-equivalent-to-quantum-states"></a><span data-ttu-id="41ebc-207">Q число последовательностей шлюзов эквивалентно состояниям такта</span><span class="sxs-lookup"><span data-stu-id="41ebc-207">Q# gate sequences equivalent to quantum states</span></span>
<span data-ttu-id="41ebc-208">В заключение стоит обратить внимание на тактовую нотацию и язык программирования Q #: в SES этого документа мы упоминали, что состояние такта является фундаментальным объектом информации в тактовых вычислениях.</span><span class="sxs-lookup"><span data-stu-id="41ebc-208">A final point worth raising about quantum notation and the Q# programming language: at the onset of this document we mentioned that the quantum state is the fundamental object of information in quantum computing.</span></span>  <span data-ttu-id="41ebc-209">В то же самое, в Q # нет понятия о состоянии такта.</span><span class="sxs-lookup"><span data-stu-id="41ebc-209">It may then come as a surprise that in Q# there is no notion of a quantum state.</span></span>  <span data-ttu-id="41ebc-210">Вместо этого все состояния описываются только операциями, используемыми для их подготовки.</span><span class="sxs-lookup"><span data-stu-id="41ebc-210">Instead, all states are described only by the operations used to prepare them.</span></span>  <span data-ttu-id="41ebc-211">Предыдущий пример — это отличная иллюстрация этого.</span><span class="sxs-lookup"><span data-stu-id="41ebc-211">The previous example is an excellent illustration of this.</span></span>  <span data-ttu-id="41ebc-212">Вместо того чтобы выражать единую подстановку для каждой строки тактового бита в регистре, результат можно представить как $H ^ {\отимес n } \ket{0 } $.</span><span class="sxs-lookup"><span data-stu-id="41ebc-212">Rather than expressing a uniform superposition over every quantum bit string in a register, we can represent the result as $H^{\otimes n} \ket{0}$.</span></span>  <span data-ttu-id="41ebc-213">Это экспоненциально-короткое описание состояния не только является преимуществом, которое можно реализовать в классическом виде, но оно также четко определяет операции, необходимые для распространения в стек программного обеспечения для реализации алгоритма.</span><span class="sxs-lookup"><span data-stu-id="41ebc-213">This exponentially shorter description of the state not only has the advantage that we can classically reason about it, but it also concisely defines the operations needed to be propagated through the software stack to implement the algorithm.</span></span>  <span data-ttu-id="41ebc-214">По этой причине функция Q # предназначена для создания последовательностей шлюзов, а не состояний тактов. Однако на теоретическом уровне две перспективы эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="41ebc-214">For this reason, Q# is designed to emit gate sequences rather than quantum states; however, at a theoretical level the two perspectives are equivalent.</span></span>
