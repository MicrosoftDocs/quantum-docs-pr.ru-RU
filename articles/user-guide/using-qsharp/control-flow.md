---
title: 'Поток управления в Q#'
description: Циклы, условные выражения и т. д.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: eca37202e5fe9b48dcfdec4eeb4ba6cafaac8723
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691091"
---
# <a name="control-flow-in-no-locq"></a><span data-ttu-id="31d00-103">Поток управления в Q#</span><span class="sxs-lookup"><span data-stu-id="31d00-103">Control flow in Q#</span></span>

<span data-ttu-id="31d00-104">Внутри операции или функции каждая инструкция выполняется по порядку, аналогично другим общим императивным классическим языкам.</span><span class="sxs-lookup"><span data-stu-id="31d00-104">Within an operation or function, each statement runs in order, similar to other common imperative classical languages.</span></span>
<span data-ttu-id="31d00-105">Однако поток управления можно изменить тремя разными способами:</span><span class="sxs-lookup"><span data-stu-id="31d00-105">However, you can modify the flow of control in three distinct ways:</span></span>

* <span data-ttu-id="31d00-106">`if` инструкции</span><span class="sxs-lookup"><span data-stu-id="31d00-106">`if` statements</span></span>
* <span data-ttu-id="31d00-107">`for` бираются</span><span class="sxs-lookup"><span data-stu-id="31d00-107">`for` loops</span></span>
* <span data-ttu-id="31d00-108">`repeat-until-success` бираются</span><span class="sxs-lookup"><span data-stu-id="31d00-108">`repeat-until-success` loops</span></span>
* <span data-ttu-id="31d00-109">лиц ( `apply-within` инструкции)</span><span class="sxs-lookup"><span data-stu-id="31d00-109">conjugations (`apply-within` statements)</span></span>

<span data-ttu-id="31d00-110">`if` `for` Конструкции потока управления и имеют привычный смысл для большинства классических языков программирования.</span><span class="sxs-lookup"><span data-stu-id="31d00-110">The `if` and `for` control flow constructs proceed in a familiar sense to most classical programming languages.</span></span> <span data-ttu-id="31d00-111">[`Repeat-until-success`](#repeat-until-success-loop) циклы и [лиц](#conjugations) обсуждаются далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="31d00-111">[`Repeat-until-success`](#repeat-until-success-loop) loops and [conjugations](#conjugations) are discussed later in this article.</span></span>

<span data-ttu-id="31d00-112">Важно `for` ! циклы и `if` инструкции можно использовать в операциях, для которых создаются [специализации](xref:microsoft.quantum.guide.operationsfunctions) автоматически.</span><span class="sxs-lookup"><span data-stu-id="31d00-112">Importantly, `for` loops and `if` statements can be used in operations for which [specializations](xref:microsoft.quantum.guide.operationsfunctions) are auto-generated.</span></span> <span data-ttu-id="31d00-113">В этом сценарии смежная часть `for` цикла обращается к направлению и принимает смежную часть каждой итерации.</span><span class="sxs-lookup"><span data-stu-id="31d00-113">In that scenario, the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="31d00-114">Это действие следует принципу "обувь-and-Socks": Если вы хотите отменить размещение по протоколу SOCKS, а затем обувь, необходимо отменить размещение обувь, а затем отменить последующую операцию по протоколу SOCKS.</span><span class="sxs-lookup"><span data-stu-id="31d00-114">This action follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span> 

## <a name="if-else-if-else"></a><span data-ttu-id="31d00-115">If, else — if, else</span><span class="sxs-lookup"><span data-stu-id="31d00-115">If, Else-if, Else</span></span>

<span data-ttu-id="31d00-116">`if`Инструкция поддерживает условную обработку.</span><span class="sxs-lookup"><span data-stu-id="31d00-116">The `if` statement supports conditional processing.</span></span>
<span data-ttu-id="31d00-117">Он состоит из ключевого слова `if` , логического выражения в круглых скобках и блока операторов (блок _then_ ).</span><span class="sxs-lookup"><span data-stu-id="31d00-117">It consists of the keyword `if`, a Boolean expression in parentheses, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="31d00-118">При необходимости может следовать любое количество других предложений else-if, каждое из которых состоит из ключевого слова `elif` , логического выражения в круглых скобках и блока операторов ( _Else-If_ ).</span><span class="sxs-lookup"><span data-stu-id="31d00-118">Optionally, any number of else-if clauses can follow, each of which consists of the keyword `elif`, a Boolean expression in parentheses, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="31d00-119">Наконец, оператор может при необходимости завершиться предложением else, которое состоит из ключевого слова, `else` за которым следует другой блок операторов (блок _else_ ).</span><span class="sxs-lookup"><span data-stu-id="31d00-119">Finally, the statement can optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="31d00-120">`if`Условие вычисляется, и, если оно равно *true* , выполняется блок *then* .</span><span class="sxs-lookup"><span data-stu-id="31d00-120">The `if` condition is evaluated, and if it is *true* , the *then* block is run.</span></span>
<span data-ttu-id="31d00-121">Если условие имеет *значение false* , то проверяется первое условие else-if; Если это так, то выполняется блок *Else-If* .</span><span class="sxs-lookup"><span data-stu-id="31d00-121">If the condition is *false* , then the first else-if condition is evaluated; if that is true, then the *else-if* block is run.</span></span>
<span data-ttu-id="31d00-122">В противном случае второй блок-If вычисляет, а затем третий и т. д. до тех пор, пока не будет обнаружено предложение с истинным условием или отсутствуют другие предложения Else-If.</span><span class="sxs-lookup"><span data-stu-id="31d00-122">Otherwise, the second else-if block evaluates, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="31d00-123">Если исходное условие *If* и все предложения Else-If имеют *значение false* , выполняется блок *else* , если он указан.</span><span class="sxs-lookup"><span data-stu-id="31d00-123">If the original *if* condition and all the else-if clauses evaluate to *false* , the *else* block is run, if provided.</span></span>

<span data-ttu-id="31d00-124">Обратите внимание, что любой блок выполняется в отдельной области.</span><span class="sxs-lookup"><span data-stu-id="31d00-124">Note that whichever block runs, it runs within its own scope.</span></span>
<span data-ttu-id="31d00-125">Привязки, сделанные внутри `if` `elif` блока, или, `else` не видны после завершения блока.</span><span class="sxs-lookup"><span data-stu-id="31d00-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after the block ends.</span></span>

<span data-ttu-id="31d00-126">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="31d00-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="31d00-127">or</span><span class="sxs-lookup"><span data-stu-id="31d00-127">or</span></span>
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a><span data-ttu-id="31d00-128">Цикл For</span><span class="sxs-lookup"><span data-stu-id="31d00-128">For loop</span></span>

<span data-ttu-id="31d00-129">`for`Инструкция поддерживает итерацию по диапазону целых чисел или массиву.</span><span class="sxs-lookup"><span data-stu-id="31d00-129">The `for` statement supports iteration over an integer range or an array.</span></span>
<span data-ttu-id="31d00-130">Оператор состоит из ключевого слова `for` , за которым следует символ или кортеж символов, ключевое слово `in` , а также выражение типа `Range` или массива, все в круглых скобках и блок инструкций.</span><span class="sxs-lookup"><span data-stu-id="31d00-130">The statement consists of the keyword `for`, followed by a symbol or symbol tuple, the keyword `in`, and an expression of type `Range` or array, all in parentheses, and a statement block.</span></span>

<span data-ttu-id="31d00-131">Блок операторов (тело цикла) выполняется повторно с определенным символом (переменной цикла), привязанным к каждому значению в диапазоне или массиве.</span><span class="sxs-lookup"><span data-stu-id="31d00-131">The statement block (the body of the loop) runs repeatedly, with the defined symbol (the loop variable) bound to each value in the range or array.</span></span>
<span data-ttu-id="31d00-132">Обратите внимание, что если выражение диапазона принимает пустой диапазон или массив, тело не выполняется вообще.</span><span class="sxs-lookup"><span data-stu-id="31d00-132">Note that if the range expression evaluates to an empty range or array, the body does not run at all.</span></span>
<span data-ttu-id="31d00-133">Выражение полностью вычисляется перед входом в цикл и не изменяется во время выполнения цикла.</span><span class="sxs-lookup"><span data-stu-id="31d00-133">The expression is fully evaluated before entering the loop, and does not change while the loop is running.</span></span>

<span data-ttu-id="31d00-134">Переменная цикла привязывается к каждому входу в тело цикла и не привязана к концу тела.</span><span class="sxs-lookup"><span data-stu-id="31d00-134">The loop variable is bound at each entrance to the loop body, and is unbound at the end of the body.</span></span>
<span data-ttu-id="31d00-135">Переменная цикла не привязана после завершения цикла for.</span><span class="sxs-lookup"><span data-stu-id="31d00-135">The loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="31d00-136">Привязка переменной цикла является неизменяемой и соответствует тем же правилам, что и другие привязки переменных.</span><span class="sxs-lookup"><span data-stu-id="31d00-136">The binding of the loop variable is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="31d00-137">В этих примерах `qubits` используется регистр Кубитс (т. е. типа `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="31d00-137">In these examples, `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

<span data-ttu-id="31d00-138">Обратите внимание, что в конце мы использовали бинарный оператор арифметического сдвига влево `<<<` .</span><span class="sxs-lookup"><span data-stu-id="31d00-138">Note that at the end, we utilized the arithmetic-shift-left binary operator, `<<<`.</span></span> <span data-ttu-id="31d00-139">Дополнительные сведения см. в разделе [числовые выражения](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span><span class="sxs-lookup"><span data-stu-id="31d00-139">For more information, see [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span></span>

## <a name="repeat-until-success-loop"></a><span data-ttu-id="31d00-140">Цикл "повторить" до "успешно"</span><span class="sxs-lookup"><span data-stu-id="31d00-140">Repeat-until-success loop</span></span>

<span data-ttu-id="31d00-141">Этот Q# язык позволяет классического потока управления зависеть от результатов измерения Кубитс.</span><span class="sxs-lookup"><span data-stu-id="31d00-141">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="31d00-142">Эта возможность, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить вычислительные затраты для реализации унитариес.</span><span class="sxs-lookup"><span data-stu-id="31d00-142">This capability, in turn, enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="31d00-143">Примерами таких шаблонов являются *повторение до успешного выполнения* (RUS) в Q# .</span><span class="sxs-lookup"><span data-stu-id="31d00-143">Examples of this are the *repeat-until-success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="31d00-144">Эти шаблоны RUS *представляют собой вероятностная программы с низкой* стоимостью в терминах простейших шлюзов. Стоимость полагается на фактическое выполнение и за несколько возможных ветвлений.</span><span class="sxs-lookup"><span data-stu-id="31d00-144">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates; the incurred cost depends on the actual run and the interleaving of the multiple possible branchings.</span></span>

<span data-ttu-id="31d00-145">Для упрощения шаблонов повторения до успешного завершения (RUS) Q# поддерживает конструкции</span><span class="sxs-lookup"><span data-stu-id="31d00-145">To facilitate repeat-until-success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="31d00-146">где `expression` — любое допустимое выражение, результатом вычисления которого является значение типа `Bool` .</span><span class="sxs-lookup"><span data-stu-id="31d00-146">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="31d00-147">Выполняется тело цикла, после чего вычисляется условие.</span><span class="sxs-lookup"><span data-stu-id="31d00-147">The loop body runs, and then the condition is evaluated.</span></span>
<span data-ttu-id="31d00-148">Если условие истинно, инструкция завершается; в противном случае запускается адресная привязка и инструкция запускается снова, начиная с тела цикла.</span><span class="sxs-lookup"><span data-stu-id="31d00-148">If the condition is true, then the statement is completed; otherwise, the fixup runs, and the statement runs again, starting with the loop body.</span></span>

<span data-ttu-id="31d00-149">Все три части цикла RUS (текст, тест и адресная привязка) обрабатываются как единая область *для каждого повторения* , поэтому символы, привязанные к телу, доступны как в тесте, так и в адресной привязке.</span><span class="sxs-lookup"><span data-stu-id="31d00-149">All three portions of an RUS loop (the body, the test, and the fixup) are treated as a single scope *for each repetition* , so symbols that are bound in the body are available in both the test and the fixup.</span></span>
<span data-ttu-id="31d00-150">Однако завершение выполнения адресной привязки завершает область действия инструкции, чтобы привязки символов, сделанные во время тела или исправления, были недоступны при последующих повторах.</span><span class="sxs-lookup"><span data-stu-id="31d00-150">However, completing the run of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="31d00-151">Кроме того, `fixup` оператор часто полезен, но не всегда нужен.</span><span class="sxs-lookup"><span data-stu-id="31d00-151">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="31d00-152">В случаях, когда это не требуется, конструкция</span><span class="sxs-lookup"><span data-stu-id="31d00-152">In cases that it is not needed, the construct</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression);
```

<span data-ttu-id="31d00-153">также является допустимым шаблоном RUS.</span><span class="sxs-lookup"><span data-stu-id="31d00-153">is also a valid RUS pattern.</span></span>

<span data-ttu-id="31d00-154">Дополнительные примеры и подробные сведения см. в разделе [примеры повторения до успешного выполнения](#repeat-until-success-examples) в этой статье.</span><span class="sxs-lookup"><span data-stu-id="31d00-154">For more examples and details, see [Repeat-until-success examples](#repeat-until-success-examples) in this article.</span></span>

> [!TIP]   
> <span data-ttu-id="31d00-155">Избегайте использования циклов повторения до успешного выполнения в функциях.</span><span class="sxs-lookup"><span data-stu-id="31d00-155">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="31d00-156">Используйте циклы *while* , чтобы обеспечить соответствующую функциональность внутри функций.</span><span class="sxs-lookup"><span data-stu-id="31d00-156">Use *while* loops to provide the corresponding functionality inside functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="31d00-157">Цикл While</span><span class="sxs-lookup"><span data-stu-id="31d00-157">While loop</span></span>

<span data-ttu-id="31d00-158">Шаблоны Repeat-Until-Success имеют очень много времени.</span><span class="sxs-lookup"><span data-stu-id="31d00-158">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="31d00-159">Они широко используются в определенных классах алгоритмов тактов, поэтому выделенная конструкция языка в Q# .</span><span class="sxs-lookup"><span data-stu-id="31d00-159">They are widely used in particular classes of quantum algorithms - hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="31d00-160">Однако циклы, которые нарушаются в зависимости от условия и длина выполнения, таким способом, неизвестны во время компиляции, обрабатываются с определенными осторожностью в среде выполнения такта.</span><span class="sxs-lookup"><span data-stu-id="31d00-160">However, loops that break based on a condition and whose run length is thus unknown at compile-time, are handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="31d00-161">Однако их использование в функциях не является проблемой, так как эти циклы содержат только код, который выполняется на обычном (не такте) оборудовании.</span><span class="sxs-lookup"><span data-stu-id="31d00-161">However, their use within functions is unproblematic since these loops only contain code that runs on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="31d00-162">Q#Таким образом, поддерживает использование циклов while только внутри функций.</span><span class="sxs-lookup"><span data-stu-id="31d00-162">Q#, therefore, supports to use of while loops within functions only.</span></span>
<span data-ttu-id="31d00-163">`while`Оператор состоит из ключевого слова `while` , логического выражения в круглых скобках и блока операторов.</span><span class="sxs-lookup"><span data-stu-id="31d00-163">A `while` statement consists of the keyword `while`, a Boolean expression in parentheses, and a statement block.</span></span>
<span data-ttu-id="31d00-164">Блок операторов (тело цикла) выполняется до тех пор, пока условие принимает значение `true` .</span><span class="sxs-lookup"><span data-stu-id="31d00-164">The statement block (the body of the loop) runs as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="conjugations"></a><span data-ttu-id="31d00-165">Лиц</span><span class="sxs-lookup"><span data-stu-id="31d00-165">Conjugations</span></span>

<span data-ttu-id="31d00-166">В отличие от классических битов освобождение памяти такта немного сложнее, так как в результате нежелательного сброса Кубитс может иметь нежелательные последствия для оставшихся вычислений, если Кубитс все еще запутанными.</span><span class="sxs-lookup"><span data-stu-id="31d00-166">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="31d00-167">Эти эффекты можно избежать, правильно выполнив вычисления перед освобождением памяти.</span><span class="sxs-lookup"><span data-stu-id="31d00-167">These effects can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="31d00-168">Общий шаблон в тактовых вычислениях, следовательно, является следующим:</span><span class="sxs-lookup"><span data-stu-id="31d00-168">A common pattern in quantum computing is hence the following:</span></span> 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

<span data-ttu-id="31d00-169">Q# поддерживает инструкцию конжугатион, которая реализует предыдущее преобразование.</span><span class="sxs-lookup"><span data-stu-id="31d00-169">Q# supports a conjugation statement that implements the preceding transformation.</span></span> <span data-ttu-id="31d00-170">С помощью этой инструкции операция `ApplyWith` может быть реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="31d00-170">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
<span data-ttu-id="31d00-171">Такая инструкция конжугатион будет полезна, если внешние и внутренние преобразования недоступны в качестве операций, но более удобны для описания блоком, состоящим из нескольких инструкций.</span><span class="sxs-lookup"><span data-stu-id="31d00-171">Such a conjugation statement becomes useful if the outer and inner transformations are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="31d00-172">Обратное преобразование для инструкций, определенных в блоке внутри блока, автоматически создается компилятором и запускается после завершения блока Apply.</span><span class="sxs-lookup"><span data-stu-id="31d00-172">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and run after the apply-block completes.</span></span>
<span data-ttu-id="31d00-173">Поскольку любые изменяемые переменные, используемые в качестве части блока in, не могут быть повторно привязаны в блоке применения, созданное преобразование гарантируется как прилегающие вычисления в блоке внутри блока.</span><span class="sxs-lookup"><span data-stu-id="31d00-173">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 

## <a name="return-statement"></a><span data-ttu-id="31d00-174">Оператор Return</span><span class="sxs-lookup"><span data-stu-id="31d00-174">Return Statement</span></span>

<span data-ttu-id="31d00-175">Оператор Return завершает выполнение операции или функции и возвращает значение вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="31d00-175">The return statement ends the run of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="31d00-176">Он состоит из ключевого слова `return` , за которым следует выражение соответствующего типа и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="31d00-176">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="31d00-177">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="31d00-177">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="31d00-178">or</span><span class="sxs-lookup"><span data-stu-id="31d00-178">or</span></span>
```qsharp
return (results, qubits);
```

* <span data-ttu-id="31d00-179">Вызываемый метод, возвращающий пустой кортеж, не `()` требует наличия оператора return.</span><span class="sxs-lookup"><span data-stu-id="31d00-179">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
* <span data-ttu-id="31d00-180">Чтобы указать ранний выход из операции или функции, используйте `return ();` .</span><span class="sxs-lookup"><span data-stu-id="31d00-180">To specify an early exit from the operation or function, use `return ();`.</span></span>
<span data-ttu-id="31d00-181">Для вызова, возвращающего любой другой тип, требуется завершающий оператор return.</span><span class="sxs-lookup"><span data-stu-id="31d00-181">Callables that return any other type require a final return statement.</span></span>
* <span data-ttu-id="31d00-182">В операции отсутствует максимальное число инструкций Return.</span><span class="sxs-lookup"><span data-stu-id="31d00-182">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="31d00-183">Компилятор может выдать предупреждение, если операторы следуют за оператором Return в блоке.</span><span class="sxs-lookup"><span data-stu-id="31d00-183">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

   
## <a name="fail-statement"></a><span data-ttu-id="31d00-184">Оператор Fail</span><span class="sxs-lookup"><span data-stu-id="31d00-184">Fail statement</span></span>

<span data-ttu-id="31d00-185">Оператор Fail завершает выполнение операции и возвращает вызывающему объекту значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="31d00-185">The fail statement ends the run of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="31d00-186">Он состоит из ключевого слова `fail` , за которым следует строка и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="31d00-186">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="31d00-187">Инструкция возвращает строку в классический драйвер в качестве сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="31d00-187">The statement returns the string to the classical driver as the error message.</span></span>

<span data-ttu-id="31d00-188">Количество инструкций Fail в операции не ограничено.</span><span class="sxs-lookup"><span data-stu-id="31d00-188">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="31d00-189">Компилятор может выдать предупреждение, если операторы следуют за оператором Fail в блоке.</span><span class="sxs-lookup"><span data-stu-id="31d00-189">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="31d00-190">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="31d00-190">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="31d00-191">или с помощью [интерполяции строк](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="31d00-191">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="31d00-192">Примеры повторения до успешного выполнения</span><span class="sxs-lookup"><span data-stu-id="31d00-192">Repeat-until-success examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="31d00-193">Шаблон RUS для однокубитного вращения по оси иррациональная</span><span class="sxs-lookup"><span data-stu-id="31d00-193">RUS pattern for single-qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="31d00-194">В типичном варианте использования Следующая Q# Операция реализует поворот вокруг иррациональная оси $ (I + 2i Z)/\скрт {5} $ в БЛОЧ Sphere.</span><span class="sxs-lookup"><span data-stu-id="31d00-194">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="31d00-195">В реализации используется известный шаблон RUS:</span><span class="sxs-lookup"><span data-stu-id="31d00-195">The implementation uses a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a><span data-ttu-id="31d00-196">RUS-цикл с изменяемой переменной в области видимости</span><span class="sxs-lookup"><span data-stu-id="31d00-196">RUS loop with a mutable variable in scope</span></span>

<span data-ttu-id="31d00-197">В этом примере показано использование изменяемой переменной, `finished` которая находится в области действия всего цикла повторения до и после цикла, которая инициализируется перед циклом и обновляется в шаге исправления.</span><span class="sxs-lookup"><span data-stu-id="31d00-197">This example shows the use of a mutable variable, `finished`, which is within the scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a><span data-ttu-id="31d00-198">RUS без `fixup`</span><span class="sxs-lookup"><span data-stu-id="31d00-198">RUS without `fixup`</span></span>

<span data-ttu-id="31d00-199">В этом примере показан цикл RUS без шага исправления.</span><span class="sxs-lookup"><span data-stu-id="31d00-199">This example shows an RUS loop without the fixup step.</span></span> <span data-ttu-id="31d00-200">Код представляет собой цепь вероятностная, которая реализует важный шлюз ротации $V _3 = (\болдоне + 2 i Z)/\скрт {5} $ с использованием `H` `T` шлюзов и.</span><span class="sxs-lookup"><span data-stu-id="31d00-200">The code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="31d00-201">Цикл завершается в среднем на $ \фрак {8} {5} $.</span><span class="sxs-lookup"><span data-stu-id="31d00-201">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="31d00-202">Дополнительные сведения см. в разделе [*Повтор-Until-Success: недетерминированная декомпозиция одного кубит унитариес*](https://arxiv.org/abs/1311.1074) (Паетзникк и своре, 2014).</span><span class="sxs-lookup"><span data-stu-id="31d00-202">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="31d00-203">RUS для подготовки состояния такта</span><span class="sxs-lookup"><span data-stu-id="31d00-203">RUS to prepare a quantum state</span></span>

<span data-ttu-id="31d00-204">Наконец, ниже приведен пример шаблона RUS для подготовки состояния такта $ \фрак {1} {\скрт {3} } \лефт (\скрт {2} \кет {0} + \кет {1} \ригхт) $, начиная с $ \кет{+} $ State.</span><span class="sxs-lookup"><span data-stu-id="31d00-204">Finally, here is an example of an RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>

<span data-ttu-id="31d00-205">В этой операции показаны следующие важные программные функции.</span><span class="sxs-lookup"><span data-stu-id="31d00-205">Notable programmatic features shown in this operation are:</span></span>

* <span data-ttu-id="31d00-206">Более сложная `fixup` часть цикла, включающая в себя операции обработки тактов.</span><span class="sxs-lookup"><span data-stu-id="31d00-206">A more complex `fixup` part of the loop, which involves quantum operations.</span></span> 
* <span data-ttu-id="31d00-207">Использование `AssertMeasurementProbability` инструкций для определения вероятности измерения состояния такта в некоторых указанных точках программы.</span><span class="sxs-lookup"><span data-stu-id="31d00-207">The use of `AssertMeasurementProbability` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>

<span data-ttu-id="31d00-208">Дополнительные сведения об [`AssertMeasurement`](xref:Microsoft.Quantum.Diagnostics.assertmeasurement) [`AssertMeasurementProbability`](xref:Microsoft.Quantum.Diagnostics.assertmeasurementprobability) операциях и см. в разделе [тестирование и отладка](xref:microsoft.quantum.guide.testingdebugging).</span><span class="sxs-lookup"><span data-stu-id="31d00-208">For more information about the [`AssertMeasurement`](xref:Microsoft.Quantum.Diagnostics.assertmeasurement) and [`AssertMeasurementProbability`](xref:Microsoft.Quantum.Diagnostics.assertmeasurementprobability) operations, see [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertMeasurementProbability(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="31d00-209">Дополнительные сведения см. [в разделе Пример модульного тестирования, предоставленный в стандартной библиотеке](https://github.com/microsoft/Quantum/blob/main/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="31d00-209">For more information, see [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/main/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

## <a name="next-steps"></a><span data-ttu-id="31d00-210">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="31d00-210">Next steps</span></span>

<span data-ttu-id="31d00-211">Сведения о [тестировании и отладке](xref:microsoft.quantum.guide.testingdebugging) в Q# .</span><span class="sxs-lookup"><span data-stu-id="31d00-211">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>
