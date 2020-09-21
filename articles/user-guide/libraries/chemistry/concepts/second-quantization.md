---
title: Второй дискретизация
description: Узнайте о втором дискретизация подходе к моделированию электронных структур в процессе программирования.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.secondquantization
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6becd348f7b3957cb60b16bbd5a28228527e1d4c
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835814"
---
# <a name="second-quantization"></a>Второй дискретизация

Вторая дискретизация просматривает проблему с электронной структурой с помощью другой линзы.
Вместо того, чтобы назначать каждому $N _e $ электронному состоянию (или Орбитал), второй дискретизация отслеживает каждый Орбитал и сохраняет, есть ли электроны в каждом из них, и в то же время автоматически гарантирует свойства симметрии соответствующей функции Wave.
Это важно, так как позволяет задавать химияные модели, не беспокоясь о том, что симметризинг входное состояние (как это требуется для фермионс), а также потому, что вторая дискретизация позволяет имитировать такие модели с помощью небольших тактовых компьютеров.

В качестве примера второго дискретизация в действии Предположим, что $ \ psi_0 \кдотс \ psi_ {N-1} $ являются орсонормал набором пространственных орбит.
Эти орбиты выбираются для представления системы как можно точнее в рамках рассматриваемого базового набора.
Распространенный пример таких орбит — атомарные орбиты, которые формируют еиженбасис для атома водорода.
Так как электроны имеют два оборота, два электрона могут быть краммед на каждый такой пространственный Орбитал.
Например, допустимыми являются следующие состояния: $ \ psi_ {0, \упарров}, \лдотс, \ psi_ {N-1, \упарров}, \ psi_ {0, \довнарров}, \лдотс, \ psi_ {N-1, \довнарров} $ WHERE $ \упарров $ и $ \довнарров $ являются метками, которые задают две еиженстатес степени свободы.
Этот комбинированный индекс $ (j, \сигма) $ для $ \сигма \ин \{ \упарров, \довнарров \} $ называется Spin-Орбитал, так как он хранит как пространственный, так и степень свободы.
В библиотеке химия объект Spin-орбиты хранится в `SpinOrbital` структуре данных и создается следующим образом.

```csharp
    // First, we load the namespace containing spin-orbital objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // First, we assign an orbital index, say `5`. Note that we use 0-indexing,
    // so this is the 6th orbital.
    var orbitalIdx = 5;

    // Second, we assign a spin index, say `Spin.u` for spin up or `Spin.d` for spin down.
    var spin = Spin.d;

    // the spin-orbital (5, ↓) is then
    var spinOrbital = new SpinOrbital(orbitalIdx, spin);

    // A tuple `(int, Spin)` is also implicitly recognized as a spin-orbital.
    (int, Spin) tuple = (orbitalIdx, spin);

    // We explicitly specify the type of `spinOrbital1` to demonstrate
    // the implicit cast to `SpinOrbital`.
    SpinOrbital spinOrbital1 = tuple;
```

Это означает, что мы можем формально представить базу для прокрутки и пространственной части функции Wave как $ \ psi_ {0} \кдотс \ psi_ {2n-1} $, где каждый из индексов теперь является перечислением $ (j, \сигма) $.
Одно возможное перечисление — $g (j, \сигма) = j + Н\сигма ' $.
Другое возможное перечисление — $h (j, \сигма) = 2 * j + \сигма $.
В библиотеке тактов химия можно использовать эти соглашения, а при создании экземпляра этой кодировки можно создать экземпляр с вращением, как показано ниже.

```csharp
    // Let us use the spin orbital created in the previous snippet.
   var spinOrbital = new SpinOrbital(5, Spin.d);

   // Let us set the total number of orbitals to be say, `7`.
   var nOrbitals = 7;

    // This converts a spin-orbital index to a unique integer, in this case `12`,
    // using the formula `g(j,σ)`.
    var integerIndexHalfUp = spinOrbital.ToInt(IndexConvention.HalfUp);

    // This converts a spin-orbital index to a unique integer, in this case `11`,
    // using the formula `h(j,σ)`.
    var integerIndexUpDown = spinOrbital.ToInt(IndexConvention.UpDown);

    // The default conversion uses the formula `h(j,σ)`, in this case `11`.
    var integerIndexDefault = spinOrbital.ToInt();
```

Для систем фермионик принцип исключения Паули предотвращает присутствие более одного электронного представления в каком-Орбитал в то же время.
Это означает, что можно написать два юридических состояния для $ \ psi_1 $ AS \бегин{екуатион} \ psi_1 \ригхтарров \бегин{Касес} \кет {0} _1 & \текст{ИФ $ \ psi_1 $ не занят,} \\\
\кет {1} _1 & \текст{ИФ $ \ psi_1 $ занято.} \енд{Касес} \енд{екуатион} эта кодировка отлично подходит для тактовых компьютеров, так как это означает, что мы можем хранить электронную должность как один тактовый бит.

Состояния профессий для орбит $2N $ Spin также могут храниться в $2N $ Кубитс.
Например, если $N = $2, то State $ $ \кет {0} \кет {1} \кет {1} \кет {0} , $ $

будет соответствовать прокрутки по орбитам $1 $ и $2 $, которые будут свободны с остатком.
Аналогично, State $ $ \кет {0} \екуив \кет {0} _ {0} \кдотс \кет {0} _{N-1}, $ $

не имеет электронов и называется "состоянием очистки".

Прекрасным побочным эффектом второго дискретизация является то, что больше не нужно явным образом отследить электросимметрию состояния такта.
Это связано с тем, что, как мы увидим, неопределенность состояния представляет собой саму себя с помощью коммутатион правил операторов, которые создают и удаляют электронные профессии прокрутки Орбитал.

## <a name="fermionic-operators"></a>Операторы фермионик

Два фундаментальных оператора, которые действуют на основе второго квантования, называются операторами создания и аннихилатион.
Эти операторы вставляют или удаляют электронную страну в определенном месте.
Они обозначаются $a ^ \ dagger_j $ и $a _j $ соответственно.

Например, \бегин{алигн} a ^ \ dagger_1 \кет {0} _1 = \кет {1} _1, \куад a ^ \ dagger_1 \кет {1} _1 = 0, \куад A_1 \кет {0} _1 = 0, \куад A_1 \кет {1} _1 = \кет {0} _1.
\енд{алигн} Обратите внимание, что здесь $a ^ \ dagger_1 \кет {1} _1 = 0 $ and $a _1 \кет {0} _1 $ дает нулевой вектор, отличный от $ \кет {0} _1 $.
Поэтому такие операторы не являются ни Хермитиан, ни единым.
Мы представляем общие операторы создания и аннихилатион, использующие <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> тип.
Например, один оператор создания представлен ниже.

```csharp
    // We load the namespace containing ladder operator objects.
    using Microsoft.Quantum.Chemistry.LadderOperators;

    // Let us use the spin orbital created in the previous snippet.
    var spinOrbitalInteger = new SpinOrbital(5, Spin.d).ToInt();

    // We specify either a creation or annihilation operator using 
    // the enumerable type `RaisingLowering.u` or `RaisingLowering.d`
    // respectively;
    var creationEnum = RaisingLowering.u;

    // The type representing a creation operator is then initialized 
    // as follows. Here, we index these operators with integers.
    // Hence we initialize the generic ladder operator with an
    // integer index type.
    var ladderOperator0 = new LadderOperator<int>(creationEnum, spinOrbitalInteger);

    // An alternate constructor for a LadderOperator instead uses
    // a tuple.
    var ladderOperator1 = new LadderOperator<int>((creationEnum, spinOrbitalInteger));
```

Кроме того, с помощью таких операторов можно выразить $ $ \кет {0} \кет {1} \кет {1} \кет {0} = a ^ \ dagger_1 a ^ \ dagger_2 \кет {0} ^ {\отимес 4}.
$ $ Эта последовательность операторов будет построена в библиотеке моделирования Хамилтониан с помощью кода C#, подобного орбиталу, рассмотренному выше:
```csharp
    // We load the namespace containing fermion-related objects.
    using Microsoft.Quantum.Chemistry.Fermion;

    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We can convert this array of tuples to a sequence of ladder
    // operators using the `ToLadderSequence()` methods.
    var ladderSequences = indices.ToLadderSequence();

    // Sequences of ladder operators are quite general. For instance,
    // they could be bosonic operators, instead of fermionic operators.
    // We specialize them by constructing a `FermionTerm` representing 
    // a fermion creation operator on the index `2` followed by `1`.
    var fermionTerm = new FermionTerm(ladderSequences);
```

Для системы $k $ Фермионс в секунду дискретизация действия оператора создания $a ^ \ dagger_i $ задается в $ $ a ^ \ dagger_i \кет{n_1, n_2, \лдотс, 0_i, \лдотс, n_k} = (-1) ^ {S_i} \кет{n_1, n_2, \лдотс, 1_i, \лдотс, n_k}, $ $ и $ $ a ^ \ dagger_i \кет{n_1, n_2, \лдотс, 1_i, \лдотс, n_k} = 0, $ $, где $S _i = \ sum_ {j<i} a ^ \ dagger_j a_j $ измеряет общее число Фермионс, которые находятся в состоянии одной частицы и имеют индекс $j < i $.

Третий оператор также часто используется во втором представлении квантования.
Этот оператор известен как оператор Number и определяется \бегин{екуатион} n_i = a ^ \ dagger_i a_i.
\енд{екуатион}. Этот оператор подсчитывает роду данного цикла Орбитал, который означает \бегин{алигн} n_i \кет {0} _i &= 0 \ нечисловое значение\\\
n_i \кет {1} _i &= \кет {1} _i.
\енд{алигн}, как и в приведенных выше `FermionTerm` примерах, этот оператор Number создается следующим образом.
```csharp
    // Let us use a new method to compactly create a sequence of ladder
    // operators. Note that we have omitted specifying whether the 
    // operators are raising or lowering. In this case, the first half
    // will be raising operators, and the second half will be lowering 
    // operators.
    var indices = new[] { 1, 1 }.ToLadderSequence();

    // We now construct a `FermionTerm` representing an annihilation operator
    // on the index 1 followed by the creation operator on the index 1.
    var fermionTerm0 = new FermionTerm(indices);
```

Однако при использовании операторов создания или аннихилатион в системах фермионик возникают тонкости.
Для обмена метками требуется, чтобы любое допустимое состояние такта было несимметричным.
Это означает, что $ $ a ^ \ dagger_2 а ^ \ dagger_1 \кет {0} =-a ^ \ dagger_1 a ^ \ dagger_2 \кет {0} .
$ $ Такие операторы называются «незащищенными» и в целом для любых $i j $ мы добавили, что \бегин{алигн} ^ \ dagger_i a ^ \ dagger_j =-(1 – \ delta_ {i, j}) а ^ \ dagger_j a ^ \ dagger_i, \куад а ^ \ dagger_i a_j = \ delta_ {i, j} — a_j a ^ \ dagger_i.
\енд{алигн}, что следующие два <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> экземпляра считаются неэквивалентными
```csharp
    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We now construct a `LadderSequence` representing a creation operator
    // on the index 1 followed by 2, then a term with the reverse ordering.
    var laddderSeqeunce = indices.ToLadderSequence();
    var laddderSeqeunceReversed = indices.Reverse().ToLadderSequence();

    // The following Boolean is `false`.
    var equal = laddderSeqeunce == laddderSeqeunceReversed;
```

Необходимость в каждом из операторов создания означает, что использование второго квантования представления делает избежать проблемы, с которыми сталкиваются сглаживание Фермионс.
Вместо этого запрос перейдет в определение операторов создания. 

Используя правила защиты от коммутатион, некоторые `LadderSequence` экземпляры фактически соответствуют одной последовательности операторов фермионик, иногда до знака минус.
Например, рассмотрим Хамилтониан $a _0 ^ \дагжер a_1 ^ \дагжер a_1 a_0 =-a_1 ^ \дагжер a_0 ^ \дагжер a_1 a_0 $.
Это мотивация, что нам нужно определить каноническую сортировку для каждого из них `FermionTerm` .
Любой `FermionTerm` из них автоматически помещается в канонический порядок, как показано ниже.
```csharp
    // We now construct two `FermionTerms` that are equivalent with respect to
    // anti-commutation up to a sign change.
    var fermionTerm0 = new FermionTerm(new[] { 0, 1, 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 1, 0, 1, 0 }.ToLadderSequence());

    // The following Boolean is `true`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // The change in sign is not compared above, but is an internally tracked
    // property of `FermionTerm`.
    int sign0 = fermionTerm0.Coefficient;
    var sign1 = fermionTerm1.Coefficient;

    // The following Boolean is `false`.
    var signEqual = sign0 == sign1;
```

## <a name="second-quantized-fermionic-hamiltonian"></a>Второй-квантования Фермионик Хамилтониан

Возможно, неудивительно, что Хамилтониан в [тактовых моделях для электронных систем](xref:microsoft.quantum.chemistry.concepts.quantummodels) можно написать с точки зрения операторов создания и аннихилатион.
В частности, если $ \пси \_ j $ — это оборотные орбиты, которые формируют базу, то

\бегин{екуатион} \Хат{х} = \сум \_ {PQ} h \_ {PQ} a ^ \дагжер \_ p a \_ q + \фрак {1} {2} \сум \_ {пкрс} h \_ {пкрс} a ^ \дагжер \_ p a ^ \дагжер \_ \_ \_ \_ . \текстрм} NUC, где $h \_ {\лабел{ЕК totalHam} $ — это ядерная энергия (которая является константой в соответствии с аппроксимацией \end{Equation}) и

\бегин{алигн} h \_ {PQ} &= \инт \_ {-\инфти} ^ \инфти \пси ^ \* \_ p (x \_ 1) \лефт (-\Фрак{\набла ^ 2} {2} + V (x \_ 1) \ригхт) \пси \_ q (x \_ 1) \масрм{д} ^ 3 раза \_ 1, \енд{алигн}

где $V (x) $ является потенциалом среднего поля и

\бегин{алигн} h \_ {пкрс} &= \инт \_ {-\инфти} ^ \инфти \инт \_ {-\инфти} ^ \инфти\пси \_ p ^ \* (x \_ 1) \пси \_ q ^ \* (x \_ 2) \лефт (\фрак {1} {| x_1-x_2 |} \ригхт) \psi \_ r (x \_ 2) \psi \_ s (x \_ 1) \mathrm{d} ^ 3 раза \_ 1 \ mathrm {d} ^ 3 раза \_ 2. \ Label {EQ: интегралы} \end{align}

Термины $h \_ {PQ} $ называются одноэлектронными интегралами, так как все эти термины содержат только отдельные электроны и точно так же $h \_ {пкрс} $ — это два электронных интеграла.
Они называются интегралами, так как вычисление значений этих коэффициентов требует целого.
В одном электронном соглашении описываются Кинетик энергия отдельных электронов и их взаимодействие с электрическими полями нуклеи.
Два электронных интеграла с другой стороны описывают взаимодействие между электронными сообщениями.

Интуиция для того, что означают эти термины, можно получить от операторов создания и аннихилатион, составляющих каждый из них.
Например, $h _ {PQ} a ^ \ dagger_p a_q $ описывает электронную прыгающее» из счетчика Орбитал $q $ to Spin Орбитал $p $.
Аналогичным образом, термин $h _ {пкрс} a ^ \ dagger_p a ^ \ dagger_q a_r a_s $ (для различных $p, q, r, s $) описывает два электрона в обороте по орбитам $r $ и $s $ разбросанность друг от друга и завершается на обороте по орбите $p $ и $q $.
Если $r = q $ and $p = s $, $h _ {ПРРП} a ^ \ dagger_p a ^ \ dagger_r a_r a_p = h_ {ПРРП} n_p n_r $ обеспечивает снижение энергии, связанное с двумя электронными, которые находятся ближе друг к другу, но не описывает динамический процесс.

Мы можем представить такие Хамилтонианс с помощью `FermionHamiltonian` класса, который, по сути, является списком, содержащим все нужные `FermionTerm` экземпляры.
Поскольку Хамилтонианс являются Хермитиан по определению, мы индексируют термины, использующие более специализированный тип `HermitianFermionTerm` , который также использует симметрию хермитиан при проверке эквивалентности терминов.

Позвольте нам создать несколько наглядных примеров.
Рассмотрим Хамилтониан $ \Хат{х} = a_0 ^ \дагжер a_1 + a_1 ^ \дагжер a_0 $.
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the terms to be added.
    var fermionTerm0 = new FermionTerm(new[] { 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 0, 1 }.ToLadderSequence());

    // These fermion terms are not equal. The following Boolean is `false`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // However, these terms are equal under Hermitian symmetry.
    // We also take the opportunity to demonstrate equivalent constructors
    // for hermitian fermion terms
    var hermitianFermionTerm0 = new HermitianFermionTerm(fermionTerm0);
    var hermitianFermionTerm1 = new HermitianFermionTerm(new[] { 0, 1 });

    // These Hermitian fermion terms are equal. The following Boolean is `true`.
    var hermitianSequenceEqual = hermitianFermionTerm0 == hermitianFermionTerm1;

    // We add the terms to the Hamiltonian with the appropriate coefficient.
    // Note that these terms are identical.
    hamiltonian.Add(hermitianFermionTerm0, 1.0);
    hamiltonian.Add(hermitianFermionTerm1, 1.0);
```
Мы можем упростить эту конструкцию, используя тот факт, что операторы Хамилтониан являются операторами Хермитиан.
При добавлении терминов в Хамилтониан с помощью `Add` любой термин, не относящийся к хермитиан, например `fermionTerm0` , считается сопряженным с его хермитианным сопряженным.
Таким образом, следующий фрагмент кода также представляет один и тот же Хамилтониан:
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the term to be added -- note the doubled coefficient.
    hamiltonian.Add(new HermitianFermionTerm(new[] { 1, 0 }), 2.0);
```

Используя правила защиты от коммутатион, некоторые `FermionTerm` экземпляры в хамилтониан на самом деле соответствуют одной последовательности операторов фермионик, иногда до знака минус.
Например, рассмотрим Хамилтониан $H = a_0 ^ \дагжер a_1 ^ \дагжер a_1 a_0-a_1 ^ \дагжер a_0 ^ \дагжер a_1 a_0 = 2a_0 ^ \дагжер a_1 ^ \дагжер a_1 a_0 $, который является суммой ранее построенных терминов.
Не всегда ясно, что это эквивалентно условиям, и поэтому их можно добавить в Хамилтониан отдельно.
Кроме того, может быть интересно изменить уже существующие термины в Хамилтониан.
В этих случаях можно сочетать эквивалентные термины следующим образом.
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We now create two Hermitian fermion terms that are equivalent with respect to
    // anti-commutation and Hermitian symmetry.
    var terms = new[] {
        (new[] { 0, 1, 1, 0 }, 1.0),
        (new[] { 1, 0, 1, 0 }, 1.0) }
    .Select(o => (new HermitianFermionTerm(o.Item1.ToLadderSequence()), o.Item2.ToDoubleCoeff()));

    // Now add `terms` to the Hamiltonian.
    hamiltonian.AddRange(terms);

    // There is only one unique term. `nTerms == 1` is `true`.
    var nTerms = hamiltonian.CountTerms();
```
Комбинируя коэффициенты эквивалентных терминов, мы уменьшаем общее количество терминов в Хамилтониан.
В дальнейшем это сокращает количество шлюзов, необходимых для имитации Хамилтониан.

### <a name="internal-representation"></a>Внутреннее представление

Фермионик Хамилтониан с двумя и двусторонними взаимодействиями представлен в нотации Second-квантования как

$ $ \бегин{алигн} H = \сум \_ {PQ} h \_ {PQ} a ^ \дагжер \_ {p} a \_ {q} + \фрак {1} {2} \сум \_ {пкрс} H \_ {пкрс} а ^ \дагжер \_ {p} a ^ \дагжер \_ {q} a \_ {r} a \_ {s}.
\енд{алигн} $ $

В этой нотации существует не более $N коэффициентов: ^ 2 + N ^ 4 $.
Однако многие из этих коэффициентов можно собрать, так как они соответствуют одному оператору.
Например, если $p, q, r, s $ — это разные индексы. мы можем использовать правила защиты от коммутатион, чтобы отобразить следующее: $ $ a ^ \дагжер \_ {p} a ^ \дагжер \_ {q} \_ {r} a \_ {s} =-a ^ \дагжер \_ {q} a ^ \дагжер \_ {p} a \_ {r} a \_ {s} =-a ^ \дагжер \_ {p} a ^ \дагжер \_ {q} a \_ {s} a \_ {r} = a ^ \дагжер \_ {q} a ^ \дагжер \_ {p} a \_ {s} a \_ {r}.
$$

Более того, поскольку $H $ является Хермитиан, каждый оператор, не Хермитиан фермионик, скажем $h \_ {пкрс} a ^ \дагжер \_ {p} a ^ \дагжер \_ {q} a \_ {r} a \_ {s} $, имеет хермитиан сопряженный, который также находится в $H $. Чтобы обеспечить уникальную индексацию групп терминов, характеризующих эти симметриес, мы определяем каноническое упорядочение по индексам $ (i \_ 1, \кдотс, i \_ n, j \_ 1, \кдотс, j \_ m) $ любой последовательности $n + m $ фермионик Operators $a ^ \дагжер \_ {i \_ 1} \кдотс a \_ \_ \_ \_ \_ {j \_ m} $as следующим образом:
-   Все операторы создания $a ^ \дагжер \_ {i \_ \кдот} $ помещаются перед всеми операторами аннихилатион $a \_ {j \_ \кдот} $.
-   Все индексы операторов создания сортируются в возрастающем порядке, то есть $i \_ 1< i \_ 2< \кдотс < я \_ n $.
-   Все индексы операторов аннихилатион сортируются в убывающем порядке, то есть $j \_ 1> j \_ 2 \кдотс > j \_ m $.
-   Самый левый индекс меньше или равен правому индексу, то есть $i \_ 1 – Le j \_ m $.

Мы можем определить этот набор канонических упорядоченных индексов как $ $ \бегин{алигн} (i \_ 1, \кдотс, i \_ n, j \_ 1, \кдотс, j \_ m) \ин S \_ {n, m}.
\енд{алигн} $ $

При таком каноническом упорядочении фермионик Хамилтониан может быть выражен как $ $ \бегин{алигн} H = \сум \_ {(p, q) \Ин S \_ {1,1} } H ' \_ {PQ} \фрак{а ^ \дагжер \_ {p} a \_ {q} + a ^ \дагжер { \_ q} a \_ {p}} {2} + \сум \_ {(p, q, r, s) \ин S \_ {2,2} } H ' \_ {пкрс} \фрак{а ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {S} + a ^ \dagger \_ {s} a ^ \dagger \_ {r} \_ {q} a \_ {p}} {2} , \end{align} $ $ с соответствующим образом адаптированные и два электронных $h " \_ {PQ} $ и $h" \_ {PQRS} $ соответственно ".

