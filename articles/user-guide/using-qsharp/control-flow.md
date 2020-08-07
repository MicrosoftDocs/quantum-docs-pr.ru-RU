---
title: Поток управления вQ#
description: Циклы, условные выражения и т. д.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
no-loc:
- Q#
- $$v
ms.openlocfilehash: fc619d64bfebfc27d7feac6dafb2dd4cf22825d6
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867953"
---
# <a name="control-flow-in-no-locq"></a><span data-ttu-id="5b085-103">Поток управления вQ#</span><span class="sxs-lookup"><span data-stu-id="5b085-103">Control flow in Q#</span></span>

<span data-ttu-id="5b085-104">Внутри операции или функции каждая инструкция выполняется по порядку, аналогично другим общим императивным классическим языкам.</span><span class="sxs-lookup"><span data-stu-id="5b085-104">Within an operation or function, each statement runs in order, similar to other common imperative classical languages.</span></span>
<span data-ttu-id="5b085-105">Однако поток управления можно изменить тремя разными способами:</span><span class="sxs-lookup"><span data-stu-id="5b085-105">However, you can modify the flow of control in three distinct ways:</span></span>

* <span data-ttu-id="5b085-106">`if`инструкции</span><span class="sxs-lookup"><span data-stu-id="5b085-106">`if` statements</span></span>
* <span data-ttu-id="5b085-107">`for`бираются</span><span class="sxs-lookup"><span data-stu-id="5b085-107">`for` loops</span></span>
* <span data-ttu-id="5b085-108">`repeat-until-success`бираются</span><span class="sxs-lookup"><span data-stu-id="5b085-108">`repeat-until-success` loops</span></span>

<span data-ttu-id="5b085-109">`if` `for` Конструкции потока управления и имеют привычный смысл для большинства классических языков программирования.</span><span class="sxs-lookup"><span data-stu-id="5b085-109">The `if` and `for` control flow constructs proceed in a familiar sense to most classical programming languages.</span></span> <span data-ttu-id="5b085-110">[`Repeat-until-success`](#repeat-until-success-loop)циклы обсуждаются далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="5b085-110">[`Repeat-until-success`](#repeat-until-success-loop) loops are discussed later in this article.</span></span>

<span data-ttu-id="5b085-111">Важно `for` ! циклы и `if` инструкции можно использовать в операциях, для которых создаются [специализации](xref:microsoft.quantum.guide.operationsfunctions) автоматически.</span><span class="sxs-lookup"><span data-stu-id="5b085-111">Importantly, `for` loops and `if` statements can be used in operations for which [specializations](xref:microsoft.quantum.guide.operationsfunctions) are auto-generated.</span></span> <span data-ttu-id="5b085-112">В этом сценарии смежная часть `for` цикла обращается к направлению и принимает смежную часть каждой итерации.</span><span class="sxs-lookup"><span data-stu-id="5b085-112">In that scenario, the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="5b085-113">Это действие следует принципу "обувь-and-Socks": Если вы хотите отменить размещение по протоколу SOCKS, а затем обувь, необходимо отменить размещение обувь, а затем отменить последующую операцию по протоколу SOCKS.</span><span class="sxs-lookup"><span data-stu-id="5b085-113">This action follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span> 

## <a name="if-else-if-else"></a><span data-ttu-id="5b085-114">If, else — if, else</span><span class="sxs-lookup"><span data-stu-id="5b085-114">If, Else-if, Else</span></span>

<span data-ttu-id="5b085-115">`if`Оператор поддерживает условное выполнение.</span><span class="sxs-lookup"><span data-stu-id="5b085-115">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="5b085-116">Он состоит из ключевого слова `if` , логического выражения в круглых скобках и блока операторов (блок _then_ ).</span><span class="sxs-lookup"><span data-stu-id="5b085-116">It consists of the keyword `if`, a Boolean expression in parentheses, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="5b085-117">При необходимости может следовать любое количество других предложений else-if, каждое из которых состоит из ключевого слова `elif` , логического выражения в круглых скобках и блока операторов ( _Else-If_ ).</span><span class="sxs-lookup"><span data-stu-id="5b085-117">Optionally, any number of else-if clauses can follow, each of which consists of the keyword `elif`, a Boolean expression in parentheses, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="5b085-118">Наконец, оператор может при необходимости завершиться предложением else, которое состоит из ключевого слова, `else` за которым следует другой блок операторов (блок _else_ ).</span><span class="sxs-lookup"><span data-stu-id="5b085-118">Finally, the statement can optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="5b085-119">`if`Условие вычисляется, и, если оно равно *true*, выполняется блок *then* .</span><span class="sxs-lookup"><span data-stu-id="5b085-119">The `if` condition is evaluated, and if it is *true*, the *then* block is run.</span></span>
<span data-ttu-id="5b085-120">Если условие имеет *значение false*, то проверяется первое условие else-if; Если это так, то выполняется блок *Else-If* .</span><span class="sxs-lookup"><span data-stu-id="5b085-120">If the condition is *false*, then the first else-if condition is evaluated; if that is true, then the *else-if* block is run.</span></span>
<span data-ttu-id="5b085-121">В противном случае второй блок-If вычисляет, а затем третий и т. д. до тех пор, пока не будет обнаружено предложение с истинным условием или отсутствуют другие предложения Else-If.</span><span class="sxs-lookup"><span data-stu-id="5b085-121">Otherwise, the second else-if block evaluates, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="5b085-122">Если исходное условие *If* и все предложения Else-If имеют *значение false*, выполняется блок *else* , если он указан.</span><span class="sxs-lookup"><span data-stu-id="5b085-122">If the original *if* condition and all the else-if clauses evaluate to *false*, the *else* block is run, if provided.</span></span>

<span data-ttu-id="5b085-123">Обратите внимание, что любой блок выполняется в отдельной области.</span><span class="sxs-lookup"><span data-stu-id="5b085-123">Note that whichever block runs, it runs within its own scope.</span></span>
<span data-ttu-id="5b085-124">Привязки, сделанные внутри `if` `elif` блока, или, `else` не видны после завершения блока.</span><span class="sxs-lookup"><span data-stu-id="5b085-124">Bindings made inside of an `if`, `elif`, or `else` block are not visible after the block ends.</span></span>

<span data-ttu-id="5b085-125">например следующие.</span><span class="sxs-lookup"><span data-stu-id="5b085-125">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="5b085-126">or</span><span class="sxs-lookup"><span data-stu-id="5b085-126">or</span></span>
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

## <a name="for-loop"></a><span data-ttu-id="5b085-127">Цикл For</span><span class="sxs-lookup"><span data-stu-id="5b085-127">For loop</span></span>

<span data-ttu-id="5b085-128">`for`Инструкция поддерживает итерацию по диапазону целых чисел или массиву.</span><span class="sxs-lookup"><span data-stu-id="5b085-128">The `for` statement supports iteration over an integer range or an array.</span></span>
<span data-ttu-id="5b085-129">Оператор состоит из ключевого слова `for` , за которым следует символ или кортеж символов, ключевое слово `in` , а также выражение типа `Range` или массива, все в круглых скобках и блок инструкций.</span><span class="sxs-lookup"><span data-stu-id="5b085-129">The statement consists of the keyword `for`, followed by a symbol or symbol tuple, the keyword `in`, and an expression of type `Range` or array, all in parentheses, and a statement block.</span></span>

<span data-ttu-id="5b085-130">Блок операторов (тело цикла) выполняется повторно с определенным символом (переменной цикла), привязанным к каждому значению в диапазоне или массиве.</span><span class="sxs-lookup"><span data-stu-id="5b085-130">The statement block (the body of the loop) runs repeatedly, with the defined symbol (the loop variable) bound to each value in the range or array.</span></span>
<span data-ttu-id="5b085-131">Обратите внимание, что если выражение диапазона принимает пустой диапазон или массив, тело не выполняется вообще.</span><span class="sxs-lookup"><span data-stu-id="5b085-131">Note that if the range expression evaluates to an empty range or array, the body does not run at all.</span></span>
<span data-ttu-id="5b085-132">Выражение полностью вычисляется перед входом в цикл и не изменяется во время выполнения цикла.</span><span class="sxs-lookup"><span data-stu-id="5b085-132">The expression is fully evaluated before entering the loop, and does not change while the loop is executing.</span></span>

<span data-ttu-id="5b085-133">Переменная цикла привязывается к каждому входу в тело цикла и не привязана к концу тела.</span><span class="sxs-lookup"><span data-stu-id="5b085-133">The loop variable is bound at each entrance to the loop body, and is unbound at the end of the body.</span></span>
<span data-ttu-id="5b085-134">Переменная цикла не привязана после завершения цикла for.</span><span class="sxs-lookup"><span data-stu-id="5b085-134">The loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="5b085-135">Привязка переменной цикла является неизменяемой и соответствует тем же правилам, что и другие привязки переменных.</span><span class="sxs-lookup"><span data-stu-id="5b085-135">The binding of the loop variable is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="5b085-136">В этих примерах `qubits` используется регистр Кубитс (т. е. типа `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="5b085-136">In these examples, `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

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

<span data-ttu-id="5b085-137">Обратите внимание, что в конце мы использовали бинарный оператор арифметического сдвига влево `<<<` .</span><span class="sxs-lookup"><span data-stu-id="5b085-137">Note that at the end, we utilized the arithmetic-shift-left binary operator, `<<<`.</span></span> <span data-ttu-id="5b085-138">Дополнительные сведения см. в разделе [числовые выражения](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span><span class="sxs-lookup"><span data-stu-id="5b085-138">For more information, see [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span></span>

## <a name="repeat-until-success-loop"></a><span data-ttu-id="5b085-139">Цикл "повторить" до "успешно"</span><span class="sxs-lookup"><span data-stu-id="5b085-139">Repeat-until-success loop</span></span>

<span data-ttu-id="5b085-140">Этот Q# язык позволяет классического потока управления зависеть от результатов измерения Кубитс.</span><span class="sxs-lookup"><span data-stu-id="5b085-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="5b085-141">Эта возможность, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить вычислительные затраты для реализации унитариес.</span><span class="sxs-lookup"><span data-stu-id="5b085-141">This capability, in turn, enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="5b085-142">Примерами таких шаблонов являются *повторение до успешного выполнения* (RUS) в Q# .</span><span class="sxs-lookup"><span data-stu-id="5b085-142">Examples of this are the *repeat-until-success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="5b085-143">Эти шаблоны RUS *представляют собой вероятностная программы с низкой* стоимостью в терминах простейших шлюзов. Стоимость полагается на фактическое выполнение и за несколько возможных ветвлений.</span><span class="sxs-lookup"><span data-stu-id="5b085-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates; the incurred cost depends on the actual run and the interleaving of the multiple possible branchings.</span></span>

<span data-ttu-id="5b085-144">Для упрощения шаблонов повторения до успешного завершения (RUS) Q# поддерживает конструкции</span><span class="sxs-lookup"><span data-stu-id="5b085-144">To facilitate repeat-until-success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="5b085-145">где `expression` — любое допустимое выражение, результатом вычисления которого является значение типа `Bool` .</span><span class="sxs-lookup"><span data-stu-id="5b085-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="5b085-146">Выполняется тело цикла, после чего вычисляется условие.</span><span class="sxs-lookup"><span data-stu-id="5b085-146">The loop body runs, and then the condition is evaluated.</span></span>
<span data-ttu-id="5b085-147">Если условие истинно, инструкция завершается; в противном случае запускается адресная привязка и инструкция запускается снова, начиная с тела цикла.</span><span class="sxs-lookup"><span data-stu-id="5b085-147">If the condition is true, then the statement is completed; otherwise, the fixup runs, and the statement runs again, starting with the loop body.</span></span>

<span data-ttu-id="5b085-148">Все три части цикла RUS (текст, тест и адресная привязка) обрабатываются как единая область *для каждого повторения*, поэтому символы, привязанные к телу, доступны как в тесте, так и в адресной привязке.</span><span class="sxs-lookup"><span data-stu-id="5b085-148">All three portions of an RUS loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in both the test and the fixup.</span></span>
<span data-ttu-id="5b085-149">Однако завершение выполнения адресной привязки завершает область действия инструкции, чтобы привязки символов, сделанные во время тела или исправления, были недоступны при последующих повторах.</span><span class="sxs-lookup"><span data-stu-id="5b085-149">However, completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="5b085-150">Кроме того, `fixup` оператор часто полезен, но не всегда нужен.</span><span class="sxs-lookup"><span data-stu-id="5b085-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="5b085-151">В случаях, когда это не требуется, конструкция</span><span class="sxs-lookup"><span data-stu-id="5b085-151">In cases that it is not needed, the construct</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression);
```

<span data-ttu-id="5b085-152">также является допустимым шаблоном RUS.</span><span class="sxs-lookup"><span data-stu-id="5b085-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="5b085-153">Дополнительные примеры и подробные сведения см. в разделе [примеры повторения до успешного выполнения](#repeat-until-success-examples) в этой статье.</span><span class="sxs-lookup"><span data-stu-id="5b085-153">For more examples and details, see [Repeat-until-success examples](#repeat-until-success-examples) in this article.</span></span>

> [!TIP]   
> <span data-ttu-id="5b085-154">Избегайте использования циклов повторения до успешного выполнения в функциях.</span><span class="sxs-lookup"><span data-stu-id="5b085-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="5b085-155">Используйте циклы *while* , чтобы обеспечить соответствующую функциональность внутри функций.</span><span class="sxs-lookup"><span data-stu-id="5b085-155">Use *while* loops to provide the corresponding functionality inside functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="5b085-156">Цикл while</span><span class="sxs-lookup"><span data-stu-id="5b085-156">While loop</span></span>

<span data-ttu-id="5b085-157">Шаблоны Repeat-Until-Success имеют очень много времени.</span><span class="sxs-lookup"><span data-stu-id="5b085-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="5b085-158">Они широко используются в определенных классах алгоритмов тактов, поэтому выделенная конструкция языка в Q# .</span><span class="sxs-lookup"><span data-stu-id="5b085-158">They are widely used in particular classes of quantum algorithms - hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="5b085-159">Однако циклы, которые нарушаются в зависимости от условия и длина выполнения которого, таким способом, неизвестны во время компиляции, обрабатываются с определенной осторожностью в среде выполнения такта.</span><span class="sxs-lookup"><span data-stu-id="5b085-159">However, loops that break based on a condition and whose execution length is thus unknown at compile-time, are handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="5b085-160">Однако их использование в функциях не является проблемой, так как эти циклы содержат только код, который выполняется на обычном (не такте) оборудовании.</span><span class="sxs-lookup"><span data-stu-id="5b085-160">However, their use within functions is unproblematic since these loops only contain code that runs on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="5b085-161">Q#Таким образом, поддерживает использование циклов while только внутри функций.</span><span class="sxs-lookup"><span data-stu-id="5b085-161">Q#, therefore, supports to use of while loops within functions only.</span></span> <span data-ttu-id="5b085-162">`while`Оператор состоит из ключевого слова `while` , логического выражения в круглых скобках и блока операторов.</span><span class="sxs-lookup"><span data-stu-id="5b085-162">A `while` statement consists of the keyword `while`, a Boolean expression in parentheses, and a statement block.</span></span>
<span data-ttu-id="5b085-163">Блок операторов (тело цикла) выполняется до тех пор, пока условие принимает значение `true` .</span><span class="sxs-lookup"><span data-stu-id="5b085-163">The statement block (the body of the loop) runs as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="return-statement"></a><span data-ttu-id="5b085-164">Оператор Return</span><span class="sxs-lookup"><span data-stu-id="5b085-164">Return Statement</span></span>

<span data-ttu-id="5b085-165">Оператор Return завершает выполнение операции или функции и возвращает значение вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="5b085-165">The return statement ends the run of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="5b085-166">Он состоит из ключевого слова `return` , за которым следует выражение соответствующего типа и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="5b085-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="5b085-167">например следующие.</span><span class="sxs-lookup"><span data-stu-id="5b085-167">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="5b085-168">or</span><span class="sxs-lookup"><span data-stu-id="5b085-168">or</span></span>
```qsharp
return (results, qubits);
```

* <span data-ttu-id="5b085-169">Вызываемый метод, возвращающий пустой кортеж, не `()` требует наличия оператора return.</span><span class="sxs-lookup"><span data-stu-id="5b085-169">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
* <span data-ttu-id="5b085-170">Чтобы указать ранний выход из операции или функции, используйте `return ();` .</span><span class="sxs-lookup"><span data-stu-id="5b085-170">To specify an early exit from the operation or function, use `return ();`.</span></span>
<span data-ttu-id="5b085-171">Для вызова, возвращающего любой другой тип, требуется завершающий оператор return.</span><span class="sxs-lookup"><span data-stu-id="5b085-171">Callables that return any other type require a final return statement.</span></span>
* <span data-ttu-id="5b085-172">В операции отсутствует максимальное число инструкций Return.</span><span class="sxs-lookup"><span data-stu-id="5b085-172">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="5b085-173">Компилятор может выдать предупреждение, если операторы следуют за оператором Return в блоке.</span><span class="sxs-lookup"><span data-stu-id="5b085-173">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

   
## <a name="fail-statement"></a><span data-ttu-id="5b085-174">Оператор Fail</span><span class="sxs-lookup"><span data-stu-id="5b085-174">Fail statement</span></span>

<span data-ttu-id="5b085-175">Оператор Fail завершает выполнение операции и возвращает вызывающему объекту значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="5b085-175">The fail statement ends the run of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="5b085-176">Он состоит из ключевого слова `fail` , за которым следует строка и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="5b085-176">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="5b085-177">Инструкция возвращает строку в классический драйвер в качестве сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="5b085-177">The statement returns the string to the classical driver as the error message.</span></span>

<span data-ttu-id="5b085-178">Количество инструкций Fail в операции не ограничено.</span><span class="sxs-lookup"><span data-stu-id="5b085-178">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="5b085-179">Компилятор может выдать предупреждение, если операторы следуют за оператором Fail в блоке.</span><span class="sxs-lookup"><span data-stu-id="5b085-179">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="5b085-180">например следующие.</span><span class="sxs-lookup"><span data-stu-id="5b085-180">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="5b085-181">или с помощью [интерполяции строк](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="5b085-181">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="5b085-182">Примеры повторения до успешного выполнения</span><span class="sxs-lookup"><span data-stu-id="5b085-182">Repeat-until-success examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="5b085-183">Шаблон RUS для однокубитного вращения по оси иррациональная</span><span class="sxs-lookup"><span data-stu-id="5b085-183">RUS pattern for single-qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="5b085-184">В типичном варианте использования Следующая Q# Операция реализует поворот вокруг иррациональная оси $ (I + 2i Z)/\скрт {5} $ в БЛОЧ Sphere.</span><span class="sxs-lookup"><span data-stu-id="5b085-184">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="5b085-185">В реализации используется известный шаблон RUS:</span><span class="sxs-lookup"><span data-stu-id="5b085-185">The implementation uses a known RUS pattern:</span></span>

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

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a><span data-ttu-id="5b085-186">RUS-цикл с изменяемой переменной в области видимости</span><span class="sxs-lookup"><span data-stu-id="5b085-186">RUS loop with a mutable variable in scope</span></span>

<span data-ttu-id="5b085-187">В этом примере показано использование изменяемой переменной, `finished` которая находится в области действия всего цикла повторения до и после цикла, которая инициализируется перед циклом и обновляется в шаге исправления.</span><span class="sxs-lookup"><span data-stu-id="5b085-187">This example shows the use of a mutable variable, `finished`, which is within the scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

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

### <a name="rus-without-fixup"></a><span data-ttu-id="5b085-188">RUS без`fixup`</span><span class="sxs-lookup"><span data-stu-id="5b085-188">RUS without `fixup`</span></span>

<span data-ttu-id="5b085-189">В этом примере показан цикл RUS без шага исправления.</span><span class="sxs-lookup"><span data-stu-id="5b085-189">This example shows an RUS loop without the fixup step.</span></span> <span data-ttu-id="5b085-190">Код представляет собой цепь вероятностная, которая реализует важный шлюз ротации $V _3 = (\болдоне + 2 i Z)/\скрт {5} $ с использованием `H` `T` шлюзов и.</span><span class="sxs-lookup"><span data-stu-id="5b085-190">The code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="5b085-191">Цикл завершается в среднем на $ \фрак {8} {5} $.</span><span class="sxs-lookup"><span data-stu-id="5b085-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="5b085-192">Дополнительные сведения см. в разделе [*Повтор-Until-Success: недетерминированная декомпозиция одного кубит унитариес*](https://arxiv.org/abs/1311.1074) (Паетзникк и своре, 2014).</span><span class="sxs-lookup"><span data-stu-id="5b085-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

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

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="5b085-193">RUS для подготовки состояния такта</span><span class="sxs-lookup"><span data-stu-id="5b085-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="5b085-194">Наконец, ниже приведен пример шаблона RUS для подготовки состояния такта $ \фрак {1} {\скрт {3} } \лефт (\скрт {2} \кет {0} + \кет {1} \ригхт) $, начиная с $ \кет{+} $ State.</span><span class="sxs-lookup"><span data-stu-id="5b085-194">Finally, here is an example of an RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>

<span data-ttu-id="5b085-195">В этой операции показаны следующие важные программные функции.</span><span class="sxs-lookup"><span data-stu-id="5b085-195">Notable programmatic features shown in this operation are:</span></span>

* <span data-ttu-id="5b085-196">Более сложная `fixup` часть цикла, включающая в себя операции обработки тактов.</span><span class="sxs-lookup"><span data-stu-id="5b085-196">A more complex `fixup` part of the loop, which involves quantum operations.</span></span> 
* <span data-ttu-id="5b085-197">Использование `AssertMeasurementProbability` инструкций для определения вероятности измерения состояния такта в некоторых указанных точках программы.</span><span class="sxs-lookup"><span data-stu-id="5b085-197">The use of `AssertMeasurementProbability` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>

<span data-ttu-id="5b085-198">Дополнительные сведения об [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) операциях и см. в разделе [тестирование и отладка](xref:microsoft.quantum.guide.testingdebugging).</span><span class="sxs-lookup"><span data-stu-id="5b085-198">For more information about the [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) and [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) operations, see [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

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

<span data-ttu-id="5b085-199">Дополнительные сведения см. [в разделе Пример модульного тестирования, предоставленный в стандартной библиотеке](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="5b085-199">For more information, see [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

## <a name="next-steps"></a><span data-ttu-id="5b085-200">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="5b085-200">Next steps</span></span>

<span data-ttu-id="5b085-201">Сведения о [тестировании и отладке](xref:microsoft.quantum.guide.testingdebugging) в Q# .</span><span class="sxs-lookup"><span data-stu-id="5b085-201">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>
