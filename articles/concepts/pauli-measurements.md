---
title: Паули измерения
description: Узнайте, как работать с одной и несколькими кубит Паули измерениями.
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
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
ms.openlocfilehash: 7f10c4ad5eb325da97552d60ff47ea89a699f08d
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269479"
---
# <a name="pauli-measurements"></a><span data-ttu-id="dbfb4-103">Паули измерения</span><span class="sxs-lookup"><span data-stu-id="dbfb4-103">Pauli Measurements</span></span>

<span data-ttu-id="dbfb4-104">В предыдущих обсуждениях мы посвящены измерениям вычислительной единицы.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-104">In the previous discussions, we have focused on computational basis measurements.</span></span>
<span data-ttu-id="dbfb4-105">На самом деле, в тактовых вычислениях существуют и другие распространенные измерения, которые удобны для вычисления измерений базисных показателей.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-105">In fact, there are other common measurements that occur in quantum computing that, from a notational perspective, are convenient to express in terms of computational basis measurements.</span></span>
<span data-ttu-id="dbfb4-106">При работе с Q # наиболее распространенные измерения, с которыми вы будете работать, скорее всего, будут *Паули измерениями*, которые обобщает базовые показатели вычислений, чтобы включить измерения в другие базовые показатели, и четность между различными Кубитс.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-106">As you work with Q#, the most common kind of measurements that you'll run into will likely be *Pauli measurements*, which generalize computational basis measurements to include measurements in other bases, and of parity between different qubits.</span></span>
<span data-ttu-id="dbfb4-107">В таких случаях часто обсуждается измерение оператора Паули, в целом оператор, например $X, Y, Z $ или $Z \otimes Z, x \otimes x, x \otimes Y $ и т. д.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-107">In such cases, it is common to discuss measuring a Pauli operator, in general an operator such as $X,Y,Z$ or $Z\otimes Z, X\otimes X, X\otimes Y$, and so forth.</span></span>

> [!TIP]
> <span data-ttu-id="dbfb4-108">В Q # операторы Multi-кубит Паули обычно представлены массивами типа `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-108">In Q#, multi-qubit Pauli operators are generally represented by arrays of type `Pauli[]`.</span></span>
> <span data-ttu-id="dbfb4-109">Например, чтобы представить $X \отимес Z \отимес Y $ , можно использовать массив `[PauliX, PauliZ, PauliY]` .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-109">For example, to represent $X \otimes Z \otimes Y$, you can use the array `[PauliX, PauliZ, PauliY]`.</span></span>

<span data-ttu-id="dbfb4-110">Обсуждение измерения с точки зрения операторов Паули особенно распространено во подполе исправления ошибок такта.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-110">Discussing measurement in terms of Pauli operators is especially common in the subfield of quantum error correction.</span></span>
<span data-ttu-id="dbfb4-111">В Q # Мы соблюдаем аналогичное соглашение. Теперь мы объясним это альтернативное представление измерений.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-111">In Q#, we follow a similar convention; we now explain this alternative view of measurements.</span></span>

<span data-ttu-id="dbfb4-112">Прежде чем углубляться в подробные сведения о том, как представить Паули измерение, полезно подумать о том, какой размер одного кубита в тактовой частоте в состоянии такта.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-112">Before delving into the details of how to think of a Pauli measurement, it is useful to think about what measuring a single qubit inside a quantum computer does to the quantum state.</span></span>
<span data-ttu-id="dbfb4-113">Представьте, что у нас есть $ состояние такта $n-кубит. затем измерение одного кубит сразу же правила выходит за пределы возможностей $2 ^ n $ , которые могут быть в состоянии.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-113">Imagine that we have an $n$-qubit quantum state; then measuring one qubit immediately rules out half of the $2^n$ possibilities that state could be in.</span></span>
<span data-ttu-id="dbfb4-114">Иными словами, измерение проецирует состояние такта на одну из двух половинных пробелов.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-114">In other words, the measurement projects the quantum state onto one of two half-spaces.</span></span>
<span data-ttu-id="dbfb4-115">Мы можем обобщить способ, который мы думаем о измерении, чтобы отразить этот интуиция.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-115">We can generalize the way we think about measurement to reflect this intuition.</span></span>

<span data-ttu-id="dbfb4-116">Для краткого выделения этих подпространств требуется язык для их описания.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-116">In order to concisely identify these subspaces, we need a language for describing them.</span></span>
<span data-ttu-id="dbfb4-117">Один из способов описания двух подразделений состоит в том, что они указываются через матрицу с двумя уникальными еиженвалуес, принятыми в соответствии с соглашением $ \пм 1 $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-117">One way to describe the two subspaces is by specifying them through a matrix that just has two unique eigenvalues, taken by convention to be $\pm 1$.</span></span>
<span data-ttu-id="dbfb4-118">Простой пример описания подпространства таким образом можно $Z $ :</span><span class="sxs-lookup"><span data-stu-id="dbfb4-118">For a simple example of describing subspaces in this way, consider $Z$:</span></span>

<span data-ttu-id="dbfb4-119">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-119">$$ \begin{align}</span></span>
  <span data-ttu-id="dbfb4-120">Z & = \бегин{ bmatrix } 1 & 0 \\ \\ 0 &-1 \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-120">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="dbfb4-121">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-121">\end{align}</span></span>
$$

<span data-ttu-id="dbfb4-122">Прочитав диагональные элементы матрицы Паули-$Z $ , можно увидеть, что $Z $ имеет два основе собственных векторов, $ \ket{0 } $ и $ \ket{1 } $, с соответствующими еиженвалуес $ \пм 1 $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-122">By reading the diagonal elements of the Pauli-$Z$ matrix, we can see that $Z$ has two eigenvectors, $\ket{0}$ and $\ket{1}$, with corresponding eigenvalues $\pm 1$.</span></span>
<span data-ttu-id="dbfb4-123">Таким образом, если мы измеряем кубит и получаем `Zero` (соответствующий состоянию $ \ket{0 } $), мы понимаем, что в качестве состояния нашего кубит используется $ еиженстате $ оператора $Z.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-123">Thus, if we measure the qubit and obtain `Zero` (corresponding to the state $\ket{0}$), we know that the state of our qubit is a $+1$ eigenstate of the $Z$ operator.</span></span>
<span data-ttu-id="dbfb4-124">Аналогичным образом, если мы получаем `One` , мы понимаем, что состояние нашего кубит — $-1 $ еиженстате $Z $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-124">Similarly, if we obtain `One`, we know that the state of our qubit is a $-1$ eigenstate of $Z$.</span></span>
<span data-ttu-id="dbfb4-125">Этот процесс упоминается в языке Паули измерений как «измерение Паули $Z» $ и полностью эквивалентен вычислению базового измерения.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-125">This process is referred to in the language of Pauli measurements as "measuring Pauli $Z$," and is entirely equivalent to performing a computational basis measurement.</span></span>

<span data-ttu-id="dbfb4-126">Любая \times $ матрица $2 2, которая является единым преобразованием $Z $ также удовлетворяет этим критериям.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-126">Any $2\times 2$ matrix that is a unitary transformation of $Z$ also satisfies this criteria.</span></span>
<span data-ttu-id="dbfb4-127">То есть можно также использовать матрицу $A = U ^ \дагжер Z U $ , где $U $ является любой другой единой матрицей, чтобы получить матрицу, определяющую два результата измерения в его основе собственных векторов $ \пм 1 $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-127">That is, we could also use a matrix $A=U^\dagger Z U$, where $U$ is any other unitary matrix, to give a matrix that defines the two outcomes of a measurement in its $\pm 1$ eigenvectors.</span></span>
<span data-ttu-id="dbfb4-128">Нотация измерений Паули ссылается на это единое эквивалентное определение $X, Y, Z $ в качестве эквивалентных измерений, которые можно сделать для получения информации из кубит.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-128">The notation of Pauli measurements references this unitary equivalence by identifying $X,Y,Z$ measurements as equivalent measurements that one could do to gain information from a qubit.</span></span>
<span data-ttu-id="dbfb4-129">Для удобства эти измерения приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-129">These measurements are given below for convenience.</span></span>


|<span data-ttu-id="dbfb4-130">Измерение Паули</span><span class="sxs-lookup"><span data-stu-id="dbfb4-130">Pauli Measurement</span></span>  |<span data-ttu-id="dbfb4-131">Единое преобразование</span><span class="sxs-lookup"><span data-stu-id="dbfb4-131">Unitary transformation</span></span>  |
|-------------------|------------------------|
| <span data-ttu-id="dbfb4-132">$Z$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-132">$Z$</span></span>               | <span data-ttu-id="dbfb4-133">\болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-133">$\boldone$</span></span>             |
| <span data-ttu-id="dbfb4-134">$X$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-134">$X$</span></span>               | <span data-ttu-id="dbfb4-135">$H$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-135">$H$</span></span>                    |
| <span data-ttu-id="dbfb4-136">$Y$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-136">$Y$</span></span>               | <span data-ttu-id="dbfb4-137">$HS ^ {\дагжер}$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-137">$HS^{\dagger}$</span></span>         |

<span data-ttu-id="dbfb4-138">То есть при использовании этого языка "мера $Y $ " эквивалентен применению $HS ^ \дагжер, $ а затем измерению на основе вычислений, где [`S`](xref:microsoft.quantum.intrinsic.s) — это внутренняя операция такта, которая иногда называется фазой фазы, и может быть смоделирована единой матрицей.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-138">That is, using this language, "measure $Y$" is equivalent to applying $HS^\dagger$ and then measuring in the computational basis, where [`S`](xref:microsoft.quantum.intrinsic.s) is an intrinsic quantum operation sometimes called the "phase gate," and can be simulated by the unitary matrix</span></span>

<span data-ttu-id="dbfb4-139">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-139">$$ \begin{align}</span></span>
    <span data-ttu-id="dbfb4-140">S = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-140">S = \begin{bmatrix}</span></span>
        <span data-ttu-id="dbfb4-141">1 & 0 \\ \\ 0 & я \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-141">1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="dbfb4-142">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-142">\end{align}</span></span>
$$

<span data-ttu-id="dbfb4-143">Он также эквивалентен применению $HS ^ \дагжер $ к вектору состояния такта, а затем измерению $Z $ , чтобы следующая операция эквивалентна `Measure([PauliY], [q])` :</span><span class="sxs-lookup"><span data-stu-id="dbfb4-143">It is also equivalent to applying $HS^\dagger$ to the quantum state vector and then measuring $Z$, such that the following operation is equivalent to `Measure([PauliY], [q])`:</span></span>

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

<span data-ttu-id="dbfb4-144">Затем правильное состояние будет найдено путем преобразования обратно в вычислительную базу, что соответствует применению $SH $ к вектору состояния такта; в приведенном выше фрагменте преобразование обратно в вычислительную базу выполняется автоматически при использовании `within … apply` блока.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-144">The correct state would then be found by transforming back to the computational basis, which amounts to applying $SH$ to the quantum state vector; in the above snippet, the transformation back to the computational basis is handled automatically by the use of the `within … apply` block.</span></span>

<span data-ttu-id="dbfb4-145">В Q # мы говорим результат---то есть классическая информация, извлеченная из взаимодействия с---ом состояния, имеет `Result` значение $j \ин \\ {\Тексттт{зеро } , \тексттт{Оне } \\ } $, указывающее, находится ли результат в выражении $ (-1) ^ j $ еиженспаце оператора Паули.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-145">In Q#, we say the outcome---that is, the classical information extracted from interacting with the state---is given by a `Result` value $j \in \\{\texttt{Zero}, \texttt{One}\\}$ indicating if the result is in the $(-1)^j$ eigenspace of the Pauli operator measured.</span></span>


## <a name="multiple-qubit-measurements"></a><span data-ttu-id="dbfb4-146">Кубит измерения</span><span class="sxs-lookup"><span data-stu-id="dbfb4-146">Multiple-qubit measurements</span></span>

<span data-ttu-id="dbfb4-147">Измерения кубит операторов Паули определены аналогично, как показано в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="dbfb4-147">Measurements of multi-qubit Pauli operators are defined similarly, as seen from:</span></span>

<span data-ttu-id="dbfb4-148">$ $ Z \otimes Z = \бегин{ bmatrix } 1 &0 &0&0 \\\\ 0 & -1&0&0 \\\\ 0&0 & -1&0 \\\\ 0&0&0&1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-148">$$ Z\otimes Z = \begin{bmatrix}1 &0 &0&0\\\\  0&-1&0&0\\\\ 0&0&-1&0\\\\ 0&0&0&1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="dbfb4-149">Таким же тензорныеные продукты двух операторов Паули-$Z $ образуют матрицу, состоящую из двух пробелов, состоящих из $ + 1 $ и $-1 $ еиженвалуес.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-149">Thus the tensor products of two Pauli-$Z$ operators forms a matrix composed of two spaces consisting of $+1$ and $-1$ eigenvalues.</span></span>
<span data-ttu-id="dbfb4-150">Как и в случае с одним кубит, оба составляют половину пространства, означающее, что половина доступного векторного пространства принадлежит к еиженспаце $ + 1 $ , а оставшаяся половина — к $-1 $ еиженспаце.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-150">As with the single-qubit case, both constitute a half-space meaning that half of the accessible vector space belongs to the $+1$ eigenspace and the remaining half to the $-1$ eigenspace.</span></span>
<span data-ttu-id="dbfb4-151">Как правило, можно легко узнать от определения продукта тензорные, что любое тензорные произведение операторов Паули-$Z $ и удостоверение также подчиняется этому.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-151">In general, it is easy to see from the definition of the tensor product that any tensor product of Pauli-$Z$ operators and the identity also obeys this.</span></span>
<span data-ttu-id="dbfb4-152">Например,</span><span class="sxs-lookup"><span data-stu-id="dbfb4-152">For example,</span></span>

<span data-ttu-id="dbfb4-153">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-153">$$ \begin{align}</span></span>
    <span data-ttu-id="dbfb4-154">Z \отимес \болдоне = \бегин{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-154">Z \otimes \boldone = \begin{bmatrix}</span></span>
        <span data-ttu-id="dbfb4-155">1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 &-1 & 0 \\ \\ 0 & 0 & 0 &-1 \енд{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-155">1 &  0 &  0 &  0 \\\\ 0 &  1 &  0 &  0 \\\\ 0 &  0 & -1 &  0 \\\\ 0 &  0 &  0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="dbfb4-156">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-156">\end{align}</span></span>
$$

<span data-ttu-id="dbfb4-157">Как и раньше, любое единое преобразование таких матриц также описывает две пробелы с меткой $ \пм 1 $ еиженвалуес.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-157">As before, any unitary transformation of such matrices also describes two half-spaces labeled by $\pm 1$ eigenvalues.</span></span>
<span data-ttu-id="dbfb4-158">Например, $X \otimes X = h h \otimes (z \otimes z) h \otimes h по $ идентификатору, $Z = хксх $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-158">For example, $X\otimes X = H\otimes H(Z\otimes Z)H\otimes H$  from the identity that $Z=HXH$.</span></span>
<span data-ttu-id="dbfb4-159">Как и в случае с одним кубит, все два кубит Паули-измерения могут быть написаны как $U ^ \дагжер (Z \otimes \ид) U $ для $4 \times 4 $ единых матриц $U $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-159">Similar to the one-qubit case, all two-qubit Pauli-measurements can be written as $U^\dagger (Z\otimes \id) U$ for $4\times 4$ unitary matrices $U$.</span></span> <span data-ttu-id="dbfb4-160">Перечислить преобразования в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-160">We enumerate the transformations in the following table.</span></span>

> [!NOTE]
> <span data-ttu-id="dbfb4-161">В таблице ниже мы используем $ \Операторнаме{СВАП } $ для обозначения матрицы $ $ \бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-161">In the table below, we use $\operatorname{SWAP}$ to indicate the matrix $$ \begin{align}</span></span>
>     <span data-ttu-id="dbfb4-162">\Операторнаме{СВАП } & = \лефт (\бегин{Матрикс}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-162">\operatorname{SWAP} & = \left(\begin{matrix}</span></span>
>         <span data-ttu-id="dbfb4-163">1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \енд{Матрикс } \ригхт) \енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-163">1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{matrix}\right) \end{align}</span></span>
> <span data-ttu-id="dbfb4-164">$ $ используется для имитации внутренней операции [`SWAP`](xref:microsoft.quantum.intrinsic) .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-164">$$ used to simulate the intrinsic operation [`SWAP`](xref:microsoft.quantum.intrinsic).</span></span>

|<span data-ttu-id="dbfb4-165">Измерение Паули</span><span class="sxs-lookup"><span data-stu-id="dbfb4-165">Pauli Measurement</span></span>     |<span data-ttu-id="dbfb4-166">Единое преобразование</span><span class="sxs-lookup"><span data-stu-id="dbfb4-166">Unitary transformation</span></span>  |
|----------------------|------------------------|
| <span data-ttu-id="dbfb4-167">$Z \отимес \болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-167">$Z \otimes \boldone$</span></span> | <span data-ttu-id="dbfb4-168">$ \болдоне \отимес \болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-168">$\boldone \otimes \boldone$</span></span> |
| <span data-ttu-id="dbfb4-169">$Z \otimes \болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-169">$Z\otimes \boldone$</span></span> | <span data-ttu-id="dbfb4-170">\болдоне $ \болдоне \otimes$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-170">$\boldone\otimes \boldone$</span></span> |
| <span data-ttu-id="dbfb4-171">$X \otimes \болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-171">$X\otimes \boldone$</span></span> | <span data-ttu-id="dbfb4-172">$H \otimes \болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-172">$H\otimes \boldone$</span></span> |
| <span data-ttu-id="dbfb4-173">$Y \otimes \болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-173">$Y\otimes \boldone$</span></span> | <span data-ttu-id="dbfb4-174">$HS ^ \дагжер \otimes \болдоне$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-174">$HS^\dagger\otimes \boldone$</span></span> |
| <span data-ttu-id="dbfb4-175">$ \болдоне \отимес Z$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-175">$\boldone \otimes Z$</span></span> | <span data-ttu-id="dbfb4-176">\Операторнаме{СВАП}$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-176">$\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="dbfb4-177">$ \болдоне \отимес X$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-177">$\boldone \otimes X$</span></span> | <span data-ttu-id="dbfb4-178">$ (H \otimes \болдоне) \операторнаме{СВАП}$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-178">$(H\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="dbfb4-179">$ \болдоне \отимес Y$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-179">$\boldone \otimes Y$</span></span> | <span data-ttu-id="dbfb4-180">$ (HS ^ \дагжер \otimes \болдоне) \операторнаме{СВАП}$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-180">$(HS^\dagger\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="dbfb4-181">$Z \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-181">$Z\otimes Z$</span></span> | <span data-ttu-id="dbfb4-182">$ \Операторнаме{кнот } \_ {10}$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-182">$\operatorname{CNOT}\_{10}$</span></span> |
| <span data-ttu-id="dbfb4-183">$X \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-183">$X\otimes Z$</span></span> | <span data-ttu-id="dbfb4-184">$ \Операторнаме{кнот } \_ {10 } (H \otimes \болдоне) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-184">$\operatorname{CNOT}\_{10}(H\otimes \boldone)$</span></span> |
| <span data-ttu-id="dbfb4-185">$Y \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-185">$Y\otimes Z$</span></span> | <span data-ttu-id="dbfb4-186">$ \Операторнаме{кнот } \_ {10 } (HS ^ \дагжер \otimes \болдоне) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-186">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes \boldone)$</span></span> |
| <span data-ttu-id="dbfb4-187">$Z \otimes X$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-187">$Z\otimes X$</span></span> | <span data-ttu-id="dbfb4-188">$ \Операторнаме{кнот } \_ {10 } (\болдоне \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-188">$\operatorname{CNOT}\_{10}(\boldone\otimes H)$</span></span> |
| <span data-ttu-id="dbfb4-189">$X \otimes X$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-189">$X\otimes X$</span></span> | <span data-ttu-id="dbfb4-190">$ \Операторнаме{кнот } \_ {10 } (h \otimes h) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-190">$\operatorname{CNOT}\_{10}(H\otimes H)$</span></span> |
| <span data-ttu-id="dbfb4-191">$Y \otimes X$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-191">$Y\otimes X$</span></span> | <span data-ttu-id="dbfb4-192">$ \Операторнаме{кнот } \_ {10 } (HS ^ \дагжер \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-192">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes H)$</span></span> |
| <span data-ttu-id="dbfb4-193">$Z \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-193">$Z\otimes Y$</span></span> | <span data-ttu-id="dbfb4-194">$ \Операторнаме{кнот } \_ {10 } (\болдоне \отимес HS ^ \дагжер) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-194">$\operatorname{CNOT}\_{10}(\boldone \otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="dbfb4-195">$X \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-195">$X\otimes Y$</span></span> | <span data-ttu-id="dbfb4-196">$ \Операторнаме{кнот } \_ {10 } (H \otimes HS ^ \дагжер) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-196">$\operatorname{CNOT}\_{10}(H\otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="dbfb4-197">$Y \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="dbfb4-197">$Y\otimes Y$</span></span> | <span data-ttu-id="dbfb4-198">$ \Операторнаме{кнот } \_ {10 } (HS ^ \дагжер \otimes HS ^ \дагжер) $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-198">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes HS^\dagger)$</span></span> |

<span data-ttu-id="dbfb4-199">Здесь [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) операция отображается по следующей причине.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-199">Here, the [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operation appears for the following reason.</span></span>
<span data-ttu-id="dbfb4-200">Каждое измерение Паули, которое не включает матрицу $ \болдоне, $ эквивалентно $Z \otimes Z $ по описанным выше причинам.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-200">Each Pauli measurement that does not include the $\boldone$ matrix is equivalent up to a unitary to $Z\otimes Z$ by the above reasoning.</span></span>
<span data-ttu-id="dbfb4-201">$Z еиженвалуес \otimes Z $ зависят только от четности Кубитс, составляющих каждый вектор вычислительных операций, а контролируемые операции не служат для вычисления этой контрольной суммы и ее сохранения в первый бит.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-201">The eigenvalues of $Z\otimes Z$ only depend on the parity of the qubits that comprise each computational basis vector, and the controlled-not operations serve to compute this parity and store it in the first bit.</span></span>
<span data-ttu-id="dbfb4-202">После того как первый бит будет измерен, мы можем восстановить удостоверение результирующей половины пространства, что эквивалентно измерению оператора Паули.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-202">Then once the first bit is measured, we can recover the identity of the resultant half-space, which is equivalent to measuring the Pauli operator.</span></span>

<span data-ttu-id="dbfb4-203">Еще одно Примечание. Хотя может показаться, что измерение $Z Z аналогично \otimes $ последовательному измерению $Z \otimes \mathbb{1 } $, а затем $ \mathbb{1 } \отимес Z $ , это предположение будет ложным.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-203">One additional note: while it may be tempting to assume that measuring $Z\otimes Z$ is the same as sequentially measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$, this assumption would be false.</span></span>
<span data-ttu-id="dbfb4-204">Причина в том, что измерение $Z \otimes Z $ проецирует состояние такта в $ + 1 $ или $-1 $ еиженстате этих операторов.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-204">The reason is that measuring $Z\otimes Z$ projects the quantum state into either the $+1$ or $-1$ eigenstate of these operators.</span></span>
<span data-ttu-id="dbfb4-205">Измерение $Z \otimes \mathbb{1 } $, а затем $ \Mathbb{1 } \отимес Z $ Проецирует вектор состояния такта сначала на половину $Z \otimes \mathbb{1 } $, а затем в половину пространства, равное $ \mathbb{1 } \отимес Z $ . При наличии четырех векторов вычисления, выполнение обоих измерений приводит к уменьшению состояния до четвертого пространства и, следовательно, сокращает его до одного вычислительного вектора.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-205">Measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$ projects the quantum state vector first onto a half space of $Z\otimes \mathbb{1}$ and then onto a half space of $\mathbb{1} \otimes Z$. As there are four computational basis vectors, performing both measurements reduces the state to a quarter-space and hence reduces it to a single computational basis vector.</span></span>

## <a name="correlations-between-qubits"></a><span data-ttu-id="dbfb4-206">Корреляции между Кубитс</span><span class="sxs-lookup"><span data-stu-id="dbfb4-206">Correlations between qubits</span></span>
<span data-ttu-id="dbfb4-207">Другим способом измерения тензорныеных продуктов Паули матриц, таких как $X \otimes X $ или $Z \otimes Z $ , является то, что эти измерения позволяют просматривать сведения, хранящиеся в корреляциях между двумя Кубитс.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-207">Another way of looking at measuring tensor products of Pauli matrices such as $X\otimes X$ or $Z\otimes Z$ is that these measurements let you look at information stored in the correlations between the two qubits.</span></span>
<span data-ttu-id="dbfb4-208">Измерение $X \otimes \ид $ позволяет просматривать информацию, которая хранится локально в первой кубит.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-208">Measuring $X\otimes \id$ lets you look at information that is locally stored in the first qubit.</span></span>
<span data-ttu-id="dbfb4-209">Несмотря на то что оба типа измерений в тактовых вычислениях одинаково важны, в бывшей степени используются возможности тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-209">While both types of measurements are equally valuable in quantum computing, the former illuminates the power of quantum computing.</span></span>
<span data-ttu-id="dbfb4-210">Он показывает, что в тактовых вычислениях часто сведения, которые вы хотите изучить, не хранятся ни в одном кубит, а в отдельном месте, а не в Кубитс, и, следовательно, только с помощью совместного измерения (например, $Z \otimes Z $ ) эти сведения становятся манифестом.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-210">It reveals that in quantum computing, often the information you wish to learn is not stored in any single qubit but rather stored non-locally in all the qubits at once, and therefore only by looking at it through a joint measurement (e.g. $Z\otimes Z$) does this information become manifest.</span></span>

<span data-ttu-id="dbfb4-211">Например, при исправлении ошибок мы часто хотели бы узнать, какая ошибка возникла при изучении состояния, которое мы пытаемся защитить.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-211">For example, in error correction, we often wish to learn what error occurred while learning nothing about the state that we're trying to protect.</span></span>
<span data-ttu-id="dbfb4-212">В примере [кода с зеркальным отражением](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) показан пример того, как это можно сделать с помощью таких измерений, как $Z \отимес Z \отимес \ид $ and $ \ид \Отимес z \отимес z $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-212">The [bit-flip code sample](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) shows an example of how you can do that using measurements like $Z \otimes Z \otimes \id$ and $\id \otimes Z \otimes Z$.</span></span>
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

<span data-ttu-id="dbfb4-213">Также можно измерять произвольные операторы Паули, такие как $X \otimes Y \Отимес Z \отимес \болдоне $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-213">Arbitrary Pauli operators such as $X\otimes Y \otimes Z \otimes \boldone$ can also be measured.</span></span>
<span data-ttu-id="dbfb4-214">Все такие тензорныеные продукты операторов Паули имеют только два еиженвалуес $ \пм 1 $ и оба еиженспацес составляют половины пространства всего вектора.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-214">All such tensor products of Pauli operators have only two eigenvalues $\pm 1$ and both eigenspaces constitute half-spaces of the entire vector space.</span></span>
<span data-ttu-id="dbfb4-215">Поэтому они совпадают с указанными выше требованиями.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-215">Thus they coincide with the requirements stated above.</span></span>

<span data-ttu-id="dbfb4-216">В Q # такие измерения возвращают $j, $ Если измерение возвращает результат в еиженспаце знака $ (-1) ^ j $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-216">In Q#, such measurements return $j$ if the measurement yields a result in the eigenspace of sign $(-1)^j$.</span></span>
<span data-ttu-id="dbfb4-217">Использование Паули измерений в качестве встроенной функции в Q # полезно, так как при измерении таких операторов требуется использовать длинные цепочки из контролируемого шлюза и преобразования базисов для описания диагонализинг $U $ шлюза, необходимого для выражения операции как тензорныеного произведения $Z $ и $ \ид $ . Благодаря возможности указать, что вы хотите выполнить одно из этих предварительно определенных измерений, не нужно беспокоиться о том, как преобразовать базу таким образом, чтобы измерение базисных данных предваряет необходимую информацию.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-217">Having Pauli measurements as a built-in feature in Q# is helpful because measuring such operators requires long chains of controlled-NOT gates and basis transformations to describe the diagonalizing $U$ gate needed to express the operation as a tensor product of $Z$ and $\id$. By being able to specify that you wish to do one of these pre-defined measurements, you don't need to worry about how to transform your basis such that a computational basis measurement provides the necessary information.</span></span>
<span data-ttu-id="dbfb4-218">Q # обрабатывает все необходимые преобразования автоматически.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-218">Q# handles all the necessary basis transformations for you automatically.</span></span>
<span data-ttu-id="dbfb4-219">Дополнительные сведения см. в разделе [`Measure`](xref:microsoft.quantum.intrinsic.measure) [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) операции и.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-219">For more information, see the [`Measure`](xref:microsoft.quantum.intrinsic.measure) and [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operations.</span></span>

## <a name="the-no-cloning-theorem"></a><span data-ttu-id="dbfb4-220">Теорема без клонирования</span><span class="sxs-lookup"><span data-stu-id="dbfb4-220">The No-Cloning Theorem</span></span>

<span data-ttu-id="dbfb4-221">Сведения о такте являются мощными.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-221">Quantum information is powerful.</span></span>
<span data-ttu-id="dbfb4-222">Это позволяет нам сделать незначительную работу, например, экспоненциальное количество факторов быстрее, чем лучшие известные классические алгоритмы, или эффективно моделировать коррелированные системы электронного представления, которые в классической степени потребовали экспоненциальной стоимости для корректной имитации.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-222">It enables us to do amazing things such as factor numbers exponentially faster than the best known classical algorithms, or efficiently simulate correlated electron systems that classically require exponential cost to simulate accurately.</span></span>
<span data-ttu-id="dbfb4-223">Однако существуют ограничения на возможности тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-223">However, there are limitations to the power of quantum computing.</span></span>
<span data-ttu-id="dbfb4-224">Одно такое ограничение предоставляется *без клонирования Теорема*.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-224">One such limitation is given by the *No-Cloning Theorem*.</span></span>

<span data-ttu-id="dbfb4-225">Теорема без клонирования — это выразился с именем.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-225">The No-Cloning Theorem is aptly named.</span></span>
<span data-ttu-id="dbfb4-226">Он запрещает клонирование универсальных состояний тактов на тактовый компьютер.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-226">It disallows cloning of generic quantum states by a quantum computer.</span></span>
<span data-ttu-id="dbfb4-227">Проверка теоремаа очень проста.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-227">The proof of the theorem is remarkably straightforward.</span></span>
<span data-ttu-id="dbfb4-228">Хотя полное подтверждение теоремаа без клонирования является слишком техническим для нашего обсуждения, в случае отсутствия дополнительного вспомогательного Кубитс в нашей области (вспомогательные кубитсы Кубитс используются для временных пространств во время вычислений и легко используются и управляются в Q #, см. раздел [позаимствование Кубитс](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span><span class="sxs-lookup"><span data-stu-id="dbfb4-228">While a full proof of the no-cloning theorem is a little too technical for our discussion here, the proof in the case of no additional auxiliary qubits is within our scope (auxiliary qubits are qubits used for scratch space during a computation and are easily used and managed in Q#, see [borrowed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span></span>

<span data-ttu-id="dbfb4-229">Для такого тактового компьютера операция клонирования должна быть описана единой матрицей.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-229">For such a quantum computer, the cloning operation must be described by a unitary matrix.</span></span>
<span data-ttu-id="dbfb4-230">Мы запрещаем измерение, так как это привело бы к повреждению состояния такта, которое мы пытаемся клонировать.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-230">We disallow measurement, since it would corrupt the quantum state we are trying to clone.</span></span>
<span data-ttu-id="dbfb4-231">Для имитации операции клонирования требуется, чтобы в единой матрице использовалось свойство, которое $ $ U \кет { \пси } \ket{0 } = \кет { \пси } \кет { \пси}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-231">To simulate the cloning operation, we want the unitary matrix used to have the property that $$ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}</span></span>
<span data-ttu-id="dbfb4-232">$ $ для любого состояния $ \кет { \пси } $.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-232">$$ for any state $\ket{\psi}$.</span></span>
<span data-ttu-id="dbfb4-233">Затем свойство линейного умножения матрицы подразумевает, что для любого второго состояния такта $ \кет { \фи } $</span><span class="sxs-lookup"><span data-stu-id="dbfb4-233">The linearity property of matrix multiplication then implies that for any second quantum state $\ket{\phi}$,</span></span>

<span data-ttu-id="dbfb4-234">\бегин{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-234">$$ \begin{align}</span></span>
    <span data-ttu-id="dbfb4-235">U \лефт [\frac{1 } {\sqrt{2 } } \лефт (\кет { \фи } + \кет { \пси } \ригхт) \ригхт] \ket{0}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-235">U \left[ \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right] \ket{0}</span></span>
    <span data-ttu-id="dbfb4-236">& = \frac{1 } {\sqrt{2 } } U \ket { \фи } \ket{0}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-236">& = \frac{1}{\sqrt{2}} U\ket{\phi}\ket{0}</span></span>
      <span data-ttu-id="dbfb4-237">+ \frac{1 } {\sqrt{2 } } U \ket { \пси } \ket{0 } \\ \\ & = \frac{1 } {\sqrt{2 } } \лефт (\кет { \фи } \кет { \фи } + \кет { \пси } \кет { \пси}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-237">+ \frac{1}{\sqrt{2}} U\ket{\psi}\ket{0} \\\\ & = \frac{1}{\sqrt{2}} \left( \ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi}</span></span>
        <span data-ttu-id="dbfb4-238">\ригхт) \\ \\ & \не \лефт (\frac{1 } {\sqrt{2 } } \лефт (\кет { \фи } + \кет { \пси } \ригхт) \ригхт) \отимес \лефт (\frac{1 } {\sqrt{2 } } \лефт (\кет { \фи } + \кет { \psi } \right) \right).</span><span class="sxs-lookup"><span data-stu-id="dbfb4-238">\right) \\\\ & \ne \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right) \otimes \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right).</span></span>
<span data-ttu-id="dbfb4-239">\енд{алигн}</span><span class="sxs-lookup"><span data-stu-id="dbfb4-239">\end{align}</span></span>
$$

<span data-ttu-id="dbfb4-240">Это обеспечивает фундаментальный интуиция за пределами Теорема без клонирования: любое устройство, которое копирует неизвестное состояние такта, должно вызвать ошибки по крайней мере в некоторых из скопированных состояний.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-240">This provides the fundamental intuition behind the No-Cloning Theorem: any device that copies an unknown quantum state must induce errors on at least some of the states it copies.</span></span>
<span data-ttu-id="dbfb4-241">Хотя в качестве ключевого предположения, что клонирование работает линейно во входном состоянии, может быть нарушено благодаря добавлению и измерению вспомогательных Кубитс, такое взаимодействие также приводит к утечке информации о системе через статистику измерений и предотвращает точную клонирование в таких случаях.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-241">While the key assumption that the cloner acts linearly on the input state can be violated through the addition and measurement of auxiliary qubits, such interactions also leak information about the system through the measurement statistics and prevent exact cloning in such cases as well.</span></span>
<span data-ttu-id="dbfb4-242">Более полное подтверждение Теорема без клонирования см. в разделе Дополнительные [сведения](xref:microsoft.quantum.more-information).</span><span class="sxs-lookup"><span data-stu-id="dbfb4-242">For a more complete proof of the No-Cloning Theorem see [For more information](xref:microsoft.quantum.more-information).</span></span>

<span data-ttu-id="dbfb4-243">Теорема без клонирования важна для качественного понимания тактовых вычислений, так как если вы могли клонировать состояния такта недорого, вам будет предоставлена возможность почти Magical получать сведения о состояниях тактов.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-243">The No-Cloning Theorem is important for qualitative understanding of quantum computing because if you could clone quantum states inexpensively then you would be granted a near-magical ability to learn from quantum states.</span></span>
<span data-ttu-id="dbfb4-244">Действительно, можно нарушать принцип неопределенности ваунтед Гейзенбега.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-244">Indeed, you could violate Heisenberg's vaunted uncertainty principle.</span></span>
<span data-ttu-id="dbfb4-245">Кроме того, можно использовать оптимальный клон для получения одного примера из сложного распределения тактов и изучить все, что вы можете узнать об этом распространении, только из одного примера.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-245">Alternatively, you could use an optimal cloner to take a single sample from a complex quantum distribution and learn everything you could possibly learn about that distribution from just one sample.</span></span>
<span data-ttu-id="dbfb4-246">Это будет похоже на то, что вы передаете монет и просматривая головки, а затем сообщаете друзьям о результате, что они отвечают: "AH. распределение этого монет должно быть Бернулли с $p = 0.512643 \ лдотс $ !"</span><span class="sxs-lookup"><span data-stu-id="dbfb4-246">This would be like you flipping a coin and observing heads and then upon telling a friend about the result having them respond "Ah the distribution of that coin must be Bernoulli with $p=0.512643\ldots$!"</span></span>  <span data-ttu-id="dbfb4-247">Такой оператор будет не сенсикал, так как один бит информации (результат Head) просто не может предоставить множество данных, необходимых для кодирования распределения, без существенной информации.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-247">Such a statement would be non-sensical because one bit of information (the heads outcome) simply cannot provide the many bits of information needed to encode the distribution without substantial prior information.</span></span>
<span data-ttu-id="dbfb4-248">Аналогично, без предварительной информации мы не можем точно клонировать состояние такта, так как мы не можем подготовить ансамблей таких монет, не зная $p $ .</span><span class="sxs-lookup"><span data-stu-id="dbfb4-248">Similarly, without prior information we cannot perfectly clone a quantum state just as we cannot prepare an ensemble of such coins without knowing $p$.</span></span>

<span data-ttu-id="dbfb4-249">В тактовых вычислениях информация не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-249">Information is not free in quantum computing.</span></span>
<span data-ttu-id="dbfb4-250">Каждый измеренный кубит предоставляет один небольшой объем информации, и теорема без клонирования показывает, что нет программы трояны, которые можно использовать для обхода фундаментального компромисса между информацией, полученной от системы, и вызываемой беспорядки.</span><span class="sxs-lookup"><span data-stu-id="dbfb4-250">Each qubit measured gives a single bit of information, and the No-Cloning Theorem shows that there is no backdoor that can be exploited to get around the fundamental tradeoff between information gained about the system and the disturbance invoked upon it.</span></span>
