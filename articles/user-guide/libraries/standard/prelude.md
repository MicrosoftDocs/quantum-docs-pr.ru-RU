---
title: Встроенные операции и функции в КДК
description: Сведения о внутренних операциях и функциях в КДК, включая классические функции и единые операции поворота и измерения.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.prelude
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 4d15226fe46be79b7d3e6f414f33f1debd691f40
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692120"
---
# <a name="the-prelude"></a><span data-ttu-id="dea76-103">Версионного</span><span class="sxs-lookup"><span data-stu-id="dea76-103">The Prelude</span></span> #

<span data-ttu-id="dea76-104">Q#Компилятор и целевые компьютеры, входящие в состав пакета средств разработки тактовой передачи, предоставляют набор встроенных функций и операций, которые можно использовать при написании тактовых программ в Q# .</span><span class="sxs-lookup"><span data-stu-id="dea76-104">The Q# compiler and the target machines included with the Quantum Development Kit provide a set of intrinsic functions and operations that can be used when writing quantum programs in Q#.</span></span>

## <a name="intrinsic-operations-and-functions"></a><span data-ttu-id="dea76-105">Встроенные операции и функции</span><span class="sxs-lookup"><span data-stu-id="dea76-105">Intrinsic Operations and Functions</span></span> ##

<span data-ttu-id="dea76-106">Внутренние операции, определенные в стандартной библиотеке, относятся к одной из нескольких категорий:</span><span class="sxs-lookup"><span data-stu-id="dea76-106">The intrinsic operations defined in the standard library roughly fall into one of several categories:</span></span>

- <span data-ttu-id="dea76-107">Неотъемлемые классические функции, собранные в <xref:Microsoft.Quantum.Core> пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="dea76-107">Essential classical functions, collected in the <xref:Microsoft.Quantum.Core> namespace.</span></span>
- <span data-ttu-id="dea76-108">Операции, представляющие унитариес, состоящие из [Клиффорд и $T $ Gates](xref:microsoft.quantum.concepts.qubit).</span><span class="sxs-lookup"><span data-stu-id="dea76-108">Operations representing unitaries composed of [Clifford and $T$ gates](xref:microsoft.quantum.concepts.qubit).</span></span>
- <span data-ttu-id="dea76-109">Операции, представляющие повороты различных операторов.</span><span class="sxs-lookup"><span data-stu-id="dea76-109">Operations representing rotations about various operators.</span></span>
- <span data-ttu-id="dea76-110">Операции, реализующие измерения.</span><span class="sxs-lookup"><span data-stu-id="dea76-110">Operations implementing measurements.</span></span>

<span data-ttu-id="dea76-111">Так как набор шлюзов Клиффорд + $T $ является [универсальным](xref:microsoft.quantum.concepts.multiple-qubits) для тактовых вычислений, эти операции достаточно для реализации любого тактового алгоритма в неглигибли небольшой ошибке.</span><span class="sxs-lookup"><span data-stu-id="dea76-111">Since the Clifford + $T$ gate set is [universal](xref:microsoft.quantum.concepts.multiple-qubits) for quantum computing, these operations suffice to approximately implement any quantum algorithm within negligibly small error.</span></span>
<span data-ttu-id="dea76-112">Предоставляя также повороты, Q# позволяя программисту работать в рамках единой кубит единой и кнот ворота библиотеки.</span><span class="sxs-lookup"><span data-stu-id="dea76-112">By providing rotations as well, Q# allows the programmer to work within the single qubit unitary and CNOT gate library.</span></span> <span data-ttu-id="dea76-113">Эту библиотеку гораздо проще подумать, так как она не требует от программиста непосредственного выражения Клиффорд + $T $, и так как существуют высокоэффективные методы для компиляции одного кубит унитариес в Клиффорд и $T $ Gates (Дополнительные сведения см. [здесь](xref:microsoft.quantum.more-information) ).</span><span class="sxs-lookup"><span data-stu-id="dea76-113">This library is much easier to think about because it does not  require the programmer to directly express the Clifford + $T$ decomposition and because highly efficient methods exist for compiling single qubit unitaries into Clifford and $T$ gates (see [here](xref:microsoft.quantum.more-information) for more information).</span></span>

<span data-ttu-id="dea76-114">Там, где это возможно, операции, определенные в версионного, которые работают с Кубитс, позволяют применить `Controlled` вариант, чтобы целевой компьютер выполнит соответствующую декомпозицию.</span><span class="sxs-lookup"><span data-stu-id="dea76-114">Where possible, the operations defined in the prelude which act on qubits allow for applying the `Controlled` variant, such that the target machine will perform the appropriate decomposition.</span></span>

<span data-ttu-id="dea76-115">Многие функции и операции, определенные в этой части версионного, находятся в @"microsoft.quantum.intrinsic" пространстве имен, так что большинство Q# исходных файлов будет иметь `open Microsoft.Quantum.Intrinsic;` директиву сразу после объявления первоначального пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dea76-115">Many of the functions and operations defined in this portion of the prelude are in the @"microsoft.quantum.intrinsic" namespace, such that most Q# source files will have an `open Microsoft.Quantum.Intrinsic;` directive immediately following the initial namespace declaration.</span></span>
<span data-ttu-id="dea76-116"><xref:Microsoft.Quantum.Core>Пространство имен автоматически открывается, поэтому такие функции, как, <xref:Microsoft.Quantum.Core.Length> можно использовать без `open` инструкции.</span><span class="sxs-lookup"><span data-stu-id="dea76-116">The <xref:Microsoft.Quantum.Core> namespace is automatically opened, so that functions such as <xref:Microsoft.Quantum.Core.Length> can be used without an `open` statement at all.</span></span>

### <a name="common-single-qubit-unitary-operations"></a><span data-ttu-id="dea76-117">Общие Single-Qubit единых операций</span><span class="sxs-lookup"><span data-stu-id="dea76-117">Common Single-Qubit Unitary Operations</span></span> ###

<span data-ttu-id="dea76-118">Версионного также определяет многие распространенные [операции с одной кубит](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).</span><span class="sxs-lookup"><span data-stu-id="dea76-118">The prelude also defines many common [single-qubit operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).</span></span>
<span data-ttu-id="dea76-119">Все эти операции допускают `Controlled` и `Adjoint` операторов.</span><span class="sxs-lookup"><span data-stu-id="dea76-119">All of these operations allow both the `Controlled` and `Adjoint` functors.</span></span>

#### <a name="pauli-operators"></a><span data-ttu-id="dea76-120">Операторы Паули</span><span class="sxs-lookup"><span data-stu-id="dea76-120">Pauli Operators</span></span> ####

<span data-ttu-id="dea76-121"><xref:Microsoft.Quantum.Intrinsic.X>Операция реализует оператор паули $X $.</span><span class="sxs-lookup"><span data-stu-id="dea76-121">The <xref:Microsoft.Quantum.Intrinsic.X> operation implements the Pauli $X$ operator.</span></span>
<span data-ttu-id="dea76-122">Это иногда также называется `NOT` шлюзом.</span><span class="sxs-lookup"><span data-stu-id="dea76-122">This is sometimes also known as the `NOT` gate.</span></span>
<span data-ttu-id="dea76-123">Он имеет подпись `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-123">It has signature `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-124">Он соответствует единому кубит едину:</span><span class="sxs-lookup"><span data-stu-id="dea76-124">It corresponds to the single-qubit unitary:</span></span>

<span data-ttu-id="dea76-125">\бегин{екуатион} \бегин{бматрикс} 0 & 1 \\ \\ % FIXME: это в настоящее время использует куадвхакк.</span><span class="sxs-lookup"><span data-stu-id="dea76-125">\begin{equation} \begin{bmatrix} 0 & 1 \\\\ % FIXME: this currently uses the quadwhack hack.</span></span>
<span data-ttu-id="dea76-126">1 & 0 \енд{бматрикс} \енд{екуатион}</span><span class="sxs-lookup"><span data-stu-id="dea76-126">1 & 0 \end{bmatrix} \end{equation}</span></span>

<span data-ttu-id="dea76-127"><xref:Microsoft.Quantum.Intrinsic.Y>Операция реализует оператор паули $Y $.</span><span class="sxs-lookup"><span data-stu-id="dea76-127">The <xref:Microsoft.Quantum.Intrinsic.Y> operation implements the Pauli $Y$ operator.</span></span>
<span data-ttu-id="dea76-128">Он имеет подпись `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-128">It has signature `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-129">Он соответствует единому кубит едину:</span><span class="sxs-lookup"><span data-stu-id="dea76-129">It corresponds to the single-qubit unitary:</span></span>

<span data-ttu-id="dea76-130">\бегин{екуатион} \бегин{бматрикс} 0 &-i \\ \\ % FIXME: в настоящее время используется куадвхакк хакер.</span><span class="sxs-lookup"><span data-stu-id="dea76-130">\begin{equation} \begin{bmatrix} 0 & -i \\\\ % FIXME: this currently uses the quadwhack hack.</span></span>
<span data-ttu-id="dea76-131">я & 0 \енд{бматрикс} \енд{екуатион}</span><span class="sxs-lookup"><span data-stu-id="dea76-131">i & 0 \end{bmatrix} \end{equation}</span></span>

<span data-ttu-id="dea76-132"><xref:Microsoft.Quantum.Intrinsic.Z>Операция реализует оператор паули $Z $.</span><span class="sxs-lookup"><span data-stu-id="dea76-132">The <xref:Microsoft.Quantum.Intrinsic.Z> operation implements the Pauli $Z$ operator.</span></span>
<span data-ttu-id="dea76-133">Он имеет подпись `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-133">It has signature `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-134">Он соответствует единому кубит едину:</span><span class="sxs-lookup"><span data-stu-id="dea76-134">It corresponds to the single-qubit unitary:</span></span>

<span data-ttu-id="dea76-135">\бегин{екуатион} \бегин{бматрикс} 1 & 0 \\ \\ % FIXME: это в настоящее время использует куадвхакк.</span><span class="sxs-lookup"><span data-stu-id="dea76-135">\begin{equation} \begin{bmatrix} 1 & 0 \\\\ % FIXME: this currently uses the quadwhack hack.</span></span>
<span data-ttu-id="dea76-136">0 &-1 \енд{бматрикс} \енд{екуатион}</span><span class="sxs-lookup"><span data-stu-id="dea76-136">0 & -1 \end{bmatrix} \end{equation}</span></span>

<span data-ttu-id="dea76-137">Ниже показаны преобразования, сопоставленные с [блочной сферой](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) (ось вращения в каждом случае выделяется красным цветом):</span><span class="sxs-lookup"><span data-stu-id="dea76-137">Below we see these transformations mapped to the [Bloch sphere](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) (the rotation axis in each case is highlighted red):</span></span>

![Операции Паули, сопоставленные с сферой БЛОЧ](~/media/prelude_pauliBloch.png)

<span data-ttu-id="dea76-139">Важно отметить, что применение одного и того же шлюза Паули дважды к тому же кубит отменяет операцию (так как теперь вы выполнили полный поворот 2π (360 °) над поверхностью БЛОЧ Sphere, что приводит к последующей отправной точке).</span><span class="sxs-lookup"><span data-stu-id="dea76-139">It is important to note that applying the same Pauli gate twice to the same qubit cancels out the operation (because you have now performed a full rotation of 2π (360°) over the surface to the Bloch Sphere, thus arriving back at the starting point).</span></span> <span data-ttu-id="dea76-140">Это приводит нас к следующему удостоверению:</span><span class="sxs-lookup"><span data-stu-id="dea76-140">This brings us to the following identity:</span></span>

<span data-ttu-id="dea76-141">$ $ X ^ 2 = Y ^ 2 = Z ^ 2 = \болдоне $ $</span><span class="sxs-lookup"><span data-stu-id="dea76-141">$$ X^2=Y^2=Z^2=\boldone $$</span></span>

<span data-ttu-id="dea76-142">Это можно визуально использовать в сфере БЛОЧ:</span><span class="sxs-lookup"><span data-stu-id="dea76-142">This can be visualised on the Bloch sphere:</span></span>

![XX = I](~/media/prelude_blochIdentity.png)

#### <a name="other-single-qubit-cliffords"></a><span data-ttu-id="dea76-144">Другие Single-Qubit Клиффордс</span><span class="sxs-lookup"><span data-stu-id="dea76-144">Other Single-Qubit Cliffords</span></span> ####

<span data-ttu-id="dea76-145"><xref:Microsoft.Quantum.Intrinsic.H>Операция реализует шлюз хадамард.</span><span class="sxs-lookup"><span data-stu-id="dea76-145">The <xref:Microsoft.Quantum.Intrinsic.H> operation implements the Hadamard gate.</span></span>
<span data-ttu-id="dea76-146">Это повлияет на оси Паули $X $ и $Z $ целевого кубит, например $H \кет {0} = \кет{+} \масрел{: =} (\кет {0} + \кет {1} )/\скрт {2} $ and $H \кет{+} = \кет {0} $.</span><span class="sxs-lookup"><span data-stu-id="dea76-146">This interchanges the Pauli $X$ and $Z$ axes of the target qubit, such that $H\ket{0} = \ket{+} \mathrel{:=} (\ket{0} + \ket{1}) / \sqrt{2}$ and $H\ket{+} = \ket{0}$.</span></span>
<span data-ttu-id="dea76-147">Он имеет сигнатуру `(Qubit => Unit is Adj + Ctl)` и соответствует кубит единому:</span><span class="sxs-lookup"><span data-stu-id="dea76-147">It has signature `(Qubit => Unit is Adj + Ctl)`, and corresponds to the single-qubit unitary:</span></span>

<span data-ttu-id="dea76-148">\бегин{екуатион} \фрак {1} {\скрт {2} } \бегин{бматрикс} 1 & 1 \\ \\ % FIXME: в настоящее время используется куадвхакк Hack.</span><span class="sxs-lookup"><span data-stu-id="dea76-148">\begin{equation} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ % FIXME: this currently uses the quadwhack hack.</span></span>
<span data-ttu-id="dea76-149">1 &-1 \енд{бматрикс} \енд{екуатион}</span><span class="sxs-lookup"><span data-stu-id="dea76-149">1 & -1 \end{bmatrix} \end{equation}</span></span>

<span data-ttu-id="dea76-150">Шлюз Хадамард особенно важен, так как он может использоваться для создания части Штатов $ \кет {0} $ и $ \кет {1} $.</span><span class="sxs-lookup"><span data-stu-id="dea76-150">The Hadamard gate is particularly important as it can be used to create a superposition of the $\ket{0}$ and $\ket{1}$ states.</span></span> <span data-ttu-id="dea76-151">В представлении БЛОЧ Sphere проще всего подумать об этом как повороте $ \кет{\пси} $ вокруг оси x на $ \пи $ радианы ($ 180 ^ \Цирк $), за которым следует вращение (по часовой стрелке) вокруг оси y на $ \ PI/2 $ радианы ($ 90 ^ \Цирк $):</span><span class="sxs-lookup"><span data-stu-id="dea76-151">In the Bloch sphere representation, it is easiest to think of this as a rotation of $\ket{\psi}$ around the x-axis by $\pi$ radians ($180^\circ$) followed by a (clockwise) rotation around the y-axis by $\pi/2$ radians ($90^\circ$):</span></span>

![Операция хадамард, сопоставленная с сферой БЛОЧ](~/media/prelude_hadamardBloch.png)

<span data-ttu-id="dea76-153"><xref:Microsoft.Quantum.Intrinsic.S>Операция реализует шлюз фазы $S $.</span><span class="sxs-lookup"><span data-stu-id="dea76-153">The <xref:Microsoft.Quantum.Intrinsic.S> operation implements the phase gate $S$.</span></span>
<span data-ttu-id="dea76-154">Это квадратный корень матрицы операции Паули $Z $.</span><span class="sxs-lookup"><span data-stu-id="dea76-154">This is the matrix square root of the Pauli $Z$ operation.</span></span>
<span data-ttu-id="dea76-155">То есть $S ^ 2 = Z $.</span><span class="sxs-lookup"><span data-stu-id="dea76-155">That is, $S^2 = Z$.</span></span>
<span data-ttu-id="dea76-156">Он имеет сигнатуру `(Qubit => Unit is Adj + Ctl)` и соответствует кубит единому:</span><span class="sxs-lookup"><span data-stu-id="dea76-156">It has signature `(Qubit => Unit is Adj + Ctl)`, and corresponds to the single-qubit unitary:</span></span>

<span data-ttu-id="dea76-157">\бегин{екуатион} \бегин{бматрикс} 1 & 0 \\ \\ % FIXME: это в настоящее время использует куадвхакк.</span><span class="sxs-lookup"><span data-stu-id="dea76-157">\begin{equation} \begin{bmatrix} 1 & 0 \\\\ % FIXME: this currently uses the quadwhack hack.</span></span>
<span data-ttu-id="dea76-158">0 & я \енд{бматрикс} \енд{екуатион}</span><span class="sxs-lookup"><span data-stu-id="dea76-158">0 & i \end{bmatrix} \end{equation}</span></span>

#### <a name="rotations"></a><span data-ttu-id="dea76-159">Ротации</span><span class="sxs-lookup"><span data-stu-id="dea76-159">Rotations</span></span> ####

<span data-ttu-id="dea76-160">В дополнение к операциям Паули и Клиффорд выше, Q# версионного предоставляет разнообразные способы выражения поворотов.</span><span class="sxs-lookup"><span data-stu-id="dea76-160">In addition to the Pauli and Clifford operations above, the Q# prelude provides a variety of ways of expressing rotations.</span></span>
<span data-ttu-id="dea76-161">Как описано в разделе [операции с одним кубит](xref:microsoft.quantum.concepts.qubit#single-qubit-operations), возможность смены критически важна для алгоритмов такта.</span><span class="sxs-lookup"><span data-stu-id="dea76-161">As described in [single-qubit operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations), the ability to rotate is critical to quantum algorithms.</span></span>

<span data-ttu-id="dea76-162">Мы начнем с отзыва, что мы можем выразить любую операцию с одним кубит, используя $H $ и $T $ Gates, где $H $ является операцией Хадамард и где \бегин{екуатион} T \масрел{: =} \бегин{бматрикс} 1 & 0 \\ \\ % FIXME: в настоящее время используется четырехъядерный отправляю.</span><span class="sxs-lookup"><span data-stu-id="dea76-162">We start by recalling that we can express any single-qubit operation using the $H$ and $T$ gates, where $H$ is the Hadamard operation, and where \begin{equation} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ % FIXME: this currently uses the quad back whack hack.</span></span>
<span data-ttu-id="dea76-163">0 & e ^ {i \пи/4} \енд{бматрикс} \енд{екуатион} это квадратный корень <xref:Microsoft.Quantum.Intrinsic.S> операции, то есть $T ^ 2 = S $.</span><span class="sxs-lookup"><span data-stu-id="dea76-163">0 & e^{i \pi / 4} \end{bmatrix} \end{equation} This is the square root of the <xref:Microsoft.Quantum.Intrinsic.S> operation, such that $T^2 = S$.</span></span>
<span data-ttu-id="dea76-164">$T $ Gate в свою очередь реализуется <xref:Microsoft.Quantum.Intrinsic.T> операцией и имеет сигнатуру `(Qubit => Unit is Adj + Ctl)` , указывающую, что она является единой операцией с одним кубит.</span><span class="sxs-lookup"><span data-stu-id="dea76-164">The $T$ gate is in turn implemented by the <xref:Microsoft.Quantum.Intrinsic.T> operation, and has signature `(Qubit => Unit is Adj + Ctl)`, indicating that it is a unitary operation on a single-qubit.</span></span>

<span data-ttu-id="dea76-165">Несмотря на то, что этот принцип достаточно для описания любой произвольной операции с одним кубит, различные целевые компьютеры могут иметь более эффективные представления для ротации операторов Паули, таким образом, версионного включает различные способы конвиенентли Express.</span><span class="sxs-lookup"><span data-stu-id="dea76-165">Even though this is in principle sufficient to describe any arbitrary single-qubit operation, different target machines may have more efficient representations for rotations about Pauli operators, such that the prelude includes a variety of ways to convienently express such rotations.</span></span>
<span data-ttu-id="dea76-166">Самый простой из них — это <xref:Microsoft.Quantum.Intrinsic.r> операция, которая реализует поворот вокруг заданной оси Паули, \Бегин{екуатион} R (\сигма, \фи) \масрел{: =} \експ (-i \фи \сигма/2), \енд{екуатион}, где $ \сигма $ является оператором Паули, $ \Phi $ является углом и где $ \exp $ представляет экспоненциальную экспоненту.</span><span class="sxs-lookup"><span data-stu-id="dea76-166">The most basic of these is the <xref:Microsoft.Quantum.Intrinsic.r> operation, which implements a rotation around a specified Pauli axis, \begin{equation} R(\sigma, \phi) \mathrel{:=} \exp(-i \phi \sigma / 2), \end{equation} where $\sigma$ is a Pauli operator, $\phi$ is an angle, and where $\exp$ represents the matrix exponential.</span></span>
<span data-ttu-id="dea76-167">Он имеет сигнатуру `((Pauli, Double, Qubit) => Unit is Adj + Ctl)` , где первые две части входных данных представляют классические аргументы $ \сигма $ и $ \фи $, необходимые для указания одного оператора $R (\сигма, \фи) $.</span><span class="sxs-lookup"><span data-stu-id="dea76-167">It has signature `((Pauli, Double, Qubit) => Unit is Adj + Ctl)`, where the first two parts of the input represent the classical arguments $\sigma$ and $\phi$ needed to specify the unitary operator $R(\sigma, \phi)$.</span></span>
<span data-ttu-id="dea76-168">Можно частично применить $ \сигма $ и $ \фи $, чтобы получить операцию, тип которой является производным от одного кубит.</span><span class="sxs-lookup"><span data-stu-id="dea76-168">We can partially apply $\sigma$ and $\phi$ to obtain an operation whose type is that of a single-qubit unitary.</span></span>
<span data-ttu-id="dea76-169">Например, `R(PauliZ, PI() / 4, _)` имеет тип `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-169">For example, `R(PauliZ, PI() / 4, _)` has type `(Qubit => Unit is Adj + Ctl)`.</span></span>

> [!NOTE]
> <span data-ttu-id="dea76-170"><xref:Microsoft.Quantum.Intrinsic.r>Операция делит входной угол на 2 и умножает его на-1.</span><span class="sxs-lookup"><span data-stu-id="dea76-170">The <xref:Microsoft.Quantum.Intrinsic.r> operation divides the input angle by 2 and multiplies it by -1.</span></span>
> <span data-ttu-id="dea76-171">Для ротаций $Z $ это означает, что параметр $ \кет {0} $ еиженстате поворачивается на $-\фи/$2, а $ \кет {1} $ еиженстате поворачивается на $ \фи/$2, поэтому параметр $ \кет {1} $ еиженстате поворачивается на $ \фи $ по отношению к $ \кет $ {0} еиженстате.</span><span class="sxs-lookup"><span data-stu-id="dea76-171">For $Z$ rotations, this means that the $\ket{0}$ eigenstate is rotated by $-\phi / 2$ and the $\ket{1}$ eigenstate is rotated by $\phi / 2$, so that the $\ket{1}$ eigenstate is rotated by $\phi$ relative to the $\ket{0}$ eigenstate.</span></span>
>
> <span data-ttu-id="dea76-172">В частности, это означает, что `T` и отличается только неактуальным `R(PauliZ, PI() / 8, _)` [глобальным этапом](xref:microsoft.quantum.glossary#global-phase).</span><span class="sxs-lookup"><span data-stu-id="dea76-172">In particular, this means that `T` and `R(PauliZ, PI() / 8, _)` differ only by an irrelevant [global phase](xref:microsoft.quantum.glossary#global-phase).</span></span>
> <span data-ttu-id="dea76-173">По этой причине $T $ иногда называют $ \фрак{\пи} {8} $-Gate.</span><span class="sxs-lookup"><span data-stu-id="dea76-173">For this reason, $T$ is sometimes known as the $\frac{\pi}{8}$-gate.</span></span>
>
> <span data-ttu-id="dea76-174">Обратите внимание также на то, что поворот вокруг `PauliI` просто применяет глобальную фазу $ \фи/$2.</span><span class="sxs-lookup"><span data-stu-id="dea76-174">Note also that rotating around `PauliI` simply applies a global phase of $\phi / 2$.</span></span> <span data-ttu-id="dea76-175">Хотя такие этапы несущественны, как в [концептуальных документах](xref:microsoft.quantum.concepts.qubit), они важны для контролируемых `PauliI` поворотов.</span><span class="sxs-lookup"><span data-stu-id="dea76-175">While such phases are irrelevant, as argued in [the conceptual documents](xref:microsoft.quantum.concepts.qubit), they are relevant for controlled `PauliI` rotations.</span></span>

<span data-ttu-id="dea76-176">В алгоритмах такта часто бывает полезно выражать повороты как ДЯДИК дроби, например $ \фи = \пи k/2 ^ n $ для некоторых $k \ин \Масбб{з} $ и $n \ин \Масбб{н} $.</span><span class="sxs-lookup"><span data-stu-id="dea76-176">Within quantum algorithms, it is often useful to express rotations as dyadic fractions, such that $\phi = \pi k / 2^n$ for some $k \in \mathbb{Z}$ and $n \in \mathbb{N}$.</span></span>
<span data-ttu-id="dea76-177"><xref:Microsoft.Quantum.Intrinsic.RFrac>Операция реализует поворот вокруг указанной оси Паули, используя это соглашение.</span><span class="sxs-lookup"><span data-stu-id="dea76-177">The <xref:Microsoft.Quantum.Intrinsic.RFrac> operation implements a rotation around a specified Pauli axis using this convention.</span></span>
<span data-ttu-id="dea76-178">Он отличается от <xref:Microsoft.Quantum.Intrinsic.R> в том, что угол вращения задается как два входных значения типа `Int` , интерпретируемые как ДЯДИК дробь.</span><span class="sxs-lookup"><span data-stu-id="dea76-178">It differs from <xref:Microsoft.Quantum.Intrinsic.R> in that the rotation angle is specified as two inputs of type `Int`, interpreted as a dyadic fraction.</span></span>
<span data-ttu-id="dea76-179">Таким словами, `RFrac` имеет сигнатуру `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-179">Thus, `RFrac` has signature `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-180">Он реализует однокубитную единую $ \експ (i \пи k \сигма/2 ^ n) $, где $ \сигма $ — это матрица Паули, соответствующая первому аргументу, $k $ является вторым аргументом, а $n $ — третьим аргументом.</span><span class="sxs-lookup"><span data-stu-id="dea76-180">It implements the single-qubit unitary $\exp(i \pi k \sigma / 2^n)$, where $\sigma$ is the Pauli matrix corresponding to the first argument, $k$ is the second argument, and $n$ is the third argument.</span></span>
<span data-ttu-id="dea76-181">`RFrac(_,k,n,_)` то же самое, что `R(_,-πk/2^n,_)` ; Обратите внимание, что угол — это *отрицательная* часть дроби.</span><span class="sxs-lookup"><span data-stu-id="dea76-181">`RFrac(_,k,n,_)` is the same as `R(_,-πk/2^n,_)`; note that the angle is the *negative* of the fraction.</span></span>

<span data-ttu-id="dea76-182"><xref:Microsoft.Quantum.Intrinsic.Rx>Операция реализует поворот вокруг оси паули $X $.</span><span class="sxs-lookup"><span data-stu-id="dea76-182">The <xref:Microsoft.Quantum.Intrinsic.Rx> operation implements a rotation around the Pauli $X$ axis.</span></span>
<span data-ttu-id="dea76-183">Он имеет подпись `((Double, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-183">It has signature `((Double, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-184">Параметр `Rx(_, _)` совпадает с параметром `R(PauliX, _, _)`.</span><span class="sxs-lookup"><span data-stu-id="dea76-184">`Rx(_, _)` is the same as `R(PauliX, _, _)`.</span></span>

<span data-ttu-id="dea76-185"><xref:Microsoft.Quantum.Intrinsic.Ry>Операция реализует поворот вокруг оси паули $Y $.</span><span class="sxs-lookup"><span data-stu-id="dea76-185">The <xref:Microsoft.Quantum.Intrinsic.Ry> operation implements a rotation around the Pauli $Y$ axis.</span></span>
<span data-ttu-id="dea76-186">Он имеет подпись `((Double, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-186">It has signature `((Double, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-187">Параметр `Ry(_, _)` совпадает с параметром `R(PauliY,_ , _)`.</span><span class="sxs-lookup"><span data-stu-id="dea76-187">`Ry(_, _)` is the same as `R(PauliY,_ , _)`.</span></span>

<span data-ttu-id="dea76-188"><xref:Microsoft.Quantum.Intrinsic.Rz>Операция реализует поворот вокруг оси паули $Z $.</span><span class="sxs-lookup"><span data-stu-id="dea76-188">The <xref:Microsoft.Quantum.Intrinsic.Rz> operation implements a rotation around the Pauli $Z$ axis.</span></span>
<span data-ttu-id="dea76-189">Он имеет подпись `((Double, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-189">It has signature `((Double, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-190">Параметр `Rz(_, _)` совпадает с параметром `R(PauliZ, _, _)`.</span><span class="sxs-lookup"><span data-stu-id="dea76-190">`Rz(_, _)` is the same as `R(PauliZ, _, _)`.</span></span>

<span data-ttu-id="dea76-191"><xref:Microsoft.Quantum.Intrinsic.R1>Операция реализует поворот на заданную величину около $ \кет {1} $, еиженстате $-$1 из $Z $.</span><span class="sxs-lookup"><span data-stu-id="dea76-191">The <xref:Microsoft.Quantum.Intrinsic.R1> operation implements a rotation by the given amount around $\ket{1}$, the $-1$ eigenstate of $Z$.</span></span>
<span data-ttu-id="dea76-192">Он имеет подпись `((Double, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-192">It has signature `((Double, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-193">`R1(phi,_)` то же, что и, `R(PauliZ,phi,_)` за которым следует `R(PauliI,-phi,_)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-193">`R1(phi,_)` is the same as `R(PauliZ,phi,_)` followed by `R(PauliI,-phi,_)`.</span></span>

<span data-ttu-id="dea76-194"><xref:Microsoft.Quantum.Intrinsic.R1Frac>Операция реализует поворот на части по заданному объему вокруг Z = 1 еиженстате.</span><span class="sxs-lookup"><span data-stu-id="dea76-194">The <xref:Microsoft.Quantum.Intrinsic.R1Frac> operation implements a fractional rotation by the given amount around the Z=1 eigenstate.</span></span>
<span data-ttu-id="dea76-195">Он имеет подпись `((Int,Int, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-195">It has signature `((Int,Int, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-196">`R1Frac(k,n,_)` то же, что и, `RFrac(PauliZ,-k.n+1,_)` за которым следует `RFrac(PauliI,k,n+1,_)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-196">`R1Frac(k,n,_)` is the same as `RFrac(PauliZ,-k.n+1,_)` followed by `RFrac(PauliI,k,n+1,_)`.</span></span>

<span data-ttu-id="dea76-197">Пример операции вращения (вокруг оси Паули $Z $ в этом экземпляре), сопоставленной с блочной сферой, показан ниже:</span><span class="sxs-lookup"><span data-stu-id="dea76-197">An example of a rotation operation (around the Pauli $Z$ axis, in this instance) mapped onto the Bloch sphere is shown below:</span></span>

![Операция вращения, сопоставленная с блочной сферой](~/media/prelude_rotationBloch.png)

#### <a name="multi-qubit-operations"></a><span data-ttu-id="dea76-199">Операции с несколькими кубит</span><span class="sxs-lookup"><span data-stu-id="dea76-199">Multi-Qubit Operations</span></span> ####

<span data-ttu-id="dea76-200">В дополнение к кубит операциям выше, версионного также определяет несколько операций с несколькими кубит.</span><span class="sxs-lookup"><span data-stu-id="dea76-200">In addition to the single-qubit operations above, the prelude also defines several multi-qubit operations.</span></span>

<span data-ttu-id="dea76-201">Во-первых, <xref:Microsoft.Quantum.Intrinsic.CNOT> операция выполняет Стандартный контролируемый `NOT` шлюз, \бегин{екуатион} \операторнаме{кнот} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="dea76-201">First, the <xref:Microsoft.Quantum.Intrinsic.CNOT> operation performs a standard controlled-`NOT` gate, \begin{equation} \operatorname{CNOT} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}.</span></span>
<span data-ttu-id="dea76-202">\енд{екуатион} имеет сигнатуру `((Qubit, Qubit) => Unit is Adj + Ctl)` , представляющую, что $ \операторнаме{кнот} $ действует унитарили на двух отдельных Кубитс.</span><span class="sxs-lookup"><span data-stu-id="dea76-202">\end{equation} It has signature `((Qubit, Qubit) => Unit is Adj + Ctl)`, representing that $\operatorname{CNOT}$ acts unitarily on two individual qubits.</span></span>
<span data-ttu-id="dea76-203">Параметр `CNOT(q1, q2)` совпадает с параметром `(Controlled X)([q1], q2)`.</span><span class="sxs-lookup"><span data-stu-id="dea76-203">`CNOT(q1, q2)` is the same as `(Controlled X)([q1], q2)`.</span></span>
<span data-ttu-id="dea76-204">Так как `Controlled` функтор позволяет управлять регистром, мы используем литерал массива, `[q1]` чтобы указать, что нам нужен только один элемент управления.</span><span class="sxs-lookup"><span data-stu-id="dea76-204">Since the `Controlled` functor allows for controlling on a register, we use the array literal `[q1]` to indicate that we want only the one control.</span></span>

<span data-ttu-id="dea76-205">Эта <xref:Microsoft.Quantum.Intrinsic.CCNOT> Операция ВЫПОЛНЯЕТ не шлюз с удвоенной назначением, иногда также известный как шлюз Тоффоли.</span><span class="sxs-lookup"><span data-stu-id="dea76-205">The <xref:Microsoft.Quantum.Intrinsic.CCNOT> operation performs doubly-controlled NOT gate, sometimes also known as the Toffoli gate.</span></span>
<span data-ttu-id="dea76-206">Он имеет подпись `((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-206">It has signature `((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-207">Параметр `CCNOT(q1, q2, q3)` совпадает с параметром `(Controlled X)([q1, q2], q3)`.</span><span class="sxs-lookup"><span data-stu-id="dea76-207">`CCNOT(q1, q2, q3)` is the same as `(Controlled X)([q1, q2], q3)`.</span></span>

<span data-ttu-id="dea76-208"><xref:Microsoft.Quantum.Intrinsic.SWAP>Операция меняет местами такты двух Кубитс.</span><span class="sxs-lookup"><span data-stu-id="dea76-208">The <xref:Microsoft.Quantum.Intrinsic.SWAP> operation swaps the quantum states of two qubits.</span></span>
<span data-ttu-id="dea76-209">То есть реализуется единая матрица \бегин{екуатион} \Операторнаме{СВАП} \масрел{: =} \бегин{бматрикс} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \енд{бматрикс}.</span><span class="sxs-lookup"><span data-stu-id="dea76-209">That is, it implements the unitary matrix \begin{equation} \operatorname{SWAP} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}.</span></span>
<span data-ttu-id="dea76-210">\енд{екуатион} имеет подпись `((Qubit, Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-210">\end{equation} It has signature `((Qubit, Qubit) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="dea76-211">`SWAP(q1,q2)` эквивалентно следующему, `CNOT(q1, q2)` `CNOT(q2, q1)` а затем `CNOT(q1, q2)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-211">`SWAP(q1,q2)` is equivalent to `CNOT(q1, q2)` followed by `CNOT(q2, q1)` and then `CNOT(q1, q2)`.</span></span>

> [!NOTE]
> <span data-ttu-id="dea76-212">Шлюз подкачки *не* совпадает с изменением расположения элементов переменной с типом `Qubit[]` .</span><span class="sxs-lookup"><span data-stu-id="dea76-212">The SWAP gate is *not* the same as rearranging the elements of a variable with type `Qubit[]`.</span></span>
> <span data-ttu-id="dea76-213">Применение `SWAP(q1, q2)` приводит к изменению состояния Кубитс, на которое ссылается `q1` и, а `q2` `let swappedRegister = [q2, q1];` также влияет только на эти Кубитс.</span><span class="sxs-lookup"><span data-stu-id="dea76-213">Applying `SWAP(q1, q2)` causes a change to the state of the qubits referred to by `q1` and `q2`, while `let swappedRegister = [q2, q1];` only affects how we refer to those qubits.</span></span>
> <span data-ttu-id="dea76-214">Кроме того, `(Controlled SWAP)([q0], (q1, q2))` позволяет `SWAP` применять к состоянию третьего кубит, который не может быть представлен путем изменения расположения элементов.</span><span class="sxs-lookup"><span data-stu-id="dea76-214">Moreover, `(Controlled SWAP)([q0], (q1, q2))` allows for `SWAP` to be conditioned on the state of a third qubit, which we cannot represent by rearranging elements.</span></span>
> <span data-ttu-id="dea76-215">Шлюз с управляемым ПЕРЕКЛЮЧЕНИЕм, также известный как шлюз Фредкин, достаточно мощный для включения всех классических вычислений.</span><span class="sxs-lookup"><span data-stu-id="dea76-215">The controlled-SWAP gate, also known as the Fredkin gate, is powerful enough to include all classical computation.</span></span>

<span data-ttu-id="dea76-216">Наконец, версионного предоставляет две операции для представления экспоненциальных функций операторов множественного кубит Паули.</span><span class="sxs-lookup"><span data-stu-id="dea76-216">Finally, the prelude provides two operations for representing exponentials of multi-qubit Pauli operators.</span></span>
<span data-ttu-id="dea76-217"><xref:Microsoft.Quantum.Intrinsic.Exp>Операция выполняет поворот на основе тензорные произведения матриц Паули, как представлено в нескольких кубит единых \Бегин{екуатион} \операторнаме{ЕКСП} (\век{\сигма}, \фи) \масрел{: =} \експ\лефт (i \Phi \ sigma_0 \otimes \ sigma_1 \otimes \cdots \otimes \ sigma_n \right), \end{Equation}, где $ \vec{\sigma} = (\ sigma_0, \ sigma_1, \dots, \ sigma_n) $ — это последовательность одноqubitных операторов Pauli, где $ \Phi $ является углом.</span><span class="sxs-lookup"><span data-stu-id="dea76-217">The <xref:Microsoft.Quantum.Intrinsic.Exp> operation performs a rotation based on a tensor product of Pauli matrices, as represented by the multi-qubit unitary \begin{equation} \operatorname{Exp}(\vec{\sigma}, \phi) \mathrel{:=} \exp\left(i \phi \sigma_0 \otimes \sigma_1 \otimes \cdots \otimes \sigma_n \right), \end{equation} where $\vec{\sigma} = (\sigma_0, \sigma_1, \dots, \sigma_n)$ is a sequence of single-qubit Pauli operators, and where $\phi$ is an angle.</span></span>
<span data-ttu-id="dea76-218">`Exp`Поворот представляет $ \век{\сигма} $ как массив `Pauli` элементов, так что он имеет сигнатуру `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-218">The `Exp` rotation represents $\vec{\sigma}$ as an array of `Pauli` elements, such that it has signature `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="dea76-219"><xref:Microsoft.Quantum.Intrinsic.ExpFrac>Операция выполняет тот же поворот, используя нотацию дробной части ДЯДИК, о которой говорилось выше.</span><span class="sxs-lookup"><span data-stu-id="dea76-219">The <xref:Microsoft.Quantum.Intrinsic.ExpFrac> operation performs the same rotation, using the dyadic fraction notation discussed above.</span></span>
<span data-ttu-id="dea76-220">Он имеет подпись `((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-220">It has signature `((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)`.</span></span>

> [!WARNING]
> <span data-ttu-id="dea76-221">Экспоненциальные произведения тензорные операторов Паули не аналогичны тензорныеным продуктам экспоненциальных операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="dea76-221">Exponentials of the tensor product of Pauli operators are not the same as tensor products of the exponentials of Pauli operators.</span></span>
> <span data-ttu-id="dea76-222">То есть $e ^ {i (Z \отимес Z) \фи} \не e ^ {i Z \фи} \отимес e ^ {i Z \фи} $.</span><span class="sxs-lookup"><span data-stu-id="dea76-222">That is, $e^{i (Z \otimes Z) \phi} \ne e^{i Z \phi} \otimes e^{i Z \phi}$.</span></span>

### <a name="measurements"></a><span data-ttu-id="dea76-223">Измерения</span><span class="sxs-lookup"><span data-stu-id="dea76-223">Measurements</span></span> ###

<span data-ttu-id="dea76-224">При измерении значение + 1 еиженвалуе оператора соответствует `Zero` результату, а значение-1 еиженвалуе — `One` результату.</span><span class="sxs-lookup"><span data-stu-id="dea76-224">When measuring, the +1 eigenvalue of the operator being measured corresponds to a `Zero` result, and the -1 eigenvalue to a `One` result.</span></span>

> [!NOTE]
> <span data-ttu-id="dea76-225">Хотя это соглашение может показаться странным, оно имеет два очень замечательных преимущества.</span><span class="sxs-lookup"><span data-stu-id="dea76-225">While this convention might seem odd, it has two very nice advantages.</span></span>
> <span data-ttu-id="dea76-226">Во-первых, наблюдение за результатом $ \кет {0} $ представлено `Result` значением `Zero` , при котором наблюдение $ \кет {1} $ соответствует `One` .</span><span class="sxs-lookup"><span data-stu-id="dea76-226">First, observing the outcome $\ket{0}$ is represented by the `Result` value `Zero`, while observing $\ket{1}$ corresponds to `One`.</span></span>
> <span data-ttu-id="dea76-227">Во-вторых, мы можем написать, что еиженвалуе $ \ламбда $ соответствует результату, $r $ — $ \ламбда = (-1) ^ r $.</span><span class="sxs-lookup"><span data-stu-id="dea76-227">Second, we can write out that the eigenvalue $\lambda$ corresponding to a result $r$ is $\lambda = (-1)^r$.</span></span>

<span data-ttu-id="dea76-228">Операции измерения поддерживают ни `Adjoint` функтор, ни параметр `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="dea76-228">Measurement operations support neither the `Adjoint` nor the `Controlled` functor.</span></span>

<span data-ttu-id="dea76-229"><xref:Microsoft.Quantum.Intrinsic.Measure>Операция выполняет совместное измерение одного или нескольких Кубитс в указанном продукте операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="dea76-229">The <xref:Microsoft.Quantum.Intrinsic.Measure> operation performs a joint measurement of one or more qubits in the specified product of Pauli operators.</span></span>
<span data-ttu-id="dea76-230">Если массив Паули и массив кубит имеют разную длину, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dea76-230">If the Pauli array and qubit array are different lengths, then the operation fails.</span></span>
<span data-ttu-id="dea76-231">`Measure` имеет сигнатуру `((Pauli[], Qubit[]) => Result)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-231">`Measure` has signature `((Pauli[], Qubit[]) => Result)`.</span></span>

<span data-ttu-id="dea76-232">Обратите внимание, что совместное измерение не совпадает с измерением каждого кубит по отдельности.</span><span class="sxs-lookup"><span data-stu-id="dea76-232">Note that a joint measurement is not the same as measuring each qubit individually.</span></span>
<span data-ttu-id="dea76-233">Например, рассмотрим состояние $ \кет {11} = \кет {1} \отимес \Кет {1} = кс\отимес X \кет {00} $.</span><span class="sxs-lookup"><span data-stu-id="dea76-233">For example, consider the state $\ket{11} = \ket{1} \otimes \ket{1} = X\otimes X \ket{00}$.</span></span>
<span data-ttu-id="dea76-234">По отдельности измеряйте $Z _0 $ и $Z _1 $, чтобы получить результаты $r _0 = $1 и $r _1 = $1.</span><span class="sxs-lookup"><span data-stu-id="dea76-234">Measuring $Z_0$ and $Z_1$ each individually, we get the results $r_0 = 1$ and $r_1 = 1$.</span></span>
<span data-ttu-id="dea76-235">Однако при измерении $Z _0 Z_1 $ мы получаем один результат $r _ {\текстрм{жоинт}} = $0, представляющий, что пара $ \кет {11} $ является положительной.</span><span class="sxs-lookup"><span data-stu-id="dea76-235">Measuring $Z_0 Z_1$, however, we get the single result $r_{\textrm{joint}} = 0$, representing that the pairity of $\ket{11}$ is positive.</span></span>
<span data-ttu-id="dea76-236">Разместите иначе $ (-1) ^ {r_0 + r_1} = (-1) ^ r_ {\текстрм{жоинт}}) $.</span><span class="sxs-lookup"><span data-stu-id="dea76-236">Put differently, $(-1)^{r_0 + r_1} = (-1)^r_{\textrm{joint}})$.</span></span>
<span data-ttu-id="dea76-237">Важно, так как мы изучен *только* четность из этого измерения, все сведения о такте, представленные в подстановке 2 2 между кубит состояниями положительной четности, $ \кет {00} $ и $ \кет {11} $, сохраняются.</span><span class="sxs-lookup"><span data-stu-id="dea76-237">Critically, since we *only* learn the parity from this measurement, any quantum information represented in the superposition between the two two-qubit states of positive parity, $\ket{00}$ and $\ket{11}$, is preserved.</span></span>
<span data-ttu-id="dea76-238">Это свойство будет необходимо для дальнейшего использования, так как мы обсудим исправление ошибок.</span><span class="sxs-lookup"><span data-stu-id="dea76-238">This property will be essential later, as we discuss error correction.</span></span>

<span data-ttu-id="dea76-239">Для удобства версионного также предоставляет две другие операции для измерения Кубитс.</span><span class="sxs-lookup"><span data-stu-id="dea76-239">For convenience, the prelude also provides two other operations for measuring qubits.</span></span>
<span data-ttu-id="dea76-240">Во-первых, поскольку выполнение однокубитных измерений довольно распространено, версионного определяет сокращение для этого случая.</span><span class="sxs-lookup"><span data-stu-id="dea76-240">First, since performing single-qubit measurements is quite common, the prelude defines a shorthand for this case.</span></span>
<span data-ttu-id="dea76-241"><xref:Microsoft.Quantum.Intrinsic.M>Операция измеряет оператор паули $Z $ в одном кубит и имеет сигнатуру `(Qubit => Result)` .</span><span class="sxs-lookup"><span data-stu-id="dea76-241">The <xref:Microsoft.Quantum.Intrinsic.M> operation measures the Pauli $Z$ operator on a single qubit, and has signature `(Qubit => Result)`.</span></span>
<span data-ttu-id="dea76-242">`M(q)` равно `Measure([PauliZ], [q])`.</span><span class="sxs-lookup"><span data-stu-id="dea76-242">`M(q)` is equivalent to `Measure([PauliZ], [q])`.</span></span>

<span data-ttu-id="dea76-243"><xref:microsoft.quantum.measurement.MultiM>Оператор паули $Z $ измеряется *отдельно* для каждого массива Кубитс, возвращая *массив* `Result` значений, полученных для каждого кубит.</span><span class="sxs-lookup"><span data-stu-id="dea76-243">The <xref:microsoft.quantum.measurement.MultiM> measures the Pauli $Z$ operator *separately* on each of an array of qubits, returning the *array* of `Result` values obtained for each qubit.</span></span>
<span data-ttu-id="dea76-244">В некоторых случаях это можно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="dea76-244">In some cases this can be optimized.</span></span> <span data-ttu-id="dea76-245">Он имеет подпись ( `Qubit[] => Result[])` .</span><span class="sxs-lookup"><span data-stu-id="dea76-245">It has signature (`Qubit[] => Result[])`.</span></span>
<span data-ttu-id="dea76-246">`MultiM(qs)` эквивалентно следующему:</span><span class="sxs-lookup"><span data-stu-id="dea76-246">`MultiM(qs)` is equivalent to:</span></span>

```qsharp
mutable rs = new Result[Length(qs)];
for (index in 0..Length(qs)-1)
{
    set rs[index] = M(qs[index]);
}
return rs;
```

## <a name="extension-functions-and-operations"></a><span data-ttu-id="dea76-247">Функции и операции расширения</span><span class="sxs-lookup"><span data-stu-id="dea76-247">Extension Functions and Operations</span></span> ##

<span data-ttu-id="dea76-248">Кроме того, версионного определяет широкий набор математических функций и функции преобразования типов на уровне .NET для использования в Q# коде.</span><span class="sxs-lookup"><span data-stu-id="dea76-248">In addition, the prelude defines a rich set of mathematical and type conversion functions at the .NET level for use within Q# code.</span></span>
<span data-ttu-id="dea76-249">Например, <xref:Microsoft.Quantum.Math> пространство имен определяет полезные операции, такие как <xref:Microsoft.Quantum.Math.Sin> и <xref:Microsoft.Quantum.Math.Log> .</span><span class="sxs-lookup"><span data-stu-id="dea76-249">For instance, the <xref:Microsoft.Quantum.Math> namespace defines useful operations such as <xref:Microsoft.Quantum.Math.Sin> and <xref:Microsoft.Quantum.Math.Log>.</span></span>
<span data-ttu-id="dea76-250">Реализация, предоставляемая пакетом разработки тактовой передачи, использует классическую библиотеку базовых классов .NET и, таким же, может затрагивать дополнительный обмен информацией между тактовыми программами и их классическими драйверами.</span><span class="sxs-lookup"><span data-stu-id="dea76-250">The implementation provided by the Quantum Development Kit uses the classical .NET base class library, and thus may involve an additional communications round trip between quantum programs and their classical drivers.</span></span>
<span data-ttu-id="dea76-251">Хотя это и не является проблемой для локального симулятора, это может быть проблемой с производительностью при использовании удаленного симулятора или реального оборудования в качестве целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="dea76-251">While this does not present a problem for a local simulator, this can be a performance issue when using a remote simulator or actual hardware as a target machine.</span></span>
<span data-ttu-id="dea76-252">С другой стороны, отдельный целевой компьютер может уменьшить это воздействие на производительность, переопределив эти операции с использованием версий, которые более эффективны для конкретной системы.</span><span class="sxs-lookup"><span data-stu-id="dea76-252">That said, an individual target machine may mitigate this performance impact by overriding these operations with versions that are more efficient for that particular system.</span></span>

### <a name="math"></a><span data-ttu-id="dea76-253">Математический</span><span class="sxs-lookup"><span data-stu-id="dea76-253">Math</span></span> ###

<span data-ttu-id="dea76-254"><xref:Microsoft.Quantum.Math>Пространство имен предоставляет множество полезных функций из [ `System.Math` класса](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1&preserve-view=true)библиотеки базовых классов .NET.</span><span class="sxs-lookup"><span data-stu-id="dea76-254">The <xref:Microsoft.Quantum.Math> namespace provides many useful functions from the .NET base class library's [`System.Math` class](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1&preserve-view=true).</span></span>
<span data-ttu-id="dea76-255">Эти функции можно использовать так же, как и любые другие Q# функции:</span><span class="sxs-lookup"><span data-stu-id="dea76-255">These functions can be used in the same manner as any other Q# functions:</span></span>

```qsharp
open Microsoft.Quantum.Math;
// ...
let y = Sin(theta);
```

<span data-ttu-id="dea76-256">Если статический метод .NET перегружен в зависимости от типа его аргументов, соответствующая Q# функция помечается суффиксом, указывающим тип входных данных:</span><span class="sxs-lookup"><span data-stu-id="dea76-256">Where a .NET static method has been overloaded based on the type of its arguments, the corresponding Q# function is annotated with a suffix indicating the type of its input:</span></span>

```qsharp
let x = AbsI(-3); // x : Int = 3
let y = AbsD(-PI()); // y : Double = 3.1415...
```


### <a name="bitwise-operations"></a><span data-ttu-id="dea76-257">Битовые операции</span><span class="sxs-lookup"><span data-stu-id="dea76-257">Bitwise Operations</span></span> ###

<span data-ttu-id="dea76-258">Наконец, <xref:Microsoft.Quantum.Bitwise> пространство имен предоставляет несколько полезных функций для управления целыми числами с помощью побитовых операторов.</span><span class="sxs-lookup"><span data-stu-id="dea76-258">Finally, the <xref:Microsoft.Quantum.Bitwise> namespace provides several useful functions for manipulating integers through bitwise operators.</span></span>
<span data-ttu-id="dea76-259">Например, <xref:Microsoft.Quantum.Bitwise.Parity> возвращает побитовую четность целого числа в виде другого целого числа.</span><span class="sxs-lookup"><span data-stu-id="dea76-259">For instance, <xref:Microsoft.Quantum.Bitwise.Parity> returns the bitwise parity of an integer as another integer.</span></span>
