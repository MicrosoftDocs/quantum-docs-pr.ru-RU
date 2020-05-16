---
title: 'Переменные в Q #'
description: Описание заливки
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 407b4ff3570816eb7bdc323a5c5b77dac2d951af
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430906"
---
# <a name="variables-in-q"></a><span data-ttu-id="f9b35-103">Переменные в Q #</span><span class="sxs-lookup"><span data-stu-id="f9b35-103">Variables in Q#</span></span>

<span data-ttu-id="f9b35-104">В Q # различаются изменяемые и неизменяемые символы, а также "переменные", которые связаны с выражениями или назначаются им.</span><span class="sxs-lookup"><span data-stu-id="f9b35-104">Q# distinguishes between mutable and immutable symbols, or "variables", which are bound/assigned to expressions.</span></span>
<span data-ttu-id="f9b35-105">Как правило, использование неизменяемых символов рекомендуется, поскольку оно позволяет компилятору выполнять более оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="f9b35-105">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="f9b35-106">Левая часть привязки состоит из кортежа символов, а также с правой стороны выражения.</span><span class="sxs-lookup"><span data-stu-id="f9b35-106">The left-hand-side of a binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

## <a name="immutable-variables"></a><span data-ttu-id="f9b35-107">Неизменяемые переменные</span><span class="sxs-lookup"><span data-stu-id="f9b35-107">Immutable Variables</span></span>

<span data-ttu-id="f9b35-108">Значение любого типа в Q # можно присвоить переменной для повторного использования в операции или функции с помощью `let` ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="f9b35-108">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>

<span data-ttu-id="f9b35-109">Неизменяемая Привязка состоит из ключевого слова `let` , за которым следует символ или кортеж символов, знак равенства `=` , выражение для привязки символов к и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="f9b35-109">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="f9b35-110">например</span><span class="sxs-lookup"><span data-stu-id="f9b35-110">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="f9b35-111">Это назначает определенный массив операторов Паули имени переменной (или символу) `measurementOperator` .</span><span class="sxs-lookup"><span data-stu-id="f9b35-111">This assigns a particular array of Pauli operators to the variable name (or "symbol"), `measurementOperator`.</span></span>

> [!NOTE]
> <span data-ttu-id="f9b35-112">Нам не нужно явно указывать тип нашей новой переменной, так как выражение в правой части `let` оператора является неоднозначным и тип выводится компилятором.</span><span class="sxs-lookup"><span data-stu-id="f9b35-112">We did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="f9b35-113">Переменные, определенные с помощью, `let` являются *неизменяемыми*. Это означает, что после определения она больше не может быть изменена каким бы то ни было.</span><span class="sxs-lookup"><span data-stu-id="f9b35-113">Variables defined using `let` are *immutable*, meaning that once it has been defined, it can no longer be changed in any way.</span></span>
<span data-ttu-id="f9b35-114">Это обеспечивает несколько выгодных оптимизаций, включая оптимизацию классической логики, действующей на переменные, для изменения порядка применения `Adjoint` варианта операции.</span><span class="sxs-lookup"><span data-stu-id="f9b35-114">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

## <a name="mutable-variables"></a><span data-ttu-id="f9b35-115">Изменяемые переменные</span><span class="sxs-lookup"><span data-stu-id="f9b35-115">Mutable Variables</span></span>

<span data-ttu-id="f9b35-116">В качестве альтернативы созданию переменной с помощью `let` `mutable` ключевого слова будет создана изменяемая переменная, которая *может* быть повторно привязана после первоначального создания с использованием `set` ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="f9b35-116">As an alternative to creating a variable with `let`, the `mutable` keyword will create a mutable variable that *can* be re-bound after it is initially created by using the `set` keyword.</span></span>

<span data-ttu-id="f9b35-117">Символы, объявленные и привязанные как часть `mutable` инструкции, могут быть повторно привязаны к другому значению позже в коде.</span><span class="sxs-lookup"><span data-stu-id="f9b35-117">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> <span data-ttu-id="f9b35-118">Если символ повторно привязан позже в коде, его тип не изменится, а вновь привязанное значение должно быть совместимо с этим типом.</span><span class="sxs-lookup"><span data-stu-id="f9b35-118">If a symbol is rebound later in the code, its type does not change, and the newly bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="f9b35-119">Повторная привязка изменяемых символов</span><span class="sxs-lookup"><span data-stu-id="f9b35-119">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="f9b35-120">Изменяемую переменную можно повторно привязать с помощью `set` инструкции.</span><span class="sxs-lookup"><span data-stu-id="f9b35-120">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="f9b35-121">Такая повторная привязка состоит из ключевого слова `set` , за которым следует символ или кортеж символов, знак равенства `=` , выражение для повторной привязки символов к и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="f9b35-121">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="f9b35-122">Ниже приведены некоторые возможные примеры методов повторной привязки.</span><span class="sxs-lookup"><span data-stu-id="f9b35-122">Here, we provide some possible examples of rebinding statement techniques</span></span>

### <a name="apply-and-reassign-statements"></a><span data-ttu-id="f9b35-123">Операторы применения и повторного назначения</span><span class="sxs-lookup"><span data-stu-id="f9b35-123">Apply-and-Reassign Statements</span></span>

<span data-ttu-id="f9b35-124">Определенный тип оператора, `set` который мы называем оператором *Apply-and-reassignя* , предоставляет удобный способ объединения, если правая часть состоит из приложения бинарного оператора, и результат должен быть повторно привязан к оператору в левом аргументе.</span><span class="sxs-lookup"><span data-stu-id="f9b35-124">A particular kind of `set`-statement we refer to as an *apply-and-reassign* statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="f9b35-125">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="f9b35-125">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="f9b35-126">увеличивает значение счетчика `counter` в каждой итерации `for` цикла.</span><span class="sxs-lookup"><span data-stu-id="f9b35-126">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="f9b35-127">Приведенный выше код эквивалентен</span><span class="sxs-lookup"><span data-stu-id="f9b35-127">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

<span data-ttu-id="f9b35-128">Аналогичные операторы доступны для всех бинарных операторов, в которых тип левой стороны соответствует типу выражения.</span><span class="sxs-lookup"><span data-stu-id="f9b35-128">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="f9b35-129">Это предоставляет пример удобного способа накопления значений.</span><span class="sxs-lookup"><span data-stu-id="f9b35-129">This provides for example a convenient way to accumulate values.</span></span>

<span data-ttu-id="f9b35-130">Например, допустим `qubits` является регситером Кубитс:</span><span class="sxs-lookup"><span data-stu-id="f9b35-130">For example, supposing `qubits` is a regsiter of qubits:</span></span>
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a><span data-ttu-id="f9b35-131">Операторы обновления и повторного назначения</span><span class="sxs-lookup"><span data-stu-id="f9b35-131">Update-and-Reassign Statements</span></span>

<span data-ttu-id="f9b35-132">Аналогичное объединение существует для [выражений копирования и обновления](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) в правой части.</span><span class="sxs-lookup"><span data-stu-id="f9b35-132">A similar concatenation exists for [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) on the right-hand-side.</span></span>
<span data-ttu-id="f9b35-133">Соответственно, операторы *Update и reassignя* существуют для *именованных элементов* в определяемых пользователем типах, а также для *элементов массива*.</span><span class="sxs-lookup"><span data-stu-id="f9b35-133">Correspondingly, *update-and-reassign* statements exist for *named items* in user-defined types as well as for *array items*.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="f9b35-134">В случае массивов [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) в стандартных библиотеках предоставляются необходимые средства для многих общих задач инициализации массива и управления ими, что позволяет избежать необходимости обновлять элементы массива в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="f9b35-134">In the case of arrays, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) in our standard libraries provides the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> 

<span data-ttu-id="f9b35-135">Инструкции обновления и повторного назначения предоставляют альтернативный вариант при необходимости:</span><span class="sxs-lookup"><span data-stu-id="f9b35-135">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

<span data-ttu-id="f9b35-136">Используя средства библиотеки для массивов, предоставляемых [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) , мы можем, например, легко определить функцию, возвращающую массив пола, где Паули по индексу `i` принимает заданное значение, а все остальные записи являются идентификатором.</span><span class="sxs-lookup"><span data-stu-id="f9b35-136">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can, for example, easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity.</span></span>

<span data-ttu-id="f9b35-137">Ниже приведены два определения такой функции, второй из которых использует средства в нашем выбытии.</span><span class="sxs-lookup"><span data-stu-id="f9b35-137">Here are two definitions of such a function, with the second taking advantage of the tools at our disposal.</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli or PauliI dep. on whether index==location
    }    
    return pauliArray;
}
```

<span data-ttu-id="f9b35-138">Вместо перебора по каждому индексу в массиве и условного присвоения ему значения `PauliI` или `Pauli` , мы можем использовать `ConstantArray` FROM [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) для создания массива `PauliI` , а затем просто возвращая выражение копирования и обновления, в котором мы изменили значение спеЦифк в индексе `location` :</span><span class="sxs-lookup"><span data-stu-id="f9b35-138">Instead of iterating over each index in the array, and conditionally setting it to `PauliI` or `Pauli`, we can instead use `ConstantArray` from [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) to create an array of `PauliI`'s, and then simply returning a copy-and-update expression in which we've changed the specifc value at index `location`:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a><span data-ttu-id="f9b35-139">Деконструкция кортежа</span><span class="sxs-lookup"><span data-stu-id="f9b35-139">Tuple Deconstruction</span></span>

<span data-ttu-id="f9b35-140">Помимо присвоения одной переменной, `let` `mutable` Ключевые слова и---или на самом деле любые другие конструкции привязки, например `set` (описанные ниже)---также позволяют распаковать содержимое [типа кортежа](xref:microsoft.quantum.guide.types#tuple-types).</span><span class="sxs-lookup"><span data-stu-id="f9b35-140">In addition to assigning a single variable, the `let` and `mutable` keywords---or in fact any other binding construct, such as `set` (described below)---also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.guide.types#tuple-types).</span></span>
<span data-ttu-id="f9b35-141">Назначение этой формы называется *деконструированием* элементов этого кортежа.</span><span class="sxs-lookup"><span data-stu-id="f9b35-141">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>

<span data-ttu-id="f9b35-142">Если правая часть привязки является кортежем, то этот кортеж можно деконструировать после назначения.</span><span class="sxs-lookup"><span data-stu-id="f9b35-142">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="f9b35-143">Такие деконструкции могут содержать вложенные кортежи, а любая полная или частичная деконструкция является допустимой, если форма кортежа в правой части совместима с формой кортежа символов.</span><span class="sxs-lookup"><span data-stu-id="f9b35-143">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>

<span data-ttu-id="f9b35-144">Пример:</span><span class="sxs-lookup"><span data-stu-id="f9b35-144">For example:</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a><span data-ttu-id="f9b35-145">Области привязки</span><span class="sxs-lookup"><span data-stu-id="f9b35-145">Binding Scopes</span></span>

<span data-ttu-id="f9b35-146">Как правило, привязки к символам выходят за пределы области действия и становятся неработоспособными в конце блока операторов, в котором они встречаются.</span><span class="sxs-lookup"><span data-stu-id="f9b35-146">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="f9b35-147">Существует два исключения из этого правила:</span><span class="sxs-lookup"><span data-stu-id="f9b35-147">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="f9b35-148">Привязка переменной цикла `for` цикла находится в области видимости тела цикла for, но не после конца цикла.</span><span class="sxs-lookup"><span data-stu-id="f9b35-148">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="f9b35-149">Все три части `repeat` / `until` цикла (текст, тест и адресная привязка) обрабатываются как одна область, поэтому символы, привязанные к тексту, доступны в тесте и в адресной привязке.</span><span class="sxs-lookup"><span data-stu-id="f9b35-149">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="f9b35-150">Для обоих типов циклов каждый проход по циклу выполняется в своей собственной области, поэтому привязки из предыдущего прохода не будут доступны на более позднем этапе.</span><span class="sxs-lookup"><span data-stu-id="f9b35-150">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>
<span data-ttu-id="f9b35-151">Подробные сведения об этих циклах можно найти в [потоке управления](xref:microsoft.quantum.guide.controlflow).</span><span class="sxs-lookup"><span data-stu-id="f9b35-151">Details on these loops can be found at [Control Flow](xref:microsoft.quantum.guide.controlflow).</span></span>

<span data-ttu-id="f9b35-152">Привязки символов из внешних блоков наследуются внутренними блоками.</span><span class="sxs-lookup"><span data-stu-id="f9b35-152">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="f9b35-153">Символ может быть привязан только один раз для каждого блока; нельзя определить символ с тем же именем, что и у другого символа, находящихся в пределах области (без "тени").</span><span class="sxs-lookup"><span data-stu-id="f9b35-153">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="f9b35-154">Следующие последовательности будут допустимыми:</span><span class="sxs-lookup"><span data-stu-id="f9b35-154">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="f9b35-155">и</span><span class="sxs-lookup"><span data-stu-id="f9b35-155">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

<span data-ttu-id="f9b35-156">Но это недопустимо:</span><span class="sxs-lookup"><span data-stu-id="f9b35-156">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="f9b35-157">как:</span><span class="sxs-lookup"><span data-stu-id="f9b35-157">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="whats-next"></a><span data-ttu-id="f9b35-158">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="f9b35-158">What's Next?</span></span>
<span data-ttu-id="f9b35-159">Дополнительные сведения о [работе с Кубитс](xref:microsoft.quantum.guide.qubits) в Q #.</span><span class="sxs-lookup"><span data-stu-id="f9b35-159">Learn about [Working With Qubits](xref:microsoft.quantum.guide.qubits) in Q#.</span></span>