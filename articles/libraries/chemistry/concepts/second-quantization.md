---
title: Второй дискретизация | Документация Майкрософт
description: Вторые дискретизация документы
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.secondquantization
ms.openlocfilehash: 4b7b5a6be6d0c1f3520128609e6b9fa83e5460d5
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036429"
---
# <a name="second-quantization"></a>Второй дискретизация

Вторая дискретизация просматривает проблему с электронной структурой с помощью другой линзы.
Вместо того, чтобы назначать каждому $N _e $ электронному состоянию (или Орбитал), второй дискретизация отслеживает каждый Орбитал и сохраняет, есть ли электроны в каждом из них, и в то же время автоматически гарантирует свойства симметрии соответствующая функция Wave.
Это важно, так как позволяет задавать химияные модели, не заботясь о том, что требуется для фермионс, а также потому, что вторая дискретизация позволяет имитировать такие модели с помощью малого такта. компьютером.

В качестве примера второго дискретизация в действии Предположим, что $ \ psi_0 \кдотс \ psi_ {N-1} $ являются орсонормал набором пространственных орбит.
Эти орбиты выбираются для представления системы как можно точнее в рамках рассматриваемого базового набора.
Распространенный пример таких орбит — атомарные орбиты, которые формируют еиженбасис для атома водорода.
Так как электроны имеют два оборота, два электрона могут быть краммед на каждый такой пространственный Орбитал.
Например, допустимыми являются следующие состояния: $ \ psi_ {0, \упарров}, \лдотс, \ psi_ {N-1, \упарров}, \ psi_ {0, \довнарров}, \лдотс, \ psi_ {N-1, \довнарров} $ WHERE $ \упарров $ и $ \довнарров $ являются метками, которые задают две еиженстатес из прокрутки степени обеспечат.
Этот комбинированный индекс $ (j, \сигма) $ для $ \сигма \ин \{\упарров, \довнарров\}$ называется Spin-Орбитал, так как он хранит как пространственный, так и степень свободы.
В библиотеке химия «Spin-орбиты» хранятся в структуре данных `SpinOrbital` и создаются следующим образом.

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

Это означает, что мы можем формально представить базу для прокрутки и пространственной части функции Wave как $ \ psi_{0} \кдотс \ psi_ {2N-1} $, где каждый из индексов теперь является перечислением $ (j, \сигма) $.
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
Это означает, что мы можем написать два юридических состояния для $ \ psi_1 $ AS \бегин{екуатион} \ psi_1 \ригхтарров \бегин{Касес} \кет{0}_1 & \текст{ИФ $ \ psi_1 $ не занят,} \\\
\кет{1}_1 & \текст{ИФ $ \ psi_1 $.} \енд{Касес} \енд{екуатион} эта кодировка отлично подходит для тактовых компьютеров, так как это означает, что мы можем хранить электронную должность как один тактовый бит.

Состояния профессий для орбит $2N $ Spin также могут храниться в $2N $ Кубитс.
Например, если $N = $2, то State $ $ \кет{0} \кет{1} \кет{1} \кет{0}, $ $

будет соответствовать прокрутки по орбитам $1 $ и $2 $, которые будут свободны с остатком.
Аналогично, State $ $ \кет{0} \екуив \кет{0} _{0} \кдотс \кет{0}_ {N-1}, $ $

не имеет электронов и называется "состоянием очистки".

Прекрасным побочным эффектом второго дискретизация является то, что больше не нужно явным образом отследить электросимметрию состояния такта.
Это связано с тем, что, как мы увидим, неопределенность состояния представляет собой саму себя с помощью коммутатион правил операторов, которые создают и удаляют электронные профессии прокрутки Орбитал.

## <a name="fermionic-operators"></a>Операторы фермионик

Два фундаментальных оператора, которые действуют на основе второго квантования, называются операторами создания и аннихилатион.
Эти операторы вставляют или удаляют электронную страну в определенном месте.
Они обозначаются $a ^ \ dagger_j $ и $a _j $ соответственно.

Например, \бегин{алигн} a ^ \ dagger_1 \кет{0}_1 = \кет{1}_1, \куад a ^ \ dagger_1 \кет{1}_1 = 0, \куад a_1 \кет{0}_1 = 0, \куад a_1 \кет{1}_1 = \кет{0}_1.
\енд{алигн} Обратите внимание, что здесь $a ^ \ dagger_1 \кет{1}_1 = 0 $ and $a _1 \кет{0}_1 $ дает нулевой вектор, отличный от $ \кет{0}_1 $.
Поэтому такие операторы не являются ни Хермитиан, ни единым.
Мы представляем общие операторы создания и аннихилатион, использующие тип <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1>.
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

Кроме того, с помощью таких операторов можно выразить $ $ \кет{0} \кет{1} \кет{1} \кет{0} = a ^ \ dagger_1 a ^ \ dagger_2 \кет{0}^ {\отимес 4}.
$ $ Эта последовательность операторов будет построена в библиотеке моделирования Хамилтониан с использованием C# кода, подобного орбиталному варианту с одним прокруткой, как описано выше:
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

Для системы $k $ Фермионс в секунду дискретизация действия оператора создания $a ^ \ dagger_i $ задается в $ $ a ^ \ dagger_i \кет{n_1, n_2, \лдотс, 0_i, \лдотс, n_k} = (-1) ^ {S_i} \кет{n_1, n_2, \лдотс, 1_i , \лдотс, n_k}, $ $ и $ $ a ^ \ dagger_i \кет{n_1, n_2, \лдотс, 1_i, \лдотс, n_k} = 0, $ $, где $S _i = \ sum_ {j < i} a ^ \ dagger_j a_j $ измеряет общее число Фермионс, которые находятся в состоянии одной части и имеют индекс $j < i $.

Третий оператор также часто используется во втором представлении квантования.
Этот оператор известен как оператор Number и определяется \бегин{екуатион} n_i = a ^ \ dagger_i a_i.
\енд{екуатион} этот оператор подсчитывает роду данного цикла Орбитал, который означает \бегин{алигн} n_i \кет{0}_i & = 0 \ число\\\
n_i \кет{1}_i & = \кет{1}_i.
\енд{алигн}, как в приведенных выше примерах `FermionTerm`, этот оператор Number создается следующим образом.
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
Это означает, что $ $ a ^ \ dagger_2 а ^ \ dagger_1 \кет{0} =-a ^ \ dagger_1 dagger_2 ^ \{0}\кет.
$ $ Такие операторы называются «незащищенными» и в целом для любых $i j $ мы добавили, что \бегин{алигн} ^ \ dagger_i a ^ \ dagger_j =-(1 – \ delta_ {i, j}) а ^ \ dagger_j a ^ \ dagger_i, \куад а ^ \ dagger_i a_j = \ delta_ {i, j} — a_j a ^ \ dagger_i.
\енд{алигн}, что следующие два экземпляра <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> считаются неэквивалентными
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

Используя правила защиты от коммутатион, некоторые экземпляры `LadderSequence` фактически соответствуют одной последовательности операторов фермионик, иногда до знака минус.
Например, рассмотрим Хамилтониан $a _0 ^ \дагжер a_1 ^ \дагжер a_1 a_0 =-a_1 ^ \дагжер a_0 ^ \дагжер a_1 a_0 $.
Это мотивация, что нам нужно определить каноническую сортировку для каждого `FermionTerm`.
Любой `FermionTerm` автоматически помещается в канонический порядок, как показано ниже.
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
В частности, если $ \пси\_j $ — это оборотные орбиты, которые формируют базу, то

\бегин{екуатион} \Хат{х} = \сум\_{PQ} H\_{PQ} a ^ \дагжер\_p a\_q + \фрак{1}{2}\сум\_{пкрс} H\_{пкрс} a ^ \дагжер\_p a ^ \дагжер\_q a\_RA\_s + H\_{\текстрм NUC} \лабел{ЕК: totalHam} \end{Equation}, где $h\_{\textrm NUC} $ — это атомная энергия (которая является константой по приближению рождения-Oppenheimer) и

\бегин{алигн} h\_{PQ} & = \инт\_{-\инфти} ^ \инфти \пси ^\*\_p (x\_1) \лефт (-\фрак{\набла ^ 2}{2} + V (x\_1) \ригхт) \пси\_q (x\_1) \масрм{д} ^ 3 раза\_1, \енд{алигн}

где $V (x) $ является потенциалом среднего поля и

\бегин{алигн} h\_{пкрс} & = \инт\_{-\инфти} ^ \инфти \инт\_{-\инфти} ^ \инфти\пси\_p ^\*(x\_1) \пси\_q ^\*(x\_2) \лефт (\фрак{1}{| x_1-x_2 |} \ригхт) \psi\_r (x\_2) \psi\_s (x\_1) \mathrm{d} ^ 3 раза\_1 \ mathrm {d} ^ 3 раза\_2. \ метка {EQ : интегралы} \енд{алигн}

Термины $h\_{PQ} $ называются одноэлектронными интегралами, так как все эти термины подразумевают только отдельные электроны и аналогично $h\_{пкрс} $ — это два электронных интеграла.
Они называются интегралами, так как вычисление значений этих коэффициентов требует целого.
В одном электронном соглашении описываются Кинетик энергия отдельных электронов и их взаимодействие с электрическими полями нуклеи.
Два электронных интеграла с другой стороны описывают взаимодействие между электронными сообщениями.

Интуиция для того, что означают эти термины, можно получить от операторов создания и аннихилатион, составляющих каждый из них.
Например, $h _ {PQ} a ^ \ dagger_p a_q $ описывает электронную прыгающее» из счетчика Орбитал $q $ to Spin Орбитал $p $.
Аналогичным образом, термин $h _ {пкрс} a ^ \ dagger_p a ^ \ dagger_q a_r a_s $ (для различных $p, q, r, s $) описывает два электрона в обороте по орбитам $r $ и $s $ разбросанность друг от друга и завершается на обороте по орбите $p $ и $q $.
Если $r = q $ and $p = s $, $h _ {ПРРП} a ^ \ dagger_p a ^ \ dagger_r a_r a_p = h_ {ПРРП} n_p n_r $ обеспечивает снижение энергии, связанное с двумя электронными, которые находятся ближе друг к другу, но не описывает динамический процесс.

Мы можем представить такие Хамилтонианс с помощью класса `FermionHamiltonian`, который, по сути, является списком, содержащим все нужные экземпляры `FermionTerm`.
Поскольку Хамилтонианс являются Хермитиан по определению, мы индексируем термины, используя более специализированный тип `HermitianFermionTerm`, который также использует симметрию Хермитиан при проверке того, эквивалентны ли термины.

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
При добавлении терминов в Хамилтониан с помощью `Add`все нехермитианные термины, такие как `fermionTerm0`, считаются парными с Хермитиан сопряженными.
Таким образом, следующий фрагмент кода также представляет один и тот же Хамилтониан:
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the term to be added -- note the doubled coefficient.
    hamiltonian.Add(new HermitianFermionTerm(new[] { 1, 0 }), 2.0);
```

Используя правила защиты от коммутатион, некоторые экземпляры `FermionTerm` в Хамилтониан фактически соответствуют одной последовательности операторов фермионик, иногда до знака минус.
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

$ $ \бегин{алигн} H = \сум\_{PQ} h\_{PQ} a ^ \дагжер\_{p}\_{q} + \фрак{1}{2}\сум\_{пкрс} H\_{пкрс} a ^ \дагжер\_{p} a ^ \дагжер\_{q} а\_{r} a\_{s}.
\енд{алигн} $ $

В этой нотации существует не более $N коэффициентов: ^ 2 + N ^ 4 $.
Однако многие из этих коэффициентов можно собрать, так как они соответствуют одному оператору.
Например, если $p, q, r, s $ — это разные индексы. мы можем использовать правила защиты от коммутатион, чтобы отобразить следующее: $ $ a ^ \дагжер\_{p} a ^ \дагжер\_{q}\_{r}\_{s} =-a ^ \дагжер\_{q} a ^ \дагжер\_{p} a\_{r} a\_{s} =-a ^ \дагжер\_{p} a ^ \дагжер\_{q}\_{s},\_{r} = a ^ \дагжер\_{q} a ^ \дагжер\_{p}\_{s}\_{r}.
$$

Более того, так как $H $ является Хермитиан, каждый\_$h оператор Хермитиан фермионик {пкрс} a ^ \дагжер\_{p} а ^ \дагжер\_{q} a\_{r} a\_{s} $ имеет Хермитиан сопряженный, который также находится в $H $. Чтобы обеспечить уникальную индексацию групп терминов, характеризующих эти симметриес, мы определяем каноническое упорядочение по индексам $ (i\_1, \кдотс, i\_n, j\_1, \кдотс, j\_m) $ любой последовательности $n + m $ фермионик Operators $a ^ \дагжер\_{i\_1} \кдотс a ^ \дагжер\_{i\_n}\_{j\_1} \кдотс\_{j\_m} :
-   Все операторы создания $a ^ \дагжер\_{i\_\кдот} $ размещаются до всех операторов аннихилатион $a\_{j\_\кдот} $.
-   Все индексы операторов создания сортируются в возрастающем порядке, то есть $i\_1 < я\_2 < \кдотс < n $.\_
-   Все индексы операторов аннихилатион сортируются в убывающем порядке, то есть $j\_1 > j\_2 \кдотс > j\_m $.
-   Самый левый индекс меньше или равен правому индексу, то есть $i\_1 \ Le j\_m $.

Мы можем определить этот набор канонических упорядоченных индексов как $ $ \бегин{алигн} (i\_1, \кдотс, i\_n, j\_1, \кдотс, j\_m) \ин S\_{n, m}.
\енд{алигн} $ $

При таком каноническом упорядочении фермионик Хамилтониан может выражаться как $ $ \бегин{алигн} H = \сум\_{(p, q) \ин S\_{1,1}} H "\_{PQ} \фрак{а ^ \дагжер\_{p} a\_{q} + a ^ \дагжер\_{q} a\_{p}}{2}+ \сум\_{(p, q, r, s) \ин S\_{2,2}} H '\_{пкрс} \фрак{а ^ \dagger\_{p} a ^ \dagger\_{q} a\_{r} a\_{s} + a ^ \dagger\_{S} a ^ \ дагжер\_{r}\_{q} a\_{p}}{2}, \енд{алигн} $ $ с соответствующим адаптированным целыми и двусторонними $h "\_{PQ} $ и $h"\_{пкрс} $ соответственно ".

