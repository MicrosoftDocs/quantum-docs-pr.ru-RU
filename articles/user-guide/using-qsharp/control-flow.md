---
title: 'Поток управления в Q #'
description: Циклы, условные выражения и т. д.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: c534e016fcb8b50e66c11ca29c253ba0512acc6e
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430957"
---
# <a name="control-flow-in-q"></a><span data-ttu-id="29682-103">Поток управления в Q #</span><span class="sxs-lookup"><span data-stu-id="29682-103">Control Flow in Q#</span></span>

<span data-ttu-id="29682-104">Внутри операции или функции каждая инструкция выполняется по порядку, аналогично наиболее распространенным императивным классическим языкам.</span><span class="sxs-lookup"><span data-stu-id="29682-104">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="29682-105">Однако этот поток управления можно изменить тремя разными способами:</span><span class="sxs-lookup"><span data-stu-id="29682-105">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="29682-106">`if`инструкции</span><span class="sxs-lookup"><span data-stu-id="29682-106">`if` statements</span></span>
- <span data-ttu-id="29682-107">`for`бираются</span><span class="sxs-lookup"><span data-stu-id="29682-107">`for` loops</span></span>
- <span data-ttu-id="29682-108">`repeat`-`until`бираются</span><span class="sxs-lookup"><span data-stu-id="29682-108">`repeat`-`until` loops</span></span>

<span data-ttu-id="29682-109">Мы относимся к обсуждению второго варианта [ниже](#repeat-until-success-loop).</span><span class="sxs-lookup"><span data-stu-id="29682-109">We defer discussion of the latter to further [below](#repeat-until-success-loop).</span></span>
<span data-ttu-id="29682-110">`if` `for` Однако конструкции потока управления и имеют привычный смысл для большинства классических языков программирования.</span><span class="sxs-lookup"><span data-stu-id="29682-110">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>

<span data-ttu-id="29682-111">Важно, `for` что циклы и `if` операторы можно даже использовать в операциях, для которых автоматически создаются специализации.</span><span class="sxs-lookup"><span data-stu-id="29682-111">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="29682-112">В этом случае смежная часть `for` цикла обращается к направлению и принимает смежную часть каждой итерации.</span><span class="sxs-lookup"><span data-stu-id="29682-112">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="29682-113">Это соответствует принципу "обувь-and-Socks": Если вы хотите отменить размещение по протоколу SOCKS, а затем обувь, необходимо отменить помещение обувь, а затем отменить последующую операцию по протоколу SOCKS.</span><span class="sxs-lookup"><span data-stu-id="29682-113">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="29682-114">Это решение работает менее эффективно, и вы можете использовать протокол Socks, пока вы по-прежнему людьмие обувь!</span><span class="sxs-lookup"><span data-stu-id="29682-114">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="if-else-if-else"></a><span data-ttu-id="29682-115">If, else — if, else</span><span class="sxs-lookup"><span data-stu-id="29682-115">If, Else-if, Else</span></span>

<span data-ttu-id="29682-116">`if`Оператор поддерживает условное выполнение.</span><span class="sxs-lookup"><span data-stu-id="29682-116">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="29682-117">Он состоит из ключевого слова `if` , открывающей скобки `(` , логического выражения, закрывающей скобки `)` и блока операторов (блок _then_ ).</span><span class="sxs-lookup"><span data-stu-id="29682-117">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="29682-118">За этим может следовать любое число предложений else-if, каждое из которых состоит из ключевого слова `elif` , открывающей скобки `(` , логического выражения, закрывающей скобки `)` и блока операторов ( _Else-If_ ).</span><span class="sxs-lookup"><span data-stu-id="29682-118">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="29682-119">Наконец, оператор может при необходимости завершиться предложением else, которое состоит из ключевого слова, `else` за которым следует другой блок операторов (блок _else_ ).</span><span class="sxs-lookup"><span data-stu-id="29682-119">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="29682-120">`if`Условие вычисляется, и, если оно равно true, выполняется блок then.</span><span class="sxs-lookup"><span data-stu-id="29682-120">The `if` condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="29682-121">Если условие имеет значение false, то проверяется первое условие else-if; Если значение равно true, выполняется блок Else-If.</span><span class="sxs-lookup"><span data-stu-id="29682-121">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="29682-122">В противном случае проверяется второй блок-If, а затем третий и т. д., пока не будет обнаружено предложение с истинным условием или отсутствуют другие предложения Else-If.</span><span class="sxs-lookup"><span data-stu-id="29682-122">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="29682-123">Если исходное условие If и все предложения Else-If имеют значение false, то блок Else выполняется, если он был предоставлен.</span><span class="sxs-lookup"><span data-stu-id="29682-123">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="29682-124">Обратите внимание, что любой блок выполняется в своей собственной области.</span><span class="sxs-lookup"><span data-stu-id="29682-124">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="29682-125">Привязки, сделанные внутри `if` `elif` блока, или, `else` не видны после завершения.</span><span class="sxs-lookup"><span data-stu-id="29682-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after its end.</span></span>

<span data-ttu-id="29682-126">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="29682-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="29682-127">or</span><span class="sxs-lookup"><span data-stu-id="29682-127">or</span></span>
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

## <a name="for-loop"></a><span data-ttu-id="29682-128">Цикл For</span><span class="sxs-lookup"><span data-stu-id="29682-128">For Loop</span></span>

<span data-ttu-id="29682-129">`for`Инструкция поддерживает итерацию по диапазону целых чисел или к массиву.</span><span class="sxs-lookup"><span data-stu-id="29682-129">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="29682-130">Оператор состоит из ключевого слова `for` , открывающей скобки `(` , за которой следует символ или кортеж символов, ключевое слово `in` , выражение типа `Range` или массива, закрывающая круглая скобка `)` и блок операторов.</span><span class="sxs-lookup"><span data-stu-id="29682-130">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="29682-131">Блок операторов (тело цикла) выполняется повторно с определенными символами (переменными цикла), привязанными к каждому значению в диапазоне или массиве.</span><span class="sxs-lookup"><span data-stu-id="29682-131">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="29682-132">Обратите внимание, что если выражение диапазона принимает пустой диапазон или массив, тело не будет выполняться вообще.</span><span class="sxs-lookup"><span data-stu-id="29682-132">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="29682-133">Выражение полностью вычисляется перед входом в цикл и не будет изменяться во время выполнения цикла.</span><span class="sxs-lookup"><span data-stu-id="29682-133">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="29682-134">Переменная цикла привязывается к каждому входу в тело цикла и не привязана к концу тела.</span><span class="sxs-lookup"><span data-stu-id="29682-134">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="29682-135">В частности, переменная цикла не привязана после завершения цикла for.</span><span class="sxs-lookup"><span data-stu-id="29682-135">In particular, the loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="29682-136">Привязка объявленных символов является неизменяемой и соответствует тем же правилам, что и другие привязки переменных.</span><span class="sxs-lookup"><span data-stu-id="29682-136">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="29682-137">В некоторых примерах допустим `qubits` является регистром Кубитс (т. е. типа `Qubit[]` ),</span><span class="sxs-lookup"><span data-stu-id="29682-137">For some examples, supposing `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

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
<span data-ttu-id="29682-138">Обратите внимание, что в конце мы использовали бинарный оператор арифметического сдвига влево, `<<<` который можно найти в [числовых выражениях](xref:microsoft.quantum.guide.expressions#numeric-expressions) .</span><span class="sxs-lookup"><span data-stu-id="29682-138">Note that at the end we utilized the arithmetic-shift-left binary operator, `<<<`, details of which can be found at [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions)</span></span>


## <a name="repeat-until-success-loop"></a><span data-ttu-id="29682-139">Цикл "повторить" до "успешно"</span><span class="sxs-lookup"><span data-stu-id="29682-139">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="29682-140">Язык Q # позволяет классического потока управления зависеть от результатов измерения Кубитс.</span><span class="sxs-lookup"><span data-stu-id="29682-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="29682-141">Эта возможность, в свою очередь, позволяет реализовать мощные мини-приложения вероятностная, которые могут снизить вычислительные затраты для реализации унитариес.</span><span class="sxs-lookup"><span data-stu-id="29682-141">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="29682-142">В качестве примера можно легко реализовать так называемые шаблоны *повторения до успешного выполнения* (RUS) в Q #.</span><span class="sxs-lookup"><span data-stu-id="29682-142">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="29682-143">Эти шаблоны RUS являются вероятностная программами, которые имеют *ожидаемую* низкую стоимость в терминах простейших шлюзов, но для которых реальная стоимость зависит от фактического запуска и фактического перехода различных вариантов ветвления.</span><span class="sxs-lookup"><span data-stu-id="29682-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="29682-144">Чтобы упростить шаблоны повторения до успешного завершения (RUS), Q # поддерживает конструкции</span><span class="sxs-lookup"><span data-stu-id="29682-144">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="29682-145">где `expression` — любое допустимое выражение, результатом вычисления которого является значение типа `Bool` .</span><span class="sxs-lookup"><span data-stu-id="29682-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="29682-146">Выполняется тело цикла, а затем вычисляется условие.</span><span class="sxs-lookup"><span data-stu-id="29682-146">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="29682-147">Если условие истинно, инструкция завершается; в противном случае выполняется адресная привязка и выполняется повторная инструкция, начиная с тела цикла.</span><span class="sxs-lookup"><span data-stu-id="29682-147">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>

<span data-ttu-id="29682-148">Все три части цикла повтора и до (текст, тест и адресная привязка) обрабатываются как единая область *для каждого повторения*, поэтому символы, привязанные к тексту, доступны в тесте и в адресной привязке.</span><span class="sxs-lookup"><span data-stu-id="29682-148">All three portions of a repeat/until loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in the test and in the fixup.</span></span>
<span data-ttu-id="29682-149">Однако завершение выполнения адресной привязки завершает область действия инструкции, чтобы привязки символов, сделанные во время тела или исправления, были недоступны при последующих повторах.</span><span class="sxs-lookup"><span data-stu-id="29682-149">However completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="29682-150">Кроме того, `fixup` оператор часто полезен, но не всегда нужен.</span><span class="sxs-lookup"><span data-stu-id="29682-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="29682-151">В случаях, когда это не требуется, конструкция</span><span class="sxs-lookup"><span data-stu-id="29682-151">In cases that it is not needed, the construct</span></span>
```qsharp
repeat {
    // do stuff
}
until (expression);
```
<span data-ttu-id="29682-152">также является допустимым шаблоном RUS.</span><span class="sxs-lookup"><span data-stu-id="29682-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="29682-153">В нижней части этой страницы представлены некоторые [примеры циклов RUS](#repeat-until-success-examples).</span><span class="sxs-lookup"><span data-stu-id="29682-153">At the bottom of this page we present some [examples of RUS loops](#repeat-until-success-examples).</span></span>

> [!TIP]   
> <span data-ttu-id="29682-154">Избегайте использования циклов повторения до успешного выполнения в функциях.</span><span class="sxs-lookup"><span data-stu-id="29682-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="29682-155">Соответствующие функциональные возможности обеспечиваются циклами while в функциях.</span><span class="sxs-lookup"><span data-stu-id="29682-155">The corresponding functionality is provided by while loops in functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="29682-156">Цикл while</span><span class="sxs-lookup"><span data-stu-id="29682-156">While Loop</span></span>

<span data-ttu-id="29682-157">Шаблоны Repeat-Until-Success имеют очень много времени.</span><span class="sxs-lookup"><span data-stu-id="29682-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="29682-158">Они широко используются в определенных классах тактовых алгоритмов, поэтому выделенная конструкция языка в Q #.</span><span class="sxs-lookup"><span data-stu-id="29682-158">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="29682-159">Однако циклы, которые нарушаются в зависимости от условия и длина выполнения которого во время компиляции неизвестны, должны обрабатываться с определенной осторожностью в среде выполнения такта.</span><span class="sxs-lookup"><span data-stu-id="29682-159">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="29682-160">Их использование в функциях с другой стороны не является проблемой, поскольку в них содержится только код, который будет выполняться на обычном (не такте) оборудовании.</span><span class="sxs-lookup"><span data-stu-id="29682-160">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="29682-161">Таким образом, Q # поддерживает использование циклов while только внутри функций.</span><span class="sxs-lookup"><span data-stu-id="29682-161">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="29682-162">`while`Оператор состоит из ключевого слова `while` , открывающей скобки `(` , условия (т. е. логического выражения), закрывающей скобки `)` и блока операторов.</span><span class="sxs-lookup"><span data-stu-id="29682-162">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="29682-163">Блок операторов (тело цикла) выполняется при условии, что условие принимает значение `true` .</span><span class="sxs-lookup"><span data-stu-id="29682-163">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```


## <a name="return-statement"></a><span data-ttu-id="29682-164">Оператор Return</span><span class="sxs-lookup"><span data-stu-id="29682-164">Return Statement</span></span>

<span data-ttu-id="29682-165">Оператор Return завершает выполнение операции или функции и возвращает значение вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="29682-165">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="29682-166">Он состоит из ключевого слова `return` , за которым следует выражение соответствующего типа и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="29682-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="29682-167">Вызываемый метод, возвращающий пустой кортеж, не `()` требует наличия оператора return.</span><span class="sxs-lookup"><span data-stu-id="29682-167">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="29682-168">Если требуется ранний выход, `return ()` в этом случае может использоваться.</span><span class="sxs-lookup"><span data-stu-id="29682-168">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="29682-169">Для вызова, возвращающего любой другой тип, требуется завершающий оператор return.</span><span class="sxs-lookup"><span data-stu-id="29682-169">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="29682-170">В операции отсутствует максимальное число инструкций Return.</span><span class="sxs-lookup"><span data-stu-id="29682-170">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="29682-171">Компилятор может выдать предупреждение, если операторы следуют за оператором Return в блоке.</span><span class="sxs-lookup"><span data-stu-id="29682-171">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="29682-172">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="29682-172">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="29682-173">or</span><span class="sxs-lookup"><span data-stu-id="29682-173">or</span></span>
```qsharp
return ();
```
<span data-ttu-id="29682-174">or</span><span class="sxs-lookup"><span data-stu-id="29682-174">or</span></span>
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a><span data-ttu-id="29682-175">Оператор Fail</span><span class="sxs-lookup"><span data-stu-id="29682-175">Fail Statement</span></span>

<span data-ttu-id="29682-176">Инструкция Fail завершает выполнение операции и возвращает вызывающему объекту значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="29682-176">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="29682-177">Он состоит из ключевого слова `fail` , за которым следует строка и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="29682-177">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="29682-178">Строка возвращается в классический драйвер в качестве сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="29682-178">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="29682-179">Количество инструкций Fail в операции не ограничено.</span><span class="sxs-lookup"><span data-stu-id="29682-179">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="29682-180">Компилятор может выдать предупреждение, если операторы следуют за оператором Fail в блоке.</span><span class="sxs-lookup"><span data-stu-id="29682-180">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="29682-181">Например, примененная к объекту директива</span><span class="sxs-lookup"><span data-stu-id="29682-181">For example,</span></span>
```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="29682-182">или с помощью [интерполяции строк](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span><span class="sxs-lookup"><span data-stu-id="29682-182">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="29682-183">Примеры повторения до успешного выполнения</span><span class="sxs-lookup"><span data-stu-id="29682-183">Repeat-Until-Success Examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="29682-184">Шаблон RUS для одного кубит вращения по оси иррациональная</span><span class="sxs-lookup"><span data-stu-id="29682-184">RUS pattern for single qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="29682-185">В типичном варианте использования следующая операция Q # реализует поворот вокруг оси иррациональная $ (I + 2i Z)/\скрт {5} $ в БЛОЧ Sphere.</span><span class="sxs-lookup"><span data-stu-id="29682-185">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="29682-186">Это достигается с помощью известного шаблона RUS:</span><span class="sxs-lookup"><span data-stu-id="29682-186">This is accomplished by using a known RUS pattern:</span></span>

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

### <a name="rus-loop-with-mutable-variable-in-scope"></a><span data-ttu-id="29682-187">Цикл RUS с изменяемой переменной в области видимости</span><span class="sxs-lookup"><span data-stu-id="29682-187">RUS loop with mutable variable in scope</span></span>

<span data-ttu-id="29682-188">В этом примере показано использование изменяемой переменной `finished` , которая находится в области действия всего цикла Repeat-Until-unадресной привязки и инициализируется перед циклом и обновляется на шаге исправления.</span><span class="sxs-lookup"><span data-stu-id="29682-188">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

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

### <a name="rus-without-fixup"></a><span data-ttu-id="29682-189">RUS без`fixup`</span><span class="sxs-lookup"><span data-stu-id="29682-189">RUS without `fixup`</span></span>

<span data-ttu-id="29682-190">Например, следующий код представляет собой цепь вероятностная, которая реализует важный шлюз ротации $V _3 = (\болдоне + 2 i Z)/\скрт {5} $ с использованием `H` шлюзов и `T` .</span><span class="sxs-lookup"><span data-stu-id="29682-190">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="29682-191">Цикл завершается в среднем на $ \фрак {8} {5} $.</span><span class="sxs-lookup"><span data-stu-id="29682-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="29682-192">Дополнительные сведения см. в разделе [*Повтор-Until-Success: недетерминированная декомпозиция одного кубит унитариес*](https://arxiv.org/abs/1311.1074) (Паетзникк и своре, 2014).</span><span class="sxs-lookup"><span data-stu-id="29682-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

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

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="29682-193">RUS для подготовки состояния такта</span><span class="sxs-lookup"><span data-stu-id="29682-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="29682-194">Наконец, мы рассмотрим пример шаблона RUS для подготовки состояния такта $ \фрак {1} {\скрт {3} } \лефт (\скрт {2} \кет {0} + \кет {1} \ригхт) $, начиная с $ \кет{+} $ State.</span><span class="sxs-lookup"><span data-stu-id="29682-194">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="29682-195">См. также [Пример модульного тестирования, поставляемый со стандартной библиотекой](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="29682-195">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
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

<span data-ttu-id="29682-196">Важные программные функции, показанные в этой операции, — более сложная `fixup` часть цикла, которая включает в себя операции обработки тактов, а также использование `AssertProb` инструкций для определения вероятности измерения состояния такта в определенных точках программы.</span><span class="sxs-lookup"><span data-stu-id="29682-196">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="29682-197">Дополнительные сведения об операциях и см. в разделе [тестирование и отладка](xref:microsoft.quantum.guide.testingdebugging) [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) .</span><span class="sxs-lookup"><span data-stu-id="29682-197">See also [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>


## <a name="whats-next"></a><span data-ttu-id="29682-198">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="29682-198">What's Next?</span></span>
<span data-ttu-id="29682-199">Сведения о [тестировании и отладке](xref:microsoft.quantum.guide.testingdebugging) в Q #.</span><span class="sxs-lookup"><span data-stu-id="29682-199">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>