---
title: 'Дальнейшие приемы-Q # | Документация Майкрософт'
description: 'Дальнейшие приемы-Q #'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.going-further
ms.openlocfilehash: 41713827a93d2cc97e198fa4ad377012c846cf8b
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036242"
---
# <a name="going-further"></a><span data-ttu-id="13002-103">Дальнейшие переходы</span><span class="sxs-lookup"><span data-stu-id="13002-103">Going Further</span></span> #

<span data-ttu-id="13002-104">Теперь, когда вы узнали, как написать интересные тактовые программы в Q #, в этом разделе вы узнаете о нескольких более сложных темах, которые должны быть полезны для пересылки.</span><span class="sxs-lookup"><span data-stu-id="13002-104">Now that you've seen how to write interesting quantum programs in Q#, this section goes further by introducing a few more advanced topics that should prove useful going forward.</span></span>


## <a name="generic-operations-and-functions"></a><span data-ttu-id="13002-105">Универсальные операции и функции</span><span class="sxs-lookup"><span data-stu-id="13002-105">Generic Operations and Functions</span></span> ##

> [!TIP]
> <span data-ttu-id="13002-106">В этом разделе предполагается, что основные знания [универсальных C#шаблонов в ](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics), [универсальных F# ](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/) [ C++ шаблонах, шаблонов](https://docs.microsoft.com/cpp/cpp/templates-cpp)и аналогичных подходов к метапрограммирование в других языках.</span><span class="sxs-lookup"><span data-stu-id="13002-106">This section assumes some basic familiarity with [generics in C#](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics), [generics in F#](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/), [C++ templates](https://docs.microsoft.com/cpp/cpp/templates-cpp), or similar approaches to metaprogramming in other languages.</span></span>

<span data-ttu-id="13002-107">Многие функции и операции, которые мы хотим определить, не сильно полагаются на типы входных данных, а только неявно используют их типы с помощью какой бы то ни было другой функции или операции.</span><span class="sxs-lookup"><span data-stu-id="13002-107">Many functions and operations that we might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="13002-108">Например, рассмотрим концепцию *Map* , общую для многих функциональных языков. При наличии функции $f (x) $ и коллекции значений $\{x_1, x_2, \дотс, x_n\}$, Map возвращает новую коллекцию $\{f (x_1), f (x_2), \дотс, f (x_n)\}$.</span><span class="sxs-lookup"><span data-stu-id="13002-108">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="13002-109">Чтобы реализовать это в Q #, мы можем воспользоваться преимуществами функций, которые являются первыми классами.</span><span class="sxs-lookup"><span data-stu-id="13002-109">To implement this in Q#, we can take advantage of that functions are first class.</span></span>
<span data-ttu-id="13002-110">Давайте запишем краткий пример `Map`, используя ★ в качестве заполнителя, пока мы выберем, какие типы нам нужны.</span><span class="sxs-lookup"><span data-stu-id="13002-110">Let's write out a quick example of `Map`, using ★ as a placeholder while we figure out what types we need.</span></span>

```qsharp
function Map(fn : (★ -> ★), values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="13002-111">Обратите внимание, что эта функция выглядит почти так же, независимо от фактических типов, которые мы заменяем.</span><span class="sxs-lookup"><span data-stu-id="13002-111">Note this function looks very much the same no matter what actual types we substitute in.</span></span>
<span data-ttu-id="13002-112">, Например, карту из целых чисел в пол, похожа на карту из чисел с плавающей запятой в строки:</span><span class="sxs-lookup"><span data-stu-id="13002-112">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="13002-113">В принципе, мы могли бы написать версию `Map` для каждой пары типов, которую мы столкнулись, но это порождает ряд трудностей.</span><span class="sxs-lookup"><span data-stu-id="13002-113">In principle, we could write a version of `Map` for every pair of types that we encounter, but this introduces a number of difficulties.</span></span>
<span data-ttu-id="13002-114">Например, если в `Map`обнаружена ошибка, необходимо убедиться, что исправление применяется единообразно во всех версиях `Map`.</span><span class="sxs-lookup"><span data-stu-id="13002-114">For instance, if we find a bug in `Map`, then we must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="13002-115">Более того, если мы создаем новый кортеж или определяемый пользователем тип, то теперь необходимо создать новый `Map` для перехода к новому типу.</span><span class="sxs-lookup"><span data-stu-id="13002-115">Moreover, if we construct a new tuple or UDT, then we must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="13002-116">Хотя это алгоритмизируемым для небольшого количества таких функций, так как мы соберем больше функций той же формы, что и `Map`, стоимость введения новых типов становится неоправданной в достаточно коротком порядке.</span><span class="sxs-lookup"><span data-stu-id="13002-116">While this is tractable for a small number of such functions, as we collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="13002-117">Однако большая часть этой сложности не дает компилятору сведения, необходимые для того, чтобы понять, как связаны разные версии `Map`.</span><span class="sxs-lookup"><span data-stu-id="13002-117">Much of this difficulty results, however, from that the we have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="13002-118">Фактически мы хотим, чтобы компилятор обрабатывал `Map` как математические функции в Q # *types* to q # functions.</span><span class="sxs-lookup"><span data-stu-id="13002-118">Effectively, we want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>
<span data-ttu-id="13002-119">Это понятие формально позволяет функциям и операциям иметь *Параметры типа*, а также их обычные параметры кортежа.</span><span class="sxs-lookup"><span data-stu-id="13002-119">This notion is formalized by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="13002-120">В приведенных выше примерах мы хотели бы представить `Map` как имеющие параметры типа `Int, Pauli` в первом случае и `Double, String` во втором случае.</span><span class="sxs-lookup"><span data-stu-id="13002-120">In the examples above, we wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="13002-121">В большинстве случаев эти параметры типа можно использовать, как будто они являются обычными типами: мы используем значения параметров типа для создания массивов и кортежей, вызова функций и операций и присваивания обычным или изменяемым переменным.</span><span class="sxs-lookup"><span data-stu-id="13002-121">For the most part, these type parameters can then be used as though they were ordinary types: we use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="13002-122">Самый крайний случай косвенной зависимости заключается в том, что Кубитс, где программа Q # не может напрямую полагаться на структуру типа `Qubit`, но **должна** передавать подобные типы другим операциям и функциям.</span><span class="sxs-lookup"><span data-stu-id="13002-122">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type, but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="13002-123">Вернувшись к приведенному выше примеру, можно увидеть, что нам нужно `Map` иметь параметры типа, один для представления входных данных для `fn` и один для представления выходных данных `fn`.</span><span class="sxs-lookup"><span data-stu-id="13002-123">Returning to the example above, then, we can see that we need `Map` to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="13002-124">В Q # это написано путем добавления угловых скобок (`<>`, а не Бракетс $ \бракет{}$!) после имени функции или операции в ее объявлении, а также путем перечисления каждого параметра типа.</span><span class="sxs-lookup"><span data-stu-id="13002-124">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="13002-125">Имя каждого параметра типа должно начинаться с деления `'`, что означает, что это параметр типа, а не обычный тип (также известен как *конкретный* тип).</span><span class="sxs-lookup"><span data-stu-id="13002-125">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="13002-126">Для `Map`мы пишем следующее:</span><span class="sxs-lookup"><span data-stu-id="13002-126">For `Map`, we thus write:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="13002-127">Обратите внимание, что определение `Map<'Input, 'Output>` очень похоже на версии, которые мы написали ранее.</span><span class="sxs-lookup"><span data-stu-id="13002-127">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the versions we wrote out before.</span></span>
<span data-ttu-id="13002-128">Единственное различие заключается в том, что мы явно осведомлены о том, что компилятор, `Map`, напрямую не зависит от того, какие `'Input` и `'Output`, но работает для любых двух типов, используя их косвенно через `fn`.</span><span class="sxs-lookup"><span data-stu-id="13002-128">The only difference is that we have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="13002-129">Определив `Map<'Input, 'Output>` таким образом, можно вызвать его, как будто это обычная функция:</span><span class="sxs-lookup"><span data-stu-id="13002-129">Once we have defined `Map<'Input, 'Output>` in this way, we can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="13002-130">Написание универсальных функций и операций — это одно из мест, где «кортеж-в кортеже» — очень полезный способ подумать о функциях и операциях Q #.</span><span class="sxs-lookup"><span data-stu-id="13002-130">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="13002-131">Поскольку каждая функция принимает ровно один вход и возвращает ровно один выход, входные данные типа `'T -> 'U` совпадают с *любыми* функциями Q #.</span><span class="sxs-lookup"><span data-stu-id="13002-131">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="13002-132">Аналогичным образом любая операция может быть передана в вход типа `'T => 'U`.</span><span class="sxs-lookup"><span data-stu-id="13002-132">Similarly, any operation can be passed to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="13002-133">Во втором примере рассмотрим задачу написания функции, возвращающей композицию двух других функций:</span><span class="sxs-lookup"><span data-stu-id="13002-133">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="13002-134">Здесь необходимо указать, что именно `A`, `B`и `C`, и, следовательно, существенно ограничивает служебную программу нашей новой функции `Compose`.</span><span class="sxs-lookup"><span data-stu-id="13002-134">Here, we must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="13002-135">В конце концов, `Compose` зависит только от `A`, `B`и `C` *через* `innerFn` и `outerFn`.</span><span class="sxs-lookup"><span data-stu-id="13002-135">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="13002-136">В качестве альтернативы можно добавить параметры типа к `Compose`, которые указывают, что он работает для *любого* `A`, `B`и `C`, пока эти параметры соответствуют ожидаемым `innerFn` и `outerFn`:</span><span class="sxs-lookup"><span data-stu-id="13002-136">As an alternative, then, we can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="13002-137">Стандартные библиотеки Q # предоставляют ряд таких операций и функций с параметрами, которые позволяют более быстро выражать поток управления с более высоким порядком.</span><span class="sxs-lookup"><span data-stu-id="13002-137">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="13002-138">Они описаны далее в статье [рекомендации по стандартной библиотеке Q #](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="13002-138">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>

## <a name="borrowing-qubits"></a><span data-ttu-id="13002-139">Заимствование Кубитс</span><span class="sxs-lookup"><span data-stu-id="13002-139">Borrowing Qubits</span></span> ##

<span data-ttu-id="13002-140">Механизм заимствования займов позволяет выделить Кубитс, который можно использовать в качестве вспомогательного пространства во время вычисления.</span><span class="sxs-lookup"><span data-stu-id="13002-140">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span> <span data-ttu-id="13002-141">Обычно эти Кубитс не находятся в чистом состоянии, т. е. они не обязательно инициализируются в известном состоянии, например $ \кет{0}$.</span><span class="sxs-lookup"><span data-stu-id="13002-141">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span> <span data-ttu-id="13002-142">Одна из них также говорит о «грязном» Кубитс, так как их состояние неизвестно и даже может быть запутанными с другими частями памяти компьютера-такта.</span><span class="sxs-lookup"><span data-stu-id="13002-142">One also speaks of "dirty" qubits as their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span> <span data-ttu-id="13002-143">Между известными случаями использования «грязных» Кубитс являются реализации многофункциональных кнот шлюзов, требующие лишь очень мало Кубитс и реализации инкрементов.</span><span class="sxs-lookup"><span data-stu-id="13002-143">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>

<span data-ttu-id="13002-144">В Canon есть примеры, в которых используется ключевое слово `borrowing`, например функция, `MultiControlledXBorrow` определена ниже.</span><span class="sxs-lookup"><span data-stu-id="13002-144">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="13002-145">Если `controls` обозначает элемент управления Кубитс, который должен быть добавлен в операцию `X`, то в этой реализации будет добавлена общая `Length(controls)-2` много грязных анЦиллас.</span><span class="sxs-lookup"><span data-stu-id="13002-145">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

<span data-ttu-id="13002-146">Обратите внимание, что широкое использование `With` объединения---в своей форме, которое применимо для операций, поддерживающих смежные элементы, т. е. `WithA`---был сделан в этом примере, что является хорошим стилем программирования, так как добавление элемента управления для структур, включающих `With`, только передает управление во внутреннюю операцию.</span><span class="sxs-lookup"><span data-stu-id="13002-146">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example which is good programming style as adding control to structures involving `With` only propagates control to the inner operation.</span></span> <span data-ttu-id="13002-147">Обратите внимание, что в дополнение к `body`у операции была явно предоставлена реализация `controlled` тела операции, а не инструкция `controlled auto`.</span><span class="sxs-lookup"><span data-stu-id="13002-147">Further note that here in addition to the `body` of the operation an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span> <span data-ttu-id="13002-148">Причина в том, что мы понимаем, что из структуры канала можно легко добавить дополнительные элементы управления, которые полезны по сравнению с добавлением элемента управления в каждый отдельный шлюз в `body`.</span><span class="sxs-lookup"><span data-stu-id="13002-148">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="13002-149">Рекомендуется сравнить этот код с другой функцией Canon `MultiControlledXClean`, которая дает ту же цель реализации операции `X`, управляемой операцией умножения, но которая использует несколько чистых Кубитс с помощью механизма `using`.</span><span class="sxs-lookup"><span data-stu-id="13002-149">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 
