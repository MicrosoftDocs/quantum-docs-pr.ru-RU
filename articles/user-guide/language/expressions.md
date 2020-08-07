---
title: Выражения вQ#
description: Узнайте, как указывать, ссылаться и объединять константы, переменные, операторы, операции и функции в качестве выражений в Q# .
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- Q#
- $$v
ms.openlocfilehash: b6cc97dfee05dc843e213e84f17043714a8a9656
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869619"
---
# <a name="expressions-in-no-locq"></a><span data-ttu-id="79224-103">Выражения вQ#</span><span class="sxs-lookup"><span data-stu-id="79224-103">Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="79224-104">Числовые выражения</span><span class="sxs-lookup"><span data-stu-id="79224-104">Numeric Expressions</span></span>

<span data-ttu-id="79224-105">Числовые выражения — это выражения типа `Int` , `BigInt` или `Double` .</span><span class="sxs-lookup"><span data-stu-id="79224-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="79224-106">То есть это либо целочисленное, либо числовое число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="79224-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="79224-107">`Int`литералы в Q# записываются как последовательность цифр.</span><span class="sxs-lookup"><span data-stu-id="79224-107">`Int` literals in Q# are written as a sequence of digits.</span></span>
<span data-ttu-id="79224-108">Шестнадцатеричные и двоичные целые числа поддерживаются и записываются с `0x` `0b` префиксом и соответственно.</span><span class="sxs-lookup"><span data-stu-id="79224-108">Hexadecimal and binary integers are supported and written with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="79224-109">`BigInt`литералы в Q# имеют завершающий `l` суффикс или `L` .</span><span class="sxs-lookup"><span data-stu-id="79224-109">`BigInt` literals in Q# have a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="79224-110">Шестнадцатеричные большие целые числа поддерживаются и записываются с помощью префикса "0x".</span><span class="sxs-lookup"><span data-stu-id="79224-110">Hexadecimal big integers are supported and written with a "0x" prefix.</span></span>
<span data-ttu-id="79224-111">Таким образом, все следующие допустимые варианты использования `BigInt` литералов:</span><span class="sxs-lookup"><span data-stu-id="79224-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="79224-112">`Double`литералы в Q# — это числа с плавающей запятой, записанные с использованием десятичных цифр.</span><span class="sxs-lookup"><span data-stu-id="79224-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="79224-113">Они могут быть записаны с десятичной запятой или без нее, `.` или экспоненциальной частью, обозначенной как "e" или "e" (после чего допустимы только возможные отрицательные знаки и знаки после запятой).</span><span class="sxs-lookup"><span data-stu-id="79224-113">They can be written with or without a decimal point, `.`, or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="79224-114">Ниже приведены допустимые `Double` литералы: `0.0` , `1.2e5` , `1e-5` .</span><span class="sxs-lookup"><span data-stu-id="79224-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="79224-115">При наличии выражения массива любого типа элементов можно сформировать `Int` выражение с помощью [`Length`](xref:microsoft.quantum.core.length) встроенной функции с выражением массива, заключенным в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="79224-115">Given an array expression of any element type, you can form an `Int` expression using the [`Length`](xref:microsoft.quantum.core.length) built-in function, with the array expression enclosed in parentheses.</span></span>
<span data-ttu-id="79224-116">Например, если `a` привязан к массиву, то `Length(a)` является целочисленным выражением.</span><span class="sxs-lookup"><span data-stu-id="79224-116">For example, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="79224-117">Если `b` является массивом массивов целых чисел, то `Int[][]` `Length(b)` — число подмассивов в `b` , а `Length(b[1])` — число целых чисел во втором подмассиве в `b` .</span><span class="sxs-lookup"><span data-stu-id="79224-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="79224-118">При наличии двух числовых выражений одного типа бинарные операторы,, `+` `-` `*` и `/` могут использоваться для формирования нового числового выражения.</span><span class="sxs-lookup"><span data-stu-id="79224-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="79224-119">Тип нового выражения совпадает с типами составных выражений.</span><span class="sxs-lookup"><span data-stu-id="79224-119">The type of the new expression is the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="79224-120">При наличии двух целочисленных выражений используйте бинарный оператор `^` (Power) для формирования нового целочисленного выражения.</span><span class="sxs-lookup"><span data-stu-id="79224-120">Given two integer expressions, use the binary operator `^` (power) to form a new integer expression.</span></span>
<span data-ttu-id="79224-121">Аналогично, можно также использовать `^` с двумя двойными выражениями для формирования нового двойного выражения.</span><span class="sxs-lookup"><span data-stu-id="79224-121">Similarly, you can also use `^` with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="79224-122">Наконец, можно использовать `^` с большим целым числом слева и целым числом справа, чтобы сформировать новое большое целочисленное выражение.</span><span class="sxs-lookup"><span data-stu-id="79224-122">Finally, you can use `^` with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="79224-123">В этом случае второй параметр должен соответствовать 32 бит; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="79224-123">In this case, the second parameter must fit into 32 bits; if not, it raises a runtime error.</span></span>

<span data-ttu-id="79224-124">При наличии двух целочисленных или больших целочисленных выражений формирует новое целочисленное или большое целочисленное выражение с помощью `%` операторов (модуль), `&&&` (побитовое и), `|||` (побитовое или) или `^^^` (побитовое исключающее).</span><span class="sxs-lookup"><span data-stu-id="79224-124">Given two integer or big integer expressions, form a new integer or big integer expression using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="79224-125">При наличии целочисленного или длинного целочисленного выражения слева и целочисленного выражения справа используйте `<<<` операторы (арифметические сдвиги влево) или `>>>` (арифметические сдвиги вправо) для создания нового выражения с тем же типом, что и у левого выражения.</span><span class="sxs-lookup"><span data-stu-id="79224-125">Given either an integer or big integer expression on the left, and an integer expression on the right, use the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="79224-126">Второй параметр (сумма сдвига) для операции сдвига должен быть больше или равен нулю; поведение для отрицательных сумм сдвига не определено.</span><span class="sxs-lookup"><span data-stu-id="79224-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="79224-127">Сумма сдвига для операции сдвига также должна соответствовать 32 бит; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="79224-127">The shift amount for either shift operation must also fit into 32 bits; if not, it raises a runtime error.</span></span>
<span data-ttu-id="79224-128">Если число, смещенное, является целым числом, то величина сдвига интерпретируется, `mod 64` то есть сдвиг 1 и сдвиг 65 имеют одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="79224-128">If the number shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="79224-129">Для целочисленных и больших целочисленных значений сдвиги являются арифметическими.</span><span class="sxs-lookup"><span data-stu-id="79224-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="79224-130">Сдвиг отрицательного значения влево или вправо приводит к отрицательному числу.</span><span class="sxs-lookup"><span data-stu-id="79224-130">Shifting a negative value either left or right results in a negative number.</span></span>
<span data-ttu-id="79224-131">Это значит, что сдвиг на один шаг влево или вправо аналогичен умножению или делению на 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="79224-131">That is, shifting one step to the left or right is the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="79224-132">Целочисленный разделитель и модуль целых чисел соответствуют тому же поведению для отрицательных чисел, что и в C#.</span><span class="sxs-lookup"><span data-stu-id="79224-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="79224-133">То есть `a % b` всегда имеет тот же знак, что `a` и, и `b * (a / b) + a % b` всегда равно `a` .</span><span class="sxs-lookup"><span data-stu-id="79224-133">That is, `a % b` always has the same sign as `a`, and `b * (a / b) + a % b` always equals `a`.</span></span>
<span data-ttu-id="79224-134">Пример:</span><span class="sxs-lookup"><span data-stu-id="79224-134">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="79224-135">5</span><span class="sxs-lookup"><span data-stu-id="79224-135">5</span></span> | <span data-ttu-id="79224-136">2</span><span class="sxs-lookup"><span data-stu-id="79224-136">2</span></span> | <span data-ttu-id="79224-137">2</span><span class="sxs-lookup"><span data-stu-id="79224-137">2</span></span> | <span data-ttu-id="79224-138">1</span><span class="sxs-lookup"><span data-stu-id="79224-138">1</span></span>
 <span data-ttu-id="79224-139">5</span><span class="sxs-lookup"><span data-stu-id="79224-139">5</span></span> | <span data-ttu-id="79224-140">-2</span><span class="sxs-lookup"><span data-stu-id="79224-140">-2</span></span> | <span data-ttu-id="79224-141">-2</span><span class="sxs-lookup"><span data-stu-id="79224-141">-2</span></span> | <span data-ttu-id="79224-142">1</span><span class="sxs-lookup"><span data-stu-id="79224-142">1</span></span>
 <span data-ttu-id="79224-143">-5</span><span class="sxs-lookup"><span data-stu-id="79224-143">-5</span></span> | <span data-ttu-id="79224-144">2</span><span class="sxs-lookup"><span data-stu-id="79224-144">2</span></span> | <span data-ttu-id="79224-145">-2</span><span class="sxs-lookup"><span data-stu-id="79224-145">-2</span></span> | <span data-ttu-id="79224-146">-1</span><span class="sxs-lookup"><span data-stu-id="79224-146">-1</span></span>
 <span data-ttu-id="79224-147">-5</span><span class="sxs-lookup"><span data-stu-id="79224-147">-5</span></span> | <span data-ttu-id="79224-148">-2</span><span class="sxs-lookup"><span data-stu-id="79224-148">-2</span></span> | <span data-ttu-id="79224-149">2</span><span class="sxs-lookup"><span data-stu-id="79224-149">2</span></span> | <span data-ttu-id="79224-150">-1</span><span class="sxs-lookup"><span data-stu-id="79224-150">-1</span></span>

<span data-ttu-id="79224-151">Операции деления больших целых чисел и операций с модулями работают аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="79224-151">Big integer division and modulus operations work the same way.</span></span>

<span data-ttu-id="79224-152">Учитывая любое числовое выражение, можно сформировать новое выражение с помощью `-` унарного оператора.</span><span class="sxs-lookup"><span data-stu-id="79224-152">Given any numeric expression, you can form a new expression using the `-` unary operator.</span></span>
<span data-ttu-id="79224-153">Новое выражение имеет тот же тип, что и составное выражение.</span><span class="sxs-lookup"><span data-stu-id="79224-153">The new expression is the same type as the constituent expression.</span></span>

<span data-ttu-id="79224-154">При наличии целочисленного или длинного целочисленного выражения можно сформировать новое выражение того же типа с помощью `~~~` унарного оператора (побитовое дополнение).</span><span class="sxs-lookup"><span data-stu-id="79224-154">Given any integer or big integer expression, you can form a new expression of the same type using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="79224-155">Логические выражения</span><span class="sxs-lookup"><span data-stu-id="79224-155">Boolean Expressions</span></span>

<span data-ttu-id="79224-156">Двумя `Bool` литеральными значениями являются `true` и `false` .</span><span class="sxs-lookup"><span data-stu-id="79224-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="79224-157">При наличии двух выражений одного и того же примитивного типа `==` `!=` для создания выражения можно использовать бинарные операторы и `Bool` .</span><span class="sxs-lookup"><span data-stu-id="79224-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="79224-158">Выражение имеет значение true, если два выражения равны, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="79224-158">The expression is true if the two expressions are equal and false if not.</span></span>

<span data-ttu-id="79224-159">Значения определяемых пользователем типов могут не сравниваться, можно сравнивать только их неупакованные значения.</span><span class="sxs-lookup"><span data-stu-id="79224-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="79224-160">Например, с помощью оператора "Unwrap" `!` (подробно описывается в [типах в Q# ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span><span class="sxs-lookup"><span data-stu-id="79224-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="79224-161">Сравнение на равенство для `Qubit` значений — равенство по идентификатору, то есть, определяет, совпадают ли два выражения с одинаковым кубит.</span><span class="sxs-lookup"><span data-stu-id="79224-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="79224-162">Состояния двух Кубитс не сравниваются, обращаются, измеряются или изменяются при этом сравнении.</span><span class="sxs-lookup"><span data-stu-id="79224-162">The states of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="79224-163">Сравнение значений на равенство `Double` может привести к неверному результату из-за эффектов округления.</span><span class="sxs-lookup"><span data-stu-id="79224-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="79224-164">Например, `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="79224-164">For example, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="79224-165">При наличии двух числовых выражений бинарные операторы, `>` , `<` `>=` и `<=` могут использоваться для создания нового логического выражения, которое имеет значение true, если первое выражение соответственно больше, меньше, больше или равно или меньше или равно второму выражению.</span><span class="sxs-lookup"><span data-stu-id="79224-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="79224-166">При наличии двух логических выражений используйте `and` бинарный оператор для создания нового логического выражения, которое имеет значение true, если оба выражения имеют значение true.</span><span class="sxs-lookup"><span data-stu-id="79224-166">Given any two Boolean expressions, use the `and` binary operator to construct a new Boolean expression that is true if both of the two expressions are true.</span></span> <span data-ttu-id="79224-167">Аналогично, `or` при использовании оператора создается выражение, которое имеет значение true, если одно из двух выражений имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="79224-167">Likewise, using the `or` operator creates an expression that is true if either of the two expressions is true.</span></span>

<span data-ttu-id="79224-168">При наличии любого логического выражения `not` унарный оператор может использоваться для создания нового логического выражения, которое имеет значение true, если составное выражение имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="79224-168">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="79224-169">Строковые выражения</span><span class="sxs-lookup"><span data-stu-id="79224-169">String expressions</span></span>

<span data-ttu-id="79224-170">Q#позволяет использовать строки в `fail` инструкции (объясняются в [потоке управления](xref:microsoft.quantum.guide.controlflow#fail-statement)) и в [`Message`](xref:microsoft.quantum.intrinsic.message) стандартной функции.</span><span class="sxs-lookup"><span data-stu-id="79224-170">Q# allows strings to be used in the `fail` statement (explained in [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:microsoft.quantum.intrinsic.message) standard function.</span></span> <span data-ttu-id="79224-171">Конкретное поведение второго зависит от используемого симулятора, но обычно записывает сообщение в консоль узла при вызове во время выполнения Q# программы.</span><span class="sxs-lookup"><span data-stu-id="79224-171">The specific behavior of the latter depends on the simulator used but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="79224-172">Строки в Q# являются либо литералами, либо интерполяциями строк.</span><span class="sxs-lookup"><span data-stu-id="79224-172">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="79224-173">Строковые литералы похожи на простые строковые литералы в большинстве языков: последовательность символов Юникода, заключенная в двойные кавычки `" "` .</span><span class="sxs-lookup"><span data-stu-id="79224-173">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double-quotes `" "`.</span></span>
<span data-ttu-id="79224-174">Внутри строки используйте символ обратной косой черты `\` для экранирования символа двойной кавычки ( `\"` ) или для вставки новой строки ( `\n` ), возврата каретки ( `\r` ) или табуляции ( `\t` ).</span><span class="sxs-lookup"><span data-stu-id="79224-174">Inside of a string, use the backslash character `\` to escape a double-quote character (`\"`), or to insert a new-line ( `\n` ), a carriage return (`\r`), or a tab (`\t`).</span></span>
<span data-ttu-id="79224-175">Пример:</span><span class="sxs-lookup"><span data-stu-id="79224-175">For example:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="79224-176">Интерполированные строки</span><span class="sxs-lookup"><span data-stu-id="79224-176">Interpolated strings</span></span>

<span data-ttu-id="79224-177">Q#Синтаксис интерполяции строк представляет собой подмножество синтаксиса C#.</span><span class="sxs-lookup"><span data-stu-id="79224-177">The Q# syntax for string interpolations is a subset of the C# syntax.</span></span> <span data-ttu-id="79224-178">Ниже приведены основные моменты, к которым они относятся Q# .</span><span class="sxs-lookup"><span data-stu-id="79224-178">Following are the key points as they pertain to Q#:</span></span>

* <span data-ttu-id="79224-179">Для определения строкового литерала в качестве интерполированной строки добавьте к началу символ `$`.</span><span class="sxs-lookup"><span data-stu-id="79224-179">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span> <span data-ttu-id="79224-180">Между элементом `$` и `"` , который запускает строковый литерал, не должно быть пробелов.</span><span class="sxs-lookup"><span data-stu-id="79224-180">There can be no white space between the `$` and the `"` that starts a string literal.</span></span>

* <span data-ttu-id="79224-181">Ниже приведен простой пример использования [`Message`](xref:microsoft.quantum.intrinsic.message) функции для записи результата измерения в консоль вместе с другими Q# выражениями.</span><span class="sxs-lookup"><span data-stu-id="79224-181">The following is a basic example using the [`Message`](xref:microsoft.quantum.intrinsic.message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* <span data-ttu-id="79224-182">Любое допустимое Q# выражение может присутствовать в интерполяции строки.</span><span class="sxs-lookup"><span data-stu-id="79224-182">Any valid Q# expression may appear in an interpolated string.</span></span>

* <span data-ttu-id="79224-183">Выражения внутри строки с интерполяцией следуют Q# синтаксису, а не синтаксису C#.</span><span class="sxs-lookup"><span data-stu-id="79224-183">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span> <span data-ttu-id="79224-184">Самым заметным отличием является то, что не Q# поддерживает буквальные строки с интерполяцией (многострочные).</span><span class="sxs-lookup"><span data-stu-id="79224-184">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>

<span data-ttu-id="79224-185">Дополнительные сведения о синтаксисе C# см. в разделе [*интерполяция строк*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span><span class="sxs-lookup"><span data-stu-id="79224-185">For more details about the C# syntax, see [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>

## <a name="range-expressions"></a><span data-ttu-id="79224-186">Выражения диапазона</span><span class="sxs-lookup"><span data-stu-id="79224-186">Range Expressions</span></span>

<span data-ttu-id="79224-187">Учитывая все три `Int` выражения `start` , `step` и `stop` , выражение `start .. step .. stop` является выражением диапазона, первый элемент которого имеет значение `start` , второй элемент —, `start+step` третий элемент — `start+step+step` и т. д., пока не будет пройден `stop` .</span><span class="sxs-lookup"><span data-stu-id="79224-187">Given any three `Int` expressions `start`, `step`, and `stop`, the expression `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, and so on, until you pass `stop`.</span></span>
<span data-ttu-id="79224-188">Диапазон может быть пустым, если, например, `step` является положительным и `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="79224-188">A range may be empty if, for example, `step` is positive and `stop < start`.</span></span>

<span data-ttu-id="79224-189">Диапазон является инклюзивным на обоих концах.</span><span class="sxs-lookup"><span data-stu-id="79224-189">The range is inclusive at both ends.</span></span> <span data-ttu-id="79224-190">То есть, если разница между `start` и `stop` является целым числом, кратным `step` , последний элемент диапазона будет иметь значение `stop` .</span><span class="sxs-lookup"><span data-stu-id="79224-190">That is, if the difference between `start` and `stop` is an integer multiple of `step`, the last element of the range will be `stop`.</span></span>

<span data-ttu-id="79224-191">При наличии двух `Int` выражений `start` и `stop` выражение `start .. stop` является выражением диапазона, равным `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="79224-191">Given any two `Int` expressions `start` and `stop`, the expression `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="79224-192">Обратите внимание, что подразумеваемым `step` является + 1, даже если `stop` значение меньше `start` ; в этом случае диапазон пуст.</span><span class="sxs-lookup"><span data-stu-id="79224-192">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="79224-193">Ниже приведены некоторые примеры диапазонов.</span><span class="sxs-lookup"><span data-stu-id="79224-193">Some example ranges are:</span></span>

- <span data-ttu-id="79224-194">`1..3`диапазон значений 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="79224-194">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="79224-195">`2..2..5`диапазон 2, 4.</span><span class="sxs-lookup"><span data-stu-id="79224-195">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="79224-196">`2..2..6`— диапазон 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="79224-196">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="79224-197">`6..-2..2`— диапазон 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="79224-197">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="79224-198">`2..1`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="79224-198">`2..1` is the empty range.</span></span>
- <span data-ttu-id="79224-199">`2..6..7`— диапазон 2.</span><span class="sxs-lookup"><span data-stu-id="79224-199">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="79224-200">`2..2..1`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="79224-200">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="79224-201">`1..-1..2`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="79224-201">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="79224-202">Выражения кубит</span><span class="sxs-lookup"><span data-stu-id="79224-202">Qubit Expressions</span></span>

<span data-ttu-id="79224-203">Единственными `Qubit` выражениями являются символы, привязанные к `Qubit` значениям или элементам массива `Qubit` массивов.</span><span class="sxs-lookup"><span data-stu-id="79224-203">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="79224-204">`Qubit`Литералы отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="79224-204">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="79224-205">Выражения Паули</span><span class="sxs-lookup"><span data-stu-id="79224-205">Pauli Expressions</span></span>

<span data-ttu-id="79224-206">Все четыре `Pauli` значения,,, `PauliI` `PauliX` `PauliY` и `PauliZ` , являются допустимыми `Pauli` выражениями.</span><span class="sxs-lookup"><span data-stu-id="79224-206">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="79224-207">Кроме того, единственными `Pauli` выражениями являются символы, привязанные к `Pauli` значениям или элементам массива `Pauli` массивов.</span><span class="sxs-lookup"><span data-stu-id="79224-207">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="79224-208">Выражения результатов</span><span class="sxs-lookup"><span data-stu-id="79224-208">Result Expressions</span></span>

<span data-ttu-id="79224-209">Два `Result` значения, `One` и `Zero` , являются допустимыми `Result` выражениями.</span><span class="sxs-lookup"><span data-stu-id="79224-209">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="79224-210">Кроме того, единственными `Result` выражениями являются символы, привязанные к `Result` значениям или элементам массива `Result` массивов.</span><span class="sxs-lookup"><span data-stu-id="79224-210">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="79224-211">В частности, обратите внимание, что `One` не совпадает с целым числом `1` и прямое преобразование между ними отсутствует.</span><span class="sxs-lookup"><span data-stu-id="79224-211">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="79224-212">Это справедливо `Zero` и для и `0` .</span><span class="sxs-lookup"><span data-stu-id="79224-212">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="79224-213">Кортежные выражения</span><span class="sxs-lookup"><span data-stu-id="79224-213">Tuple Expressions</span></span>

<span data-ttu-id="79224-214">Литерал кортежа — это последовательность выражений элементов соответствующего типа, разделенных запятыми, заключенная в круглые скобки.</span><span class="sxs-lookup"><span data-stu-id="79224-214">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in parentheses.</span></span>
<span data-ttu-id="79224-215">Например, `(1, One)` является `(Int, Result)` выражением.</span><span class="sxs-lookup"><span data-stu-id="79224-215">For example, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="79224-216">Кроме литералов, единственными кортежными выражениями являются символы, привязанные к значениям кортежа, элементы массива кортежей и вызываемые вызовы, возвращающие кортежи.</span><span class="sxs-lookup"><span data-stu-id="79224-216">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="79224-217">Выражения определяемого пользователем типа</span><span class="sxs-lookup"><span data-stu-id="79224-217">User-Defined Type Expressions</span></span>

<span data-ttu-id="79224-218">Литерал определяемого пользователем типа состоит из имени типа, за которым следует литерал кортежа базового типа кортежа типа.</span><span class="sxs-lookup"><span data-stu-id="79224-218">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="79224-219">Например, если `IntPair` является определяемым пользователем типом, основанным на `(Int, Int)` , то `IntPair(2, 3)` является допустимым литералом этого типа.</span><span class="sxs-lookup"><span data-stu-id="79224-219">For example, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` is a valid literal of that type.</span></span>

<span data-ttu-id="79224-220">Кроме литералов, единственными выражениями определяемого пользователем типа являются символы, привязанные к значениям этого типа, элементы массива массивов этого типа и вызываемые вызовы, возвращающие этот тип.</span><span class="sxs-lookup"><span data-stu-id="79224-220">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="79224-221">Разносить выражения</span><span class="sxs-lookup"><span data-stu-id="79224-221">Unwrap Expressions</span></span>

<span data-ttu-id="79224-222">В Q# оператор Unwrap — это восклицательный знак в конце `!` .</span><span class="sxs-lookup"><span data-stu-id="79224-222">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="79224-223">Например, если `IntPair` является определяемым пользователем типом с базовым типом `(Int, Int)` и `s` является переменной со значением `IntPair(2, 3)` , то `s!` имеет значение `(2, 3)` .</span><span class="sxs-lookup"><span data-stu-id="79224-223">For example, if `IntPair` is a user-defined type with the underlying type `(Int, Int)` and `s` is a variable with value `IntPair(2, 3)`, then `s!` is `(2, 3)`.</span></span>

<span data-ttu-id="79224-224">Для определяемых пользователем типов, определенных с точки зрения других определяемых пользователем типов, можно повторить оператор Unwrap.</span><span class="sxs-lookup"><span data-stu-id="79224-224">For user-defined types defined in terms of other user-defined types, you can repeat the unwrap operator.</span></span> <span data-ttu-id="79224-225">Например, `s!!` указывает значение удвоенного неупакованного значения `s` .</span><span class="sxs-lookup"><span data-stu-id="79224-225">For example, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="79224-226">Таким же, если `WrappedPair` является определяемым пользователем типом с базовым типом `IntPair` и `t` является переменной со значением `WrappedPair(IntPair(1,2))` , то имеет значение `t!!` `(1,2)` .</span><span class="sxs-lookup"><span data-stu-id="79224-226">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` is `(1,2)`.</span></span>

<span data-ttu-id="79224-227">`!`Оператор имеет более высокий приоритет, чем все остальные операторы `[]` , кроме для индексирования и среза массива.</span><span class="sxs-lookup"><span data-stu-id="79224-227">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="79224-228">`!`и `[]` привяжите позиционированное значение, то есть `a[i]![3]` считывается следующим образом `((a[i])!)[3]` : взять `i` элемент th `a` , распаковать его, а затем получить третий элемент неупакованного значения (который должен быть массивом).</span><span class="sxs-lookup"><span data-stu-id="79224-228">`!` and `[]` bind positionally; that is, `a[i]![3]` is read as `((a[i])!)[3]`: take the `i`th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="79224-229">Приоритет `!` оператора имеет одно влияние, которое может быть неочевидным.</span><span class="sxs-lookup"><span data-stu-id="79224-229">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="79224-230">Если функция или операция возвращает значение, которое затем извлекается, функция или вызов операции должны быть заключены в круглые скобки, чтобы кортеж аргументов привязывается к вызову, а не к развернутому.</span><span class="sxs-lookup"><span data-stu-id="79224-230">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="79224-231">Пример:</span><span class="sxs-lookup"><span data-stu-id="79224-231">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="79224-232">Выражения массива</span><span class="sxs-lookup"><span data-stu-id="79224-232">Array Expressions</span></span>

<span data-ttu-id="79224-233">Литерал массива — это последовательность из одного или нескольких выражений элементов, разделенных запятыми, заключенная в квадратные скобки `[]` .</span><span class="sxs-lookup"><span data-stu-id="79224-233">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in square brackets `[]`.</span></span>
<span data-ttu-id="79224-234">Все элементы должны быть совместимы с одним и тем же типом.</span><span class="sxs-lookup"><span data-stu-id="79224-234">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="79224-235">При наличии двух массивов одного типа используйте бинарный `+` оператор для формирования нового массива, который объединяет два массива.</span><span class="sxs-lookup"><span data-stu-id="79224-235">Given two arrays of the same type, use the binary `+` operator to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="79224-236">Например, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="79224-236">For example, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="79224-237">Создание массива</span><span class="sxs-lookup"><span data-stu-id="79224-237">Array Creation</span></span>

<span data-ttu-id="79224-238">При наличии типа и `Int` выражения используйте `new` оператор для выделения нового массива заданного размера.</span><span class="sxs-lookup"><span data-stu-id="79224-238">Given a type and an `Int` expression, use the `new` operator to allocate a new array of the given size.</span></span>
<span data-ttu-id="79224-239">Например, `new Int[i + 1]` выделяет новый `Int` массив с `i + 1` элементами.</span><span class="sxs-lookup"><span data-stu-id="79224-239">For example, `new Int[i + 1]` allocates a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="79224-240">Пустые литералы массива, такие как `[]` , не допускаются.</span><span class="sxs-lookup"><span data-stu-id="79224-240">Empty array literals, such as `[]`, are not allowed.</span></span>
<span data-ttu-id="79224-241">Вместо этого можно создать массив нулевой длины с помощью `new T[0]` , где — это `T` заполнитель для подходящего типа.</span><span class="sxs-lookup"><span data-stu-id="79224-241">Instead, you can create an array of length zero by using `new T[0]`, where `T` is a placeholder for a suitable type.</span></span>

<span data-ttu-id="79224-242">Элементы нового массива инициализируются значением по умолчанию, зависящим от типа.</span><span class="sxs-lookup"><span data-stu-id="79224-242">The elements of a new array initialize to a type-dependent default value.</span></span>
<span data-ttu-id="79224-243">В большинстве случаев это разновидность нуля.</span><span class="sxs-lookup"><span data-stu-id="79224-243">In most cases, this is some variation of zero.</span></span>

<span data-ttu-id="79224-244">Для Кубитс и вызываемых объектов, которые являются ссылками на сущности, не существует разумного значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="79224-244">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="79224-245">Таким образом, для этих типов по умолчанию используется недопустимая ссылка, которую нельзя использовать, не вызывая ошибку времени выполнения, аналогичную пустой ссылке на таких языках, как C# или Java.</span><span class="sxs-lookup"><span data-stu-id="79224-245">Thus, for these types, the default is an invalid reference that you cannot use without causing a runtime error, similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="79224-246">Массивы, содержащие Кубитс или вызываемые, должны быть инициализированы значениями, отличными от значений по умолчанию, прежде чем можно будет использовать их элементы безопасно.</span><span class="sxs-lookup"><span data-stu-id="79224-246">Arrays containing qubits or callables must be initialized with non-default values before you can use their elements safely.</span></span> <span data-ttu-id="79224-247">Подходящие процедуры инициализации см. в разделе <xref:microsoft.quantum.arrays> .</span><span class="sxs-lookup"><span data-stu-id="79224-247">For suitable initialization routines, see <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="79224-248">Значения по умолчанию для каждого типа:</span><span class="sxs-lookup"><span data-stu-id="79224-248">The default values for each type are:</span></span>

<span data-ttu-id="79224-249">Тип</span><span class="sxs-lookup"><span data-stu-id="79224-249">Type</span></span> | <span data-ttu-id="79224-250">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="79224-250">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="79224-251">_Недопустимый кубит_</span><span class="sxs-lookup"><span data-stu-id="79224-251">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="79224-252">Пустой диапазон,`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="79224-252">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="79224-253">_Недопустимый вызываемый_</span><span class="sxs-lookup"><span data-stu-id="79224-253">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="79224-254">Типы кортежей инициализируют элемент по элементу.</span><span class="sxs-lookup"><span data-stu-id="79224-254">Tuple types initialize element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="79224-255">Элементы массива</span><span class="sxs-lookup"><span data-stu-id="79224-255">Array Elements</span></span>

<span data-ttu-id="79224-256">При наличии выражения массива и `Int` выражения формируют новое выражение с помощью оператора элемента массива `[]` .</span><span class="sxs-lookup"><span data-stu-id="79224-256">Given an array expression and an `Int` expression, form a new expression using the array element operator `[]`.</span></span>
<span data-ttu-id="79224-257">Новое выражение имеет тот же тип, что и тип элемента массива.</span><span class="sxs-lookup"><span data-stu-id="79224-257">The new expression is the same type as the element type of the array.</span></span>
<span data-ttu-id="79224-258">Например, если `a` привязан к массиву типа `Double` , то `a[4]` является `Double` выражением.</span><span class="sxs-lookup"><span data-stu-id="79224-258">For example, if `a` is bound to an array of type `Double`, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="79224-259">Если выражение массива не является простым идентификатором, необходимо заключить его в круглые скобки, чтобы выбрать элемент.</span><span class="sxs-lookup"><span data-stu-id="79224-259">If the array expression is not a simple identifier, you must enclose it in parentheses to select an element.</span></span>
<span data-ttu-id="79224-260">Например, если `a` и `b` являются массивами типа `Int` , элемент из объединения выражается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="79224-260">For example, if `a` and `b` are both arrays of type `Int`, an element from the concatenation is expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="79224-261">Все массивы в Q# отсчитываются от нуля.</span><span class="sxs-lookup"><span data-stu-id="79224-261">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="79224-262">То есть первый элемент массива `a` всегда имеет значение `a[0]` .</span><span class="sxs-lookup"><span data-stu-id="79224-262">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="79224-263">Срезы массива</span><span class="sxs-lookup"><span data-stu-id="79224-263">Array Slices</span></span>

<span data-ttu-id="79224-264">При наличии выражения массива и `Range` выражения формируют новое выражение с помощью оператора среза массива `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="79224-264">Given an array expression and a `Range` expression, form a new expression using the array slice operator `[ ]`.</span></span>
<span data-ttu-id="79224-265">Новое выражение имеет тот же тип, что и массив, и содержит элементы массива, индексируемые элементами `Range` , в порядке, определенном `Range` .</span><span class="sxs-lookup"><span data-stu-id="79224-265">The new expression is the same type as the array and contains the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="79224-266">Например, если `a` привязан к массиву типа `Double` , то `a[3..-1..0]` представляет собой `Double[]` выражение, содержащее первые четыре элемента, `a` но в порядке, в котором они отображаются в `a` .</span><span class="sxs-lookup"><span data-stu-id="79224-266">For example, if `a` is bound to an array of type `Double`, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="79224-267">Если объект `Range` пуст, результирующий срез массива имеет нулевую длину.</span><span class="sxs-lookup"><span data-stu-id="79224-267">If the `Range` is empty, then the resulting array slice is zero length.</span></span>

<span data-ttu-id="79224-268">Как и для ссылок на элементы массива, если выражение массива не является простым идентификатором, его необходимо заключить в круглые скобки, чтобы разделить его.</span><span class="sxs-lookup"><span data-stu-id="79224-268">Just as with referencing array elements, if the array expression is not a simple identifier, you must enclose it in parentheses to slice it.</span></span>
<span data-ttu-id="79224-269">Например, если `a` и `b` являются массивами типа `Int` , срез из объединения выражается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="79224-269">For example, if `a` and `b` are both arrays of type `Int`, a slice from the concatenation is expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="79224-270">Выводимые начальные и конечные значения</span><span class="sxs-lookup"><span data-stu-id="79224-270">Inferred start/end values</span></span>

<span data-ttu-id="79224-271">Начиная с нашего [выпуска 0,8](xref:microsoft.quantum.relnotes)мы поддерживаем контекстные выражения для среза диапазона.</span><span class="sxs-lookup"><span data-stu-id="79224-271">Starting with our [0.8 release](xref:microsoft.quantum.relnotes), we support contextual expressions for range slicing.</span></span> <span data-ttu-id="79224-272">В частности, можно опустить начальные и конечные значения диапазона в контексте выражения среза диапазона.</span><span class="sxs-lookup"><span data-stu-id="79224-272">In particular, you may omit range start and end values in the context of a range slicing expression.</span></span> <span data-ttu-id="79224-273">В этом случае компилятор применяет следующие правила, чтобы определить предполагаемые разделители для диапазона:</span><span class="sxs-lookup"><span data-stu-id="79224-273">In that case, the compiler applies the following rules to infer the intended delimiters for the range:</span></span>

* <span data-ttu-id="79224-274">Если *Начальное* значение диапазона опущено, то выводимое начальное значение</span><span class="sxs-lookup"><span data-stu-id="79224-274">If the range *start* value is omitted, then the inferred start value</span></span>
  * <span data-ttu-id="79224-275">равно нулю, если шаг не указан или указанный шаг является положительным.</span><span class="sxs-lookup"><span data-stu-id="79224-275">is zero if no step is specified or the specified step is positive.</span></span>  
  * <span data-ttu-id="79224-276">Длина фрагментированного массива минус один, если указанный шаг является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="79224-276">is the length of the sliced array minus one if the specified step is negative.</span></span>

* <span data-ttu-id="79224-277">Если значение *конца* диапазона опущено, то выводимое конечное значение</span><span class="sxs-lookup"><span data-stu-id="79224-277">If the range *end* value is omitted, then the inferred end value</span></span>
  * <span data-ttu-id="79224-278">длина среза массива минус единица, если шаг не указан или указанный шаг является положительным.</span><span class="sxs-lookup"><span data-stu-id="79224-278">is the length of the sliced array minus one if no step is specified or the specified step is positive.</span></span>
  * <span data-ttu-id="79224-279">равно нулю, если указанный шаг является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="79224-279">is zero if the specified step is negative.</span></span>

<span data-ttu-id="79224-280">Некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="79224-280">Some examples are:</span></span>

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

### <a name="copy-and-update-expressions"></a><span data-ttu-id="79224-281">Выражения копирования и обновления</span><span class="sxs-lookup"><span data-stu-id="79224-281">Copy-and-Update Expressions</span></span>

<span data-ttu-id="79224-282">Так как все Q# типы являются типами значений (с Кубитс, принимающей несколько специальных ролей), формально «Copy» создается при привязке значения к символу или при повторной привязке символа.</span><span class="sxs-lookup"><span data-stu-id="79224-282">Since all Q# types are value types (with the qubits taking a somewhat special role), formally a "copy" is created when a value is bound to a symbol or when a symbol is rebound.</span></span> <span data-ttu-id="79224-283">Это означает, что поведение Q# аналогично тому, как если бы копия была создана с помощью оператора присваивания.</span><span class="sxs-lookup"><span data-stu-id="79224-283">That is to say, the behavior of Q# is the same as if a copy were created using an assignment operator.</span></span> 

<span data-ttu-id="79224-284">Конечно, на практике при необходимости создаются только соответствующие части.</span><span class="sxs-lookup"><span data-stu-id="79224-284">Of course, in practice, only the relevant pieces are recreated as needed.</span></span> <span data-ttu-id="79224-285">Это влияет на способ копирования массивов, поскольку невозможно обновить элементы массива.</span><span class="sxs-lookup"><span data-stu-id="79224-285">This affects how you copy arrays because it is not possible to update array items.</span></span> <span data-ttu-id="79224-286">Чтобы изменить существующий массив, необходимо использовать механизм *копирования и обновления* .</span><span class="sxs-lookup"><span data-stu-id="79224-286">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="79224-287">Можно создать новый массив из существующего массива с помощью выражений *копирования и обновления* , использующих операторы `w/` и `<-` .</span><span class="sxs-lookup"><span data-stu-id="79224-287">You can create a new array from an existing array via *copy-and-update* expressions, which use the operators `w/` and `<-`.</span></span>
<span data-ttu-id="79224-288">Выражение копирования и обновления является выражением формы `expression1 w/ expression2 <- expression3` , где</span><span class="sxs-lookup"><span data-stu-id="79224-288">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where</span></span>

* <span data-ttu-id="79224-289">`expression1`тип должен быть типом `T[]` `T` .</span><span class="sxs-lookup"><span data-stu-id="79224-289">`expression1` must be type `T[]` for some type `T`.</span></span>
* <span data-ttu-id="79224-290">`expression2`Определяет, какие индексы в массиве задаются в `expression1` для изменения.</span><span class="sxs-lookup"><span data-stu-id="79224-290">`expression2` defines which indices in the array specified in `expression1` to modify.</span></span> <span data-ttu-id="79224-291">`expression2`должен быть либо типом `Int` , либо типом `Range` .</span><span class="sxs-lookup"><span data-stu-id="79224-291">`expression2` must be either type `Int` or type `Range`.</span></span>
* <span data-ttu-id="79224-292">`expression3`— Это значения, используемые для обновления элементов в `expression1` на основе индексов, указанных в параметре `expression2` .</span><span class="sxs-lookup"><span data-stu-id="79224-292">`expression3` is the value(s) used to update elements in `expression1`, based on the indices specified in `expression2`.</span></span> <span data-ttu-id="79224-293">Если `expression2` имеет тип `Int` , то `expression3` должен иметь тип `T` .</span><span class="sxs-lookup"><span data-stu-id="79224-293">If `expression2` is type `Int`, `expression3` must be type `T`.</span></span> <span data-ttu-id="79224-294">Если `expression2` имеет тип `Range` , то `expression3` должен иметь тип `T[]` .</span><span class="sxs-lookup"><span data-stu-id="79224-294">If `expression2` is type `Range`, `expression3` must be type `T[]`.</span></span>

<span data-ttu-id="79224-295">Например, выражение копирования и обновления `arr w/ idx <- value` формирует новый массив со всеми элементами, для которых заданы соответствующие элементы в `arr` , за исключением элементов, заданных параметром `idx` , для которого заданы значения в `value` .</span><span class="sxs-lookup"><span data-stu-id="79224-295">For example, the copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding elements in `arr`, except for the element(s) specified by `idx`, which is set to the value(s) in `value`.</span></span> 

<span data-ttu-id="79224-296">Заданный `arr` объект содержит массив `[0,1,2,3]` , затем</span><span class="sxs-lookup"><span data-stu-id="79224-296">Given `arr` contains the array `[0,1,2,3]`, then</span></span> 

- <span data-ttu-id="79224-297">`arr w/ 0 <- 10`является массивом `[10,1,2,3]` .</span><span class="sxs-lookup"><span data-stu-id="79224-297">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="79224-298">`arr w/ 2 <- 10`является массивом `[0,1,10,3]` .</span><span class="sxs-lookup"><span data-stu-id="79224-298">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="79224-299">`arr w/ 0..2..3 <- [10,12]`является массивом `[10,1,12,3]` .</span><span class="sxs-lookup"><span data-stu-id="79224-299">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="79224-300">Выражения копирования и обновления для именованных элементов</span><span class="sxs-lookup"><span data-stu-id="79224-300">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="79224-301">Аналогичные выражения существуют для именованных элементов в определяемых пользователем типах.</span><span class="sxs-lookup"><span data-stu-id="79224-301">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="79224-302">Например, рассмотрим тип</span><span class="sxs-lookup"><span data-stu-id="79224-302">For example, consider the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="79224-303">Если `c` параметр содержит значение типа `Complex(1., -1.)` , то `c w/ Re <- 0.` является выражением типа `Complex` , результатом вычисления которого является `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="79224-303">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="79224-304">Массивы массивов</span><span class="sxs-lookup"><span data-stu-id="79224-304">Jagged Arrays</span></span>

<span data-ttu-id="79224-305">Массив массива, иногда называемый «массивом массивов», представляет собой массив, элементы которого являются массивами.</span><span class="sxs-lookup"><span data-stu-id="79224-305">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="79224-306">Элементы массива массивов могут иметь разные размеры.</span><span class="sxs-lookup"><span data-stu-id="79224-306">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="79224-307">В следующем примере показано объявление и инициализация массива массивов, представляющего таблицу умножения.</span><span class="sxs-lookup"><span data-stu-id="79224-307">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {
    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```

### <a name="arrays-of-callables"></a><span data-ttu-id="79224-308">Массивы вызываемых элементов</span><span class="sxs-lookup"><span data-stu-id="79224-308">Arrays of callables</span></span> 

<span data-ttu-id="79224-309">Можно также создать массив вызываемых элементов.</span><span class="sxs-lookup"><span data-stu-id="79224-309">You can also create an array of callables.</span></span>

* <span data-ttu-id="79224-310">Если тип общего элемента является операцией или типом функции, все элементы должны иметь одинаковые входные и выходные типы.</span><span class="sxs-lookup"><span data-stu-id="79224-310">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
* <span data-ttu-id="79224-311">Тип элемента массива поддерживает любые [операторов](xref:microsoft.quantum.guide.operationsfunctions) , поддерживаемые всеми элементами.</span><span class="sxs-lookup"><span data-stu-id="79224-311">The element type of the array supports any [functors](xref:microsoft.quantum.guide.operationsfunctions) that are supported by all of the elements.</span></span>
<span data-ttu-id="79224-312">Например, если `Op1` , `Op2` и `Op3` все являются `Qubit[] => Unit` операциями, но `Op1` поддерживают, поддерживают `Adjoint` `Op2` `Controlled` и `Op3` поддерживают оба:</span><span class="sxs-lookup"><span data-stu-id="79224-312">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit` operations, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>
  * <span data-ttu-id="79224-313">`[Op1, Op2]`является массивом `(Qubit[] => Unit)` операций.</span><span class="sxs-lookup"><span data-stu-id="79224-313">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
  * <span data-ttu-id="79224-314">`[Op1, Op3]`является массивом `(Qubit[] => Unit is Adj)` операций.</span><span class="sxs-lookup"><span data-stu-id="79224-314">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
  * <span data-ttu-id="79224-315">`[Op2, Op3]`является массивом `(Qubit[] => Unit is Ctl)` операций.</span><span class="sxs-lookup"><span data-stu-id="79224-315">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="79224-316">Однако, хотя операции `(Qubit[] => Unit is Adj)` и `(Qubit[] => Unit is Ctl)` имеют общий базовый тип `(Qubit[] => Unit)` , *массивы* этих операций не имеют общего базового типа.</span><span class="sxs-lookup"><span data-stu-id="79224-316">However, while the operations `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` have the common base type of `(Qubit[] => Unit)`, *arrays* of these operations do not share a common base type.</span></span>

<span data-ttu-id="79224-317">Например, `[[Op1], [Op2]]` в настоящее время вызовет ошибку, так как пытается создать массив из двух несовместимых типов массивов `(Qubit[] => Unit is Adj)[]` и `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="79224-317">For example, `[[Op1], [Op2]]` would currently raise an error because it attempts to create an array of the two incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>

<span data-ttu-id="79224-318">Дополнительные сведения о вызываемых функциях см. в разделе [вызываемые выражения](#callable-expressions) на этой странице, [операции и функции в Q# ](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="79224-318">For more information on callables, see [Callable expressions](#callable-expressions)  on this page or [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="79224-319">Условные выражения</span><span class="sxs-lookup"><span data-stu-id="79224-319">Conditional Expressions</span></span>

<span data-ttu-id="79224-320">При наличии двух выражений одного типа и логического выражения формируют условное выражение с помощью вопросительного знака, `?` и вертикальной черты `|` .</span><span class="sxs-lookup"><span data-stu-id="79224-320">Given two expressions of the same type and a Boolean expression, form a conditional expression using the question mark, `?`, and the vertical bar `|`.</span></span> <span data-ttu-id="79224-321">`a==b ? c | d`В данном случае значение условного выражения равно, `c` Если `a==b` равно true и `d` если оно имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="79224-321">Given `a==b ? c | d`, the value of the conditional expression is `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="79224-322">Условные выражения с вызываемыми</span><span class="sxs-lookup"><span data-stu-id="79224-322">Conditional expressions with callables</span></span>

<span data-ttu-id="79224-323">Условные выражения могут возвращать операции с одинаковыми входными и выходными данными, но поддерживают разные операторов.</span><span class="sxs-lookup"><span data-stu-id="79224-323">Conditional expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span> <span data-ttu-id="79224-324">В этом случае тип условного выражения является операцией с входными и выходными данными, которые поддерживают любой операторов, поддерживаемый обоими выражениями.</span><span class="sxs-lookup"><span data-stu-id="79224-324">In this case, the type of the conditional expression is an operation with inputs and outputs that support any functors supported by both expressions.</span></span>
<span data-ttu-id="79224-325">Например, если `Op1` , `Op2` , и `Op3` все являются `Qubit[]=>Unit` , но поддерживают, поддерживают `Op1` `Adjoint` `Op2` `Controlled` и `Op3` поддерживают оба:</span><span class="sxs-lookup"><span data-stu-id="79224-325">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="79224-326">`flag ? Op1 | Op2`является `(Qubit[] => Unit)` операцией.</span><span class="sxs-lookup"><span data-stu-id="79224-326">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="79224-327">`flag ? Op1 | Op3`является `(Qubit[] => Unit is Adj)` операцией.</span><span class="sxs-lookup"><span data-stu-id="79224-327">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="79224-328">`flag ? Op2 | Op3`является `(Qubit[] => Unit is Ctl)` операцией.</span><span class="sxs-lookup"><span data-stu-id="79224-328">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="79224-329">Если одно из двух возможных результатов содержит вызов функции или операции, этот вызов выполняется только в том случае, если результатом является значение, которое является значением вызова.</span><span class="sxs-lookup"><span data-stu-id="79224-329">If either of the two possible result expressions include a function or operation call, that call only takes place if that result is the one that is the value of the call.</span></span> <span data-ttu-id="79224-330">Например, `a==b ? C(qs) | D(qs)` Если `a==b` имеет значение true, то `C` вызывается операция, и если это значение равно false, `D` вызывается только операция.</span><span class="sxs-lookup"><span data-stu-id="79224-330">For example, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true, then the `C` operation is invoked, and if it is false then only the `D` operation is invoked.</span></span> <span data-ttu-id="79224-331">Этот подход аналогичен *сокращению* в других языках.</span><span class="sxs-lookup"><span data-stu-id="79224-331">This approach is similar to *short-circuiting* in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="79224-332">Вызываемые выражения</span><span class="sxs-lookup"><span data-stu-id="79224-332">Callable Expressions</span></span>

<span data-ttu-id="79224-333">Вызываемый литерал — это имя операции или функции, определенной в области компиляции.</span><span class="sxs-lookup"><span data-stu-id="79224-333">A callable literal is the name of an operation or function defined in the compilation scope.</span></span> <span data-ttu-id="79224-334">Например, `X` — это литерал операции, который ссылается на стандартную `X` операцию библиотеки и `Message` является литералом функции, который ссылается на стандартную библиотеку `Message` .</span><span class="sxs-lookup"><span data-stu-id="79224-334">For example, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="79224-335">Если операция поддерживает `Adjoint` функтор, то `Adjoint op` это выражение операции.</span><span class="sxs-lookup"><span data-stu-id="79224-335">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="79224-336">Аналогично, если операция поддерживает `Controlled` функтор, то `Controlled op` это выражение операции.</span><span class="sxs-lookup"><span data-stu-id="79224-336">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="79224-337">Дополнительные сведения о типах этих выражений см. в разделе [вызов специализаций операций](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span><span class="sxs-lookup"><span data-stu-id="79224-337">For more information about the types of these expressions, see [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="79224-338">Операторов ( `Adjoint` и `Controlled` ) привязываются более тесно, чем все другие операторы, за исключением оператора Unwrap `!` и индексирования массивов с помощью `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="79224-338">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[ ]`.</span></span>
<span data-ttu-id="79224-339">Таким образом, все приведенные ниже действия являются допустимыми, предполагая, что операции поддерживают используемую операторов:</span><span class="sxs-lookup"><span data-stu-id="79224-339">Thus, the following are all valid, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="79224-340">Вызываемые выражения типа с параметрами</span><span class="sxs-lookup"><span data-stu-id="79224-340">Type-parameterized callable expressions</span></span>

<span data-ttu-id="79224-341">Можно использовать вызываемый литерал в качестве значения, например, чтобы присвоить ему переменную или передать ее другому вызываемому.</span><span class="sxs-lookup"><span data-stu-id="79224-341">You can use a callable literal as a value, for example, to assign it to a variable or pass it to another callable.</span></span> <span data-ttu-id="79224-342">В этом случае, если вызываемый [тип имеет параметры типа](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), необходимо указать параметры в качестве части вызываемого значения.</span><span class="sxs-lookup"><span data-stu-id="79224-342">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), you must provide the parameters as part of the callable value.</span></span>

<span data-ttu-id="79224-343">Вызываемое значение не может иметь неопределенные параметры типа.</span><span class="sxs-lookup"><span data-stu-id="79224-343">A callable value cannot have any unspecified type parameters.</span></span> <span data-ttu-id="79224-344">Например, если `Fun` является функцией с сигнатурой `'T1->Unit` :</span><span class="sxs-lookup"><span data-stu-id="79224-344">For example, if `Fun` is a function with the signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="79224-345">Выражения вызываемого вызова</span><span class="sxs-lookup"><span data-stu-id="79224-345">Callable Invocation Expressions</span></span>

<span data-ttu-id="79224-346">При наличии вызываемого выражения (операции или функции) и кортежного выражения входного типа сигнатуры вызываемого метода можно сформировать *выражение вызова* , добавив выражение кортежа в вызываемое выражение.</span><span class="sxs-lookup"><span data-stu-id="79224-346">Given a callable expression (operation or function) and a tuple expression of the input type of the callable's signature, you can form an *invocation expression* by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="79224-347">Тип выражения вызова является выходным типом сигнатуры вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="79224-347">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="79224-348">Например, если `Op` является операцией с сигнатурой `((Int, Qubit) => Double)` , `Op(3, qubit1)` то является выражением типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="79224-348">For example, if `Op` is an operation with the signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="79224-349">Аналогично, если `Sin` является функцией с сигнатурой `(Double -> Double)` , `Sin(0.1)` является выражением типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="79224-349">Similarly, if `Sin` is a function with the signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="79224-350">Наконец, если `Builder` является функцией с сигнатурой `(Int -> (Int -> Int))` , то `Builder(3)` функция является функцией из `Int` to `Int` .</span><span class="sxs-lookup"><span data-stu-id="79224-350">Finally, if `Builder` is a function with the signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from `Int` to `Int`.</span></span>

<span data-ttu-id="79224-351">Для вызова результата выражения с вызываемым значением требуется еще одна пара круглых скобок вокруг вызываемого выражения.</span><span class="sxs-lookup"><span data-stu-id="79224-351">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="79224-352">Таким образом, чтобы вызвать результат вызова `Builder` из предыдущего абзаца, правильным синтаксисом является:</span><span class="sxs-lookup"><span data-stu-id="79224-352">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="79224-353">При вызове вызываемого [параметризованного типа](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) можно указать фактические параметры типа в угловых скобках `< >` после вызываемого выражения.</span><span class="sxs-lookup"><span data-stu-id="79224-353">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, you can specify the actual type parameters within angle brackets `< >` after the callable expression.</span></span>
<span data-ttu-id="79224-354">Это действие обычно не требуется, так как Q# компилятор выводит фактические типы.</span><span class="sxs-lookup"><span data-stu-id="79224-354">This action is usually unnecessary as the Q# compiler infers the actual types.</span></span>
<span data-ttu-id="79224-355">Однако *он необходим* для [частичного приложения](xref:microsoft.quantum.guide.operationsfunctions#partial-application) , если аргумент с параметризованным типом не указан.</span><span class="sxs-lookup"><span data-stu-id="79224-355">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="79224-356">Он также полезен при передаче операций с разными функтор, которые поддерживаются для вызова.</span><span class="sxs-lookup"><span data-stu-id="79224-356">It is also useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="79224-357">Например, если `Func` имеет сигнатуру и имеет сигнатуру `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` `(Qubit[] => Unit is Adj)` и `Op3` имеет сигнатуру, то `(Qubit[] => Unit)` для вызова `Func` с помощью в `Op1` качестве первого аргумента, `Op2` а также в `Op3` качестве третьей:</span><span class="sxs-lookup"><span data-stu-id="79224-357">For example, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="79224-358">Спецификация типа является обязательной `Op3` , поскольку и `Op1` имеет разные типы, поэтому компилятор будет считать его неоднозначным без спецификации.</span><span class="sxs-lookup"><span data-stu-id="79224-358">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="79224-359">Приоритет операторов</span><span class="sxs-lookup"><span data-stu-id="79224-359">Operator Precedence</span></span>

* <span data-ttu-id="79224-360">Все бинарные операторы являются правой ассоциативными, за исключением `^` .</span><span class="sxs-lookup"><span data-stu-id="79224-360">All binary operators are right-associative, except for `^`.</span></span>

* <span data-ttu-id="79224-361">Квадратные скобки, `[ ]` для среза и индексирования массива перед любым оператором.</span><span class="sxs-lookup"><span data-stu-id="79224-361">Brackets, `[ ]`, for array slicing and indexing, bind before any operator.</span></span>

* <span data-ttu-id="79224-362">Операторов `Adjoint` и `Controlled` BIND после индексирования массива, но перед всеми другими операторами.</span><span class="sxs-lookup"><span data-stu-id="79224-362">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

* <span data-ttu-id="79224-363">Круглые скобки для операции и вызова функции также привязываются перед любым оператором, но после индексирования массива и операторов.</span><span class="sxs-lookup"><span data-stu-id="79224-363">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="79224-364">Q#операторы в порядке приоритета, от самого высокого до самого низкого:</span><span class="sxs-lookup"><span data-stu-id="79224-364">Q# operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="79224-365">Оператор</span><span class="sxs-lookup"><span data-stu-id="79224-365">Operator</span></span> | <span data-ttu-id="79224-366">Арность</span><span class="sxs-lookup"><span data-stu-id="79224-366">Arity</span></span> | <span data-ttu-id="79224-367">Описание:</span><span class="sxs-lookup"><span data-stu-id="79224-367">Description</span></span> | <span data-ttu-id="79224-368">Типы операндов</span><span class="sxs-lookup"><span data-stu-id="79224-368">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="79224-369">конечные`!`</span><span class="sxs-lookup"><span data-stu-id="79224-369">trailing `!`</span></span> | <span data-ttu-id="79224-370">Унарный</span><span class="sxs-lookup"><span data-stu-id="79224-370">Unary</span></span> | <span data-ttu-id="79224-371">разворачивание;</span><span class="sxs-lookup"><span data-stu-id="79224-371">Unwrap</span></span> | <span data-ttu-id="79224-372">Любой определяемый пользователем тип</span><span class="sxs-lookup"><span data-stu-id="79224-372">Any user-defined type</span></span>
 <span data-ttu-id="79224-373">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="79224-373">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="79224-374">Унарный</span><span class="sxs-lookup"><span data-stu-id="79224-374">Unary</span></span> | <span data-ttu-id="79224-375">Числовое отрицательное, побитовое дополнение, логическое отрицание</span><span class="sxs-lookup"><span data-stu-id="79224-375">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="79224-376">`Int`, `BigInt` или `Double` для `-` , `Int` или `BigInt` для `~~~` `Bool` для`not`</span><span class="sxs-lookup"><span data-stu-id="79224-376">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="79224-377">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-377">Binary</span></span> | <span data-ttu-id="79224-378">Целочисленное энергопотребление</span><span class="sxs-lookup"><span data-stu-id="79224-378">Integer power</span></span> | <span data-ttu-id="79224-379">`Int`или `BigInt` для основания, `Int` для показателя степени</span><span class="sxs-lookup"><span data-stu-id="79224-379">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="79224-380">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="79224-380">`/`, `*`, `%`</span></span> | <span data-ttu-id="79224-381">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-381">Binary</span></span> | <span data-ttu-id="79224-382">Деление, умножение, целочисленный модуль</span><span class="sxs-lookup"><span data-stu-id="79224-382">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="79224-383">`Int`, `BigInt` или `Double` для `/` и `*` , `Int` или `BigInt` для`%`</span><span class="sxs-lookup"><span data-stu-id="79224-383">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="79224-384">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="79224-384">`+`, `-`</span></span> | <span data-ttu-id="79224-385">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-385">Binary</span></span> | <span data-ttu-id="79224-386">Сложение или объединение строк и массивов, вычитание</span><span class="sxs-lookup"><span data-stu-id="79224-386">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="79224-387">`Int`, `BigInt` или `Double` , Кроме того, `String` или любого типа массива для`+`</span><span class="sxs-lookup"><span data-stu-id="79224-387">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="79224-388">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="79224-388">`<<<`, `>>>`</span></span> | <span data-ttu-id="79224-389">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-389">Binary</span></span> | <span data-ttu-id="79224-390">Сдвиг влево, сдвиг вправо</span><span class="sxs-lookup"><span data-stu-id="79224-390">Left shift, right shift</span></span> | <span data-ttu-id="79224-391">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="79224-391">`Int` or `BigInt`</span></span>
 <span data-ttu-id="79224-392">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="79224-392">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="79224-393">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-393">Binary</span></span> | <span data-ttu-id="79224-394">Сравнения "меньше чем", "меньше или равно", "больше чем", "больше или равно"</span><span class="sxs-lookup"><span data-stu-id="79224-394">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="79224-395">`Int`, `BigInt` или`Double`</span><span class="sxs-lookup"><span data-stu-id="79224-395">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="79224-396">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="79224-396">`==`, `!=`</span></span> | <span data-ttu-id="79224-397">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-397">Binary</span></span> | <span data-ttu-id="79224-398">сравнения «равно» и «не равно»</span><span class="sxs-lookup"><span data-stu-id="79224-398">equal, not-equal comparisons</span></span> | <span data-ttu-id="79224-399">любой тип-примитив</span><span class="sxs-lookup"><span data-stu-id="79224-399">any primitive type</span></span>
 `&&&` | <span data-ttu-id="79224-400">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-400">Binary</span></span> | <span data-ttu-id="79224-401">Побитовое И</span><span class="sxs-lookup"><span data-stu-id="79224-401">Bitwise AND</span></span> | <span data-ttu-id="79224-402">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="79224-402">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="79224-403">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-403">Binary</span></span> | <span data-ttu-id="79224-404">Побитовое исключающее ИЛИ</span><span class="sxs-lookup"><span data-stu-id="79224-404">Bitwise XOR</span></span> | <span data-ttu-id="79224-405">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="79224-405">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="79224-406">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-406">Binary</span></span> | <span data-ttu-id="79224-407">Побитовое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="79224-407">Bitwise OR</span></span> | <span data-ttu-id="79224-408">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="79224-408">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="79224-409">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-409">Binary</span></span> | <span data-ttu-id="79224-410">Логическое И</span><span class="sxs-lookup"><span data-stu-id="79224-410">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="79224-411">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="79224-411">Binary</span></span> | <span data-ttu-id="79224-412">Логическое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="79224-412">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="79224-413">Двоичный/Ternary</span><span class="sxs-lookup"><span data-stu-id="79224-413">Binary/Ternary</span></span> | <span data-ttu-id="79224-414">Оператор Range</span><span class="sxs-lookup"><span data-stu-id="79224-414">Range operator</span></span> | `Int`
 <span data-ttu-id="79224-415">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="79224-415">`?` `|`</span></span> | <span data-ttu-id="79224-416">Ternary</span><span class="sxs-lookup"><span data-stu-id="79224-416">Ternary</span></span> | <span data-ttu-id="79224-417">Условная логика</span><span class="sxs-lookup"><span data-stu-id="79224-417">Conditional</span></span> | <span data-ttu-id="79224-418">`Bool`для левой стороны</span><span class="sxs-lookup"><span data-stu-id="79224-418">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="79224-419">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="79224-419">`w/` `<-`</span></span> | <span data-ttu-id="79224-420">Ternary</span><span class="sxs-lookup"><span data-stu-id="79224-420">Ternary</span></span> | <span data-ttu-id="79224-421">Копирование и обновление</span><span class="sxs-lookup"><span data-stu-id="79224-421">Copy-and-update</span></span> | <span data-ttu-id="79224-422">См. раздел [выражения копирования и обновления](#copy-and-update-expressions) .</span><span class="sxs-lookup"><span data-stu-id="79224-422">See [Copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="79224-423">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="79224-423">Next steps</span></span>

<span data-ttu-id="79224-424">Теперь, когда вы можете работать с выражениями в Q# , переходите к [операциям Q# и функциям в](xref:microsoft.quantum.guide.operationsfunctions) , чтобы научиться определять и вызывать операции и функции.</span><span class="sxs-lookup"><span data-stu-id="79224-424">Now that you can work with expressions in Q#, move on to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
