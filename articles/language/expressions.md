---
title: 'Выражения Q #'
description: 'Узнайте, как указывать, ссылаться и объединять константы, переменные, операторы, операции и функции в качестве выражений в Q #.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 095be52af27f827f3e52d39a70702f50d6d59ee8
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683926"
---
# <a name="expressions"></a><span data-ttu-id="654b7-103">Выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-103">Expressions</span></span>

## <a name="grouping"></a><span data-ttu-id="654b7-104">Группирование</span><span class="sxs-lookup"><span data-stu-id="654b7-104">Grouping</span></span>

<span data-ttu-id="654b7-105">При наличии любого выражения такое же выражение, заключенное в круглые скобки, является выражением того же типа.</span><span class="sxs-lookup"><span data-stu-id="654b7-105">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="654b7-106">`(7)` Например, `Int` является выражением, `([1,2,3])` является выражением типа массива `Int`s и `((1,2))` является выражением с типом. `(Int, Int)`</span><span class="sxs-lookup"><span data-stu-id="654b7-106">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="654b7-107">Эквивалентность простых значений и кортежей с одним элементом, описанных в [модели типов](xref:microsoft.quantum.language.type-model#tuple-types) , устраняет неоднозначность между `(6)` как группой и `(6)` кортежем с одним элементом.</span><span class="sxs-lookup"><span data-stu-id="654b7-107">The equivalence between simple values and single-element tuples described in [the type model](xref:microsoft.quantum.language.type-model#tuple-types) removes the ambiguity between `(6)` as a group and `(6)` as a single-element tuple.</span></span>

## <a name="symbols"></a><span data-ttu-id="654b7-108">Символы</span><span class="sxs-lookup"><span data-stu-id="654b7-108">Symbols</span></span>

<span data-ttu-id="654b7-109">Имя символа, привязанного к значению типа `'T` или присваиваемое ему, является выражением типа `'T`.</span><span class="sxs-lookup"><span data-stu-id="654b7-109">The name of a symbol bound or assigned to a value of type `'T` is an expression of type `'T`.</span></span>
<span data-ttu-id="654b7-110">Например, если символ `count` привязан к целому значению `5`, то `count` является целочисленным выражением.</span><span class="sxs-lookup"><span data-stu-id="654b7-110">For instance, if the symbol `count` is bound to the integer value `5`, then `count` is an integer expression.</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="654b7-111">Числовые выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-111">Numeric Expressions</span></span>

<span data-ttu-id="654b7-112">Числовые выражения — это выражения `Int`типа `BigInt`, или `Double`.</span><span class="sxs-lookup"><span data-stu-id="654b7-112">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="654b7-113">То есть это либо целочисленное, либо числовое число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="654b7-113">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="654b7-114">`Int`литералы в Q # идентичны целочисленным литералам в C#, за исключением того, что конечные знаки "l" и "L" не являются обязательными (или не разрешены).</span><span class="sxs-lookup"><span data-stu-id="654b7-114">`Int` literals in Q# are identical to integer literals in C#, except that no trailing "l" or "L" is required (or allowed).</span></span>
<span data-ttu-id="654b7-115">Шестнадцатеричные и двоичные целые числа поддерживаются с префиксом "0x" и "0b" соответственно.</span><span class="sxs-lookup"><span data-stu-id="654b7-115">Hexadecimal and binary integers are supported with a "0x" and "0b" prefix respectively.</span></span>

<span data-ttu-id="654b7-116">`BigInt`литералы в Q # идентичны строкам больших целых чисел в .NET с завершающим "l" или "L".</span><span class="sxs-lookup"><span data-stu-id="654b7-116">`BigInt` literals in Q# are identical to big integer strings in .NET, with a trailing "l" or "L".</span></span>
<span data-ttu-id="654b7-117">Шестнадцатеричные большие целые числа поддерживаются с префиксом "0x".</span><span class="sxs-lookup"><span data-stu-id="654b7-117">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="654b7-118">Таким образом, все следующие допустимые варианты использования `BigInt` литералов:</span><span class="sxs-lookup"><span data-stu-id="654b7-118">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="654b7-119">`Double`литералы в Q # идентичны двойным литералам в C#, за исключением того, что завершающие "d" или "D" не являются обязательными (или не разрешены).</span><span class="sxs-lookup"><span data-stu-id="654b7-119">`Double` literals in Q# are identical to double literals in C#, except that no trailing "d" or "D" is required (or allowed).</span></span>

<span data-ttu-id="654b7-120">При наличии выражения массива `Int` любого типа элементов выражение может быть сформировано с помощью `Length` встроенной функции с выражением массива, заключенным в круглые скобки, `(` и. `)`</span><span class="sxs-lookup"><span data-stu-id="654b7-120">Given an array expression of any element type, an `Int` expression may be formed using the `Length` built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="654b7-121">Например, если `a` привязан к массиву, то `Length(a)` является целочисленным выражением.</span><span class="sxs-lookup"><span data-stu-id="654b7-121">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="654b7-122">Если `b` является массивом массивов целых `Int[][]`чисел, то `Length(b)` — число подмассивов в `b`, а `Length(b[1])` — число целых чисел во втором подмассиве в. `b`</span><span class="sxs-lookup"><span data-stu-id="654b7-122">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="654b7-123">При наличии двух числовых выражений одного `+`типа бинарные операторы `-` `*`,, и `/` могут использоваться для формирования нового числового выражения.</span><span class="sxs-lookup"><span data-stu-id="654b7-123">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="654b7-124">Тип нового выражения будет таким же, как и типы составных выражений.</span><span class="sxs-lookup"><span data-stu-id="654b7-124">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="654b7-125">При наличии двух целочисленных выражений бинарный `^` оператор (Power) может использоваться для формирования нового целочисленного выражения.</span><span class="sxs-lookup"><span data-stu-id="654b7-125">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="654b7-126">Аналогичным `^` образом для формирования нового двойного выражения можно использовать два выражения типа Double.</span><span class="sxs-lookup"><span data-stu-id="654b7-126">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="654b7-127">Наконец, `^` можно использовать с большим целым числом слева и целым числом справа для формирования нового выражения больших целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="654b7-127">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="654b7-128">В этом случае второй параметр должен соответствовать 32 бит; Если нет, возникнет ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="654b7-128">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="654b7-129">При наличии двух целочисленных или больших целочисленных выражений можно формировать новое целочисленное или большое целочисленное выражение `%` с помощью операторов ( `&&&` модуль), (побитовое и), `|||` ( `^^^` побитовое или) или (побитовое исключающее).</span><span class="sxs-lookup"><span data-stu-id="654b7-129">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="654b7-130">При наличии целочисленного или длинного целочисленного выражения слева, а также целочисленного выражения справа можно использовать операторы `<<<` (арифметические сдвиги влево `>>>` ) или (арифметические сдвиги вправо) для создания нового выражения с тем же типом, что и у левого выражения.</span><span class="sxs-lookup"><span data-stu-id="654b7-130">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="654b7-131">Второй параметр (сумма сдвига) для операции сдвига должен быть больше или равен нулю; поведение для отрицательных сумм сдвига не определено.</span><span class="sxs-lookup"><span data-stu-id="654b7-131">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="654b7-132">Сумма сдвига для операции сдвига также должна соответствовать 32 бит; Если нет, возникнет ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="654b7-132">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="654b7-133">Если число, которое необходимо сдвинуть, является целым числом, то величина сдвига интерпретируется `mod 64`; то есть сдвиг 1 и сдвиг 65 имеют одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="654b7-133">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="654b7-134">Для целочисленных и больших целочисленных значений сдвиги являются арифметическими.</span><span class="sxs-lookup"><span data-stu-id="654b7-134">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="654b7-135">Сдвиг отрицательного значения влево или вправо приведет к отрицательному числу.</span><span class="sxs-lookup"><span data-stu-id="654b7-135">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="654b7-136">Это значит, что сдвиг на один шаг влево или вправо точно так же, как умножение или деление на 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="654b7-136">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="654b7-137">Целочисленный разделитель и модуль целых чисел соответствуют тому же поведению для отрицательных чисел, что и в C#.</span><span class="sxs-lookup"><span data-stu-id="654b7-137">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="654b7-138">То есть всегда `a % b` будет иметь тот же знак, что `a`и, `b * (a / b) + a % b` и всегда будет `a`равно.</span><span class="sxs-lookup"><span data-stu-id="654b7-138">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="654b7-139">Пример:</span><span class="sxs-lookup"><span data-stu-id="654b7-139">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="654b7-140">5</span><span class="sxs-lookup"><span data-stu-id="654b7-140">5</span></span> | <span data-ttu-id="654b7-141">2</span><span class="sxs-lookup"><span data-stu-id="654b7-141">2</span></span> | <span data-ttu-id="654b7-142">2</span><span class="sxs-lookup"><span data-stu-id="654b7-142">2</span></span> | <span data-ttu-id="654b7-143">1</span><span class="sxs-lookup"><span data-stu-id="654b7-143">1</span></span>
 <span data-ttu-id="654b7-144">5</span><span class="sxs-lookup"><span data-stu-id="654b7-144">5</span></span> | <span data-ttu-id="654b7-145">-2</span><span class="sxs-lookup"><span data-stu-id="654b7-145">-2</span></span> | <span data-ttu-id="654b7-146">-2</span><span class="sxs-lookup"><span data-stu-id="654b7-146">-2</span></span> | <span data-ttu-id="654b7-147">1</span><span class="sxs-lookup"><span data-stu-id="654b7-147">1</span></span>
 <span data-ttu-id="654b7-148">-5</span><span class="sxs-lookup"><span data-stu-id="654b7-148">-5</span></span> | <span data-ttu-id="654b7-149">2</span><span class="sxs-lookup"><span data-stu-id="654b7-149">2</span></span> | <span data-ttu-id="654b7-150">-2</span><span class="sxs-lookup"><span data-stu-id="654b7-150">-2</span></span> | <span data-ttu-id="654b7-151">-1</span><span class="sxs-lookup"><span data-stu-id="654b7-151">-1</span></span>
 <span data-ttu-id="654b7-152">-5</span><span class="sxs-lookup"><span data-stu-id="654b7-152">-5</span></span> | <span data-ttu-id="654b7-153">-2</span><span class="sxs-lookup"><span data-stu-id="654b7-153">-2</span></span> | <span data-ttu-id="654b7-154">2</span><span class="sxs-lookup"><span data-stu-id="654b7-154">2</span></span> | <span data-ttu-id="654b7-155">-1</span><span class="sxs-lookup"><span data-stu-id="654b7-155">-1</span></span>

<span data-ttu-id="654b7-156">Подразделение больших целых чисел и модуль работают одинаково.</span><span class="sxs-lookup"><span data-stu-id="654b7-156">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="654b7-157">При наличии любого числового выражения новое выражение может быть сформировано с `-` помощью унарного оператора.</span><span class="sxs-lookup"><span data-stu-id="654b7-157">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="654b7-158">Новое выражение будет иметь тот же тип, что и составное выражение.</span><span class="sxs-lookup"><span data-stu-id="654b7-158">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="654b7-159">При наличии целочисленного или длинного целочисленного выражения новое выражение того же типа может быть сформировано с `~~~` помощью унарного оператора (побитовое дополнение).</span><span class="sxs-lookup"><span data-stu-id="654b7-159">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="654b7-160">Логические выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-160">Boolean Expressions</span></span>

<span data-ttu-id="654b7-161">Двумя `Bool` литеральными значениями являются `true` и `false`.</span><span class="sxs-lookup"><span data-stu-id="654b7-161">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="654b7-162">При наличии двух выражений одного и того же примитивного типа `==` для `!=` создания `Bool` выражения можно использовать бинарные операторы и.</span><span class="sxs-lookup"><span data-stu-id="654b7-162">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="654b7-163">Выражение будет иметь значение true, если два выражения равны, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="654b7-163">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="654b7-164">Значения определяемых пользователем типов могут не сравниваться, можно сравнивать только их неупакованные значения.</span><span class="sxs-lookup"><span data-stu-id="654b7-164">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="654b7-165">Например, с помощью оператора `!` "Распаковка" (см. описание на [странице "модель типов Q #](xref:microsoft.quantum.language.type-model#user-defined-types)").</span><span class="sxs-lookup"><span data-stu-id="654b7-165">For example, using the "unwrap" operator `!` (explained in the [Q# type model page](xref:microsoft.quantum.language.type-model#user-defined-types)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="654b7-166">Сравнение на равенство для `Qubit` значений — равенство идентификаторов; то есть, определяет, совпадают ли два выражения одинаковым кубит.</span><span class="sxs-lookup"><span data-stu-id="654b7-166">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="654b7-167">Состояние двух Кубитс не сравнивается, обращается, измеряется или изменяется с помощью этого сравнения.</span><span class="sxs-lookup"><span data-stu-id="654b7-167">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="654b7-168">Сравнение значений на `Double` равенство может привести к неверному результату из-за эффектов округления.</span><span class="sxs-lookup"><span data-stu-id="654b7-168">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="654b7-169">Например, `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="654b7-169">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="654b7-170">При наличии двух числовых `>`выражений бинарные операторы `<` `>=`,, и `<=` могут использоваться для создания нового логического выражения, которое имеет значение true, если первое выражение соответственно больше, меньше, больше или равно или меньше или равно второму выражению.</span><span class="sxs-lookup"><span data-stu-id="654b7-170">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="654b7-171">При наличии двух логических выражений бинарные `and` операторы `or` и можно использовать для создания нового логического выражения, которое имеет значение true, если оба выражения (отв. оба или оба) имеют значение true.</span><span class="sxs-lookup"><span data-stu-id="654b7-171">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="654b7-172">При наличии любого логического выражения `not` унарный оператор может использоваться для создания нового логического выражения, которое имеет значение true, если составное выражение имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="654b7-172">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="654b7-173">Строковые выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-173">String Expressions</span></span>

<span data-ttu-id="654b7-174">Q # позволяет использовать строки в `fail` операторе и `Log` стандартной функции.</span><span class="sxs-lookup"><span data-stu-id="654b7-174">Q# allows strings to be used in the `fail` statement and the `Log` standard function.</span></span>

<span data-ttu-id="654b7-175">Строки в Q # — это литералы или интерполяции строк.</span><span class="sxs-lookup"><span data-stu-id="654b7-175">Strings in Q# are either literals or interpolated strings.</span></span>
<span data-ttu-id="654b7-176">Строковые литералы похожи на простые строковые литералы в большинстве языков: последовательность символов Юникода, `"`заключенная в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="654b7-176">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="654b7-177">Внутри строки `\` символ обратной косой черты может использоваться для экранирования символа двойной кавычки, а также для вставки новой строки `\n`как, возврата каретки в виде `\r`и табуляции как. `\t`</span><span class="sxs-lookup"><span data-stu-id="654b7-177">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="654b7-178">например</span><span class="sxs-lookup"><span data-stu-id="654b7-178">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```

<span data-ttu-id="654b7-179">Синтаксис Q # для интерполяции строк представляет собой подмножество синтаксиса C# 7,0. Q # не поддерживает буквальные строки с интерполяцией (многострочные).</span><span class="sxs-lookup"><span data-stu-id="654b7-179">The Q# syntax for string interpolations is a subset of the C# 7.0 syntax; Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="654b7-180">Синтаксис C# см. в разделе [*интерполяция строк*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) .</span><span class="sxs-lookup"><span data-stu-id="654b7-180">See [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) for the C# syntax.</span></span>

<span data-ttu-id="654b7-181">Выражения внутри строки с интерполяцией следуют синтаксису Q #, а не синтаксису C#.</span><span class="sxs-lookup"><span data-stu-id="654b7-181">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>
<span data-ttu-id="654b7-182">Любое допустимое выражение Q # может присутствовать в интерполяции строки.</span><span class="sxs-lookup"><span data-stu-id="654b7-182">Any valid Q# expression may appear in an interpolated string.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="654b7-183">Выражения кубит</span><span class="sxs-lookup"><span data-stu-id="654b7-183">Qubit Expressions</span></span>

<span data-ttu-id="654b7-184">Единственными `Qubit` выражениями являются символы, привязанные `Qubit` к значениям или элементам `Qubit` массива массивов.</span><span class="sxs-lookup"><span data-stu-id="654b7-184">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="654b7-185">Литералы отсутствуют `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="654b7-185">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="654b7-186">Выражения Паули</span><span class="sxs-lookup"><span data-stu-id="654b7-186">Pauli Expressions</span></span>

<span data-ttu-id="654b7-187">Все четыре `Pauli` значения, `PauliI` `PauliX` `PauliY`,, и `PauliZ`, являются допустимыми `Pauli` выражениями.</span><span class="sxs-lookup"><span data-stu-id="654b7-187">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="654b7-188">Кроме того, единственными `Pauli` выражениями являются символы, привязанные к `Pauli` значениям или элементам массива `Pauli` массивов.</span><span class="sxs-lookup"><span data-stu-id="654b7-188">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="654b7-189">Выражения результатов</span><span class="sxs-lookup"><span data-stu-id="654b7-189">Result Expressions</span></span>

<span data-ttu-id="654b7-190">Два `Result` значения, `One` и `Zero`, являются допустимыми `Result` выражениями.</span><span class="sxs-lookup"><span data-stu-id="654b7-190">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="654b7-191">Кроме того, единственными `Result` выражениями являются символы, привязанные к `Result` значениям или элементам массива `Result` массивов.</span><span class="sxs-lookup"><span data-stu-id="654b7-191">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="654b7-192">В частности, обратите `One` внимание, что не совпадает с целым `1`числом и прямое преобразование между ними отсутствует.</span><span class="sxs-lookup"><span data-stu-id="654b7-192">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="654b7-193">Это справедливо и для `Zero` и. `0`</span><span class="sxs-lookup"><span data-stu-id="654b7-193">The same is true for `Zero` and `0`.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="654b7-194">Выражения диапазона</span><span class="sxs-lookup"><span data-stu-id="654b7-194">Range Expressions</span></span>

<span data-ttu-id="654b7-195">Учитывая все три `Int` выражения `start`, `step`, и `stop`, `start .. step .. stop` — это выражение диапазона, первый элемент которого `start`имеет значение, второй `start+step`элемент —, третий `start+step+step`элемент — и т. `stop` д., пока не будет передан.</span><span class="sxs-lookup"><span data-stu-id="654b7-195">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="654b7-196">Диапазон может быть пустым, если, например, `step` положительным и. `stop < start`</span><span class="sxs-lookup"><span data-stu-id="654b7-196">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="654b7-197">Последний элемент `stop` в диапазоне будет иметь значение, если разница между `start` и `stop` является целым числом `step`, кратным. Это значит, что диапазон является инклюзивным на обоих концах.</span><span class="sxs-lookup"><span data-stu-id="654b7-197">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="654b7-198">`start .. stop` При `start .. 1 .. stop`наличии двух `Int` выражений `start` и `stop`является выражением диапазона, равным.</span><span class="sxs-lookup"><span data-stu-id="654b7-198">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="654b7-199">Обратите внимание, `step` что подразумеваемым является + `stop` 1, даже `start`если меньше; в этом случае диапазон пуст.</span><span class="sxs-lookup"><span data-stu-id="654b7-199">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="654b7-200">Ниже приведены некоторые примеры диапазонов.</span><span class="sxs-lookup"><span data-stu-id="654b7-200">Some example ranges are:</span></span>

- <span data-ttu-id="654b7-201">`1..3`диапазон значений 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="654b7-201">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="654b7-202">`2..2..5`диапазон 2, 4.</span><span class="sxs-lookup"><span data-stu-id="654b7-202">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="654b7-203">`2..2..6`— диапазон 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="654b7-203">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="654b7-204">`6..-2..2`— диапазон 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="654b7-204">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="654b7-205">`2..1`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="654b7-205">`2..1` is the empty range.</span></span>
- <span data-ttu-id="654b7-206">`2..6..7`— диапазон 2.</span><span class="sxs-lookup"><span data-stu-id="654b7-206">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="654b7-207">`2..2..1`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="654b7-207">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="654b7-208">`1..-1..2`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="654b7-208">`1..-1..2` is the empty range.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="654b7-209">Вызываемые выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-209">Callable Expressions</span></span>

<span data-ttu-id="654b7-210">Вызываемый литерал — это имя операции или функции, определенной в области компиляции.</span><span class="sxs-lookup"><span data-stu-id="654b7-210">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="654b7-211">Например, `X` — это литерал операции, который ссылается на стандартную операцию `X` библиотеки и `Message` является литералом функции, который ссылается на стандартную библиотеку `Message` .</span><span class="sxs-lookup"><span data-stu-id="654b7-211">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="654b7-212">Если операция поддерживает `Adjoint` функтор, то `Adjoint op` это выражение операции.</span><span class="sxs-lookup"><span data-stu-id="654b7-212">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="654b7-213">Аналогично, если операция поддерживает `Controlled` функтор, то `Controlled op` это выражение операции.</span><span class="sxs-lookup"><span data-stu-id="654b7-213">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="654b7-214">Типы этих выражений указываются в [операторов](xref:microsoft.quantum.language.type-model#functors).</span><span class="sxs-lookup"><span data-stu-id="654b7-214">The types of these expressions are specified in [Functors](xref:microsoft.quantum.language.type-model#functors).</span></span>

<span data-ttu-id="654b7-215">Операторов (`Adjoint` и `Controlled`) привязываются более тесно, чем все другие операторы, за исключением `!` оператора Unwrap и `[]`индексирования массивов с помощью.</span><span class="sxs-lookup"><span data-stu-id="654b7-215">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[]`.</span></span>
<span data-ttu-id="654b7-216">Таким образом, все следующие юридические, предполагая, что операции поддерживают операторов.</span><span class="sxs-lookup"><span data-stu-id="654b7-216">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

<span data-ttu-id="654b7-217">В качестве значения можно использовать вызываемый литерал, например, чтобы присвоить значение переменной или передать другому вызываемому.</span><span class="sxs-lookup"><span data-stu-id="654b7-217">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="654b7-218">В этом случае, если вызываемый тип имеет параметры типа, они должны быть предоставлены как часть вызываемого значения.</span><span class="sxs-lookup"><span data-stu-id="654b7-218">In this case, if the callable has type parameters, they must be provided as part of the callable value.</span></span>
<span data-ttu-id="654b7-219">Вызываемое значение не может иметь неопределенные параметры типа.</span><span class="sxs-lookup"><span data-stu-id="654b7-219">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="654b7-220">Например, если `Fun` является функцией с сигнатурой `'T1->Unit`:</span><span class="sxs-lookup"><span data-stu-id="654b7-220">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomeOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="654b7-221">Выражения вызываемого вызова</span><span class="sxs-lookup"><span data-stu-id="654b7-221">Callable Invocation Expressions</span></span>

<span data-ttu-id="654b7-222">При наличии вызываемого выражения (операции или функции) и кортежного выражения входного типа сигнатуры вызываемого метода выражение вызова может быть сформировано путем добавления кортежного выражения к вызываемому выражению.</span><span class="sxs-lookup"><span data-stu-id="654b7-222">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="654b7-223">Тип выражения вызова является выходным типом сигнатуры вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="654b7-223">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="654b7-224">Например `Op` , если является операцией с сигнатурой `((Int, Qubit) => Double)`, `Op(3, qubit1)` является выражением типа `Double`.</span><span class="sxs-lookup"><span data-stu-id="654b7-224">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="654b7-225">Аналогично, `Sin` если является функцией с `(Double -> Double)`сигнатурой `Sin(0.1)` , является выражением типа `Double`.</span><span class="sxs-lookup"><span data-stu-id="654b7-225">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="654b7-226">Наконец, если `Builder` является функцией с сигнатурой `(Int -> (Int -> Int))`, `Builder(3)` функция преобразуется в тип в int.</span><span class="sxs-lookup"><span data-stu-id="654b7-226">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="654b7-227">Для вызова результата выражения с вызываемым значением требуется еще одна пара круглых скобок вокруг вызываемого выражения.</span><span class="sxs-lookup"><span data-stu-id="654b7-227">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="654b7-228">Таким образом, чтобы вызвать результат вызова `Builder` из предыдущего абзаца, правильным синтаксисом является:</span><span class="sxs-lookup"><span data-stu-id="654b7-228">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="654b7-229">При вызове вызываемого типа с параметрами, фактические параметры типа могут быть указаны в угловых `<` скобках и `>` после вызываемого выражения.</span><span class="sxs-lookup"><span data-stu-id="654b7-229">When invoking a type-parameterized callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="654b7-230">Обычно это не требуется, так как компилятор Q # будет вычислять фактические типы.</span><span class="sxs-lookup"><span data-stu-id="654b7-230">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="654b7-231">Он необходим для частичного применения (см. ниже), если аргумент с параметризованным типом не указан.</span><span class="sxs-lookup"><span data-stu-id="654b7-231">It is required for partial application (see below) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="654b7-232">Кроме того, она иногда полезна при передаче операций с разными функтор, которые поддерживаются для вызова.</span><span class="sxs-lookup"><span data-stu-id="654b7-232">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="654b7-233">`Func` Например, если имеет сигнатуру `('T1, 'T2, 'T1) -> 'T2` `Op1` и `Op2` `(Qubit[] => Unit is Adj)`имеет сигнатуру и `Op3` имеет `(Qubit[] => Unit)`сигнатуру, то для `Func` вызова `Op1` с помощью в качестве первого `Op2` аргумента, а `Op3` также в качестве третьей:</span><span class="sxs-lookup"><span data-stu-id="654b7-233">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="654b7-234">Спецификация типа является обязательной, `Op3` поскольку `Op1` и имеет разные типы, поэтому компилятор будет считать его неоднозначным без спецификации.</span><span class="sxs-lookup"><span data-stu-id="654b7-234">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>

### <a name="partial-application"></a><span data-ttu-id="654b7-235">Частичное приложение</span><span class="sxs-lookup"><span data-stu-id="654b7-235">Partial Application</span></span>

<span data-ttu-id="654b7-236">При наличии вызываемого выражения можно создать новый вызываемый объект, предоставив подмножество аргументов вызываемому.</span><span class="sxs-lookup"><span data-stu-id="654b7-236">Given a callable expression, a new callable may be created by providing a subset of the arguments to the callable.</span></span>
<span data-ttu-id="654b7-237">Это называется _частичным приложением_.</span><span class="sxs-lookup"><span data-stu-id="654b7-237">This is called _partial application_.</span></span>

<span data-ttu-id="654b7-238">В Q # частично примененный вызываемый объект выражается путем написания обычного выражения вызова, но с использованием символа подчеркивания `_`для неуказанных аргументов.</span><span class="sxs-lookup"><span data-stu-id="654b7-238">In Q#, a partially applied callable is expressed by writing a normal invocation expression, but using an underscore, `_`, for the unspecified arguments.</span></span>
<span data-ttu-id="654b7-239">Результирующий вызываемый объект имеет тот же тип результата, что и базовый вызываемый, и те же специализации для операций.</span><span class="sxs-lookup"><span data-stu-id="654b7-239">The resulting callable has the same result type as the base callable, and the same specializations for operations.</span></span>
<span data-ttu-id="654b7-240">Тип входных данных частичного приложения — это просто исходный тип с удаленными указанными аргументами.</span><span class="sxs-lookup"><span data-stu-id="654b7-240">The input type of the partial application is simply the original type with the specified arguments removed.</span></span>

<span data-ttu-id="654b7-241">Если изменяемая переменная передается в качестве указанного аргумента при создании частичного приложения, используется текущее значение переменной.</span><span class="sxs-lookup"><span data-stu-id="654b7-241">If a mutable variable is passed as a specified argument when creating a partial application, the current value of the variable is used.</span></span>
<span data-ttu-id="654b7-242">Изменение значения переменной после этого не влияет на часть приложения.</span><span class="sxs-lookup"><span data-stu-id="654b7-242">Changing the value of the variable afterward will not impact the partial application.</span></span>

<span data-ttu-id="654b7-243">Например, если `Op` имеет тип `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`:</span><span class="sxs-lookup"><span data-stu-id="654b7-243">For example, if `Op` has type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`:</span></span>

- <span data-ttu-id="654b7-244">`Op(5,(_,_))`имеет тип `(((Qubit,Qubit), Double) => Unit is Adj)`и т `Op(5,_)`. д.</span><span class="sxs-lookup"><span data-stu-id="654b7-244">`Op(5,(_,_))` has type `(((Qubit,Qubit), Double) => Unit is Adj)`, and so has `Op(5,_)`.</span></span>
- <span data-ttu-id="654b7-245">`Op(_,(_,1.0))` имеет тип `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="654b7-245">`Op(_,(_,1.0))` has type `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span></span>
- <span data-ttu-id="654b7-246">`Op(_,((q1,q2),_))` имеет тип `((Int,Double) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="654b7-246">`Op(_,((q1,q2),_))` has type `((Int,Double) => Unit is Adj)`.</span></span>
   <span data-ttu-id="654b7-247">Обратите внимание, что здесь применяется эквивалентность одноэлементного кортежа.</span><span class="sxs-lookup"><span data-stu-id="654b7-247">Note that we have applied singleton tuple equivalence here.</span></span>

<span data-ttu-id="654b7-248">Если частично применяемый тип вызываемого метода имеет параметры типа, которые не могут быть определены компилятором, они должны быть предоставлены на сайте вызова.</span><span class="sxs-lookup"><span data-stu-id="654b7-248">If the partially-applied callable has type parameters that cannot be inferred by the compiler, they must be provided at the invocation site.</span></span>
<span data-ttu-id="654b7-249">Часть приложения не может иметь неопределенные параметры типа.</span><span class="sxs-lookup"><span data-stu-id="654b7-249">The partial application cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="654b7-250">Например, если `Op` имеет тип `(('T1, Qubit, 'T1) => Unit : Adjoint)`:</span><span class="sxs-lookup"><span data-stu-id="654b7-250">For example, if `Op` has type `(('T1, Qubit, 'T1) => Unit : Adjoint)`:</span></span>

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a><span data-ttu-id="654b7-251">Рекурсия</span><span class="sxs-lookup"><span data-stu-id="654b7-251">Recursion</span></span>

<span data-ttu-id="654b7-252">Возможность вызовов Q # может быть прямо или косвенно рекурсивной.</span><span class="sxs-lookup"><span data-stu-id="654b7-252">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="654b7-253">Это значит, что операция или функция может вызвать саму себя или вызвать другой вызываемый метод, который напрямую или косвенно вызывает вызываемую операцию.</span><span class="sxs-lookup"><span data-stu-id="654b7-253">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="654b7-254">Однако существует два важных комментария об использовании рекурсии.</span><span class="sxs-lookup"><span data-stu-id="654b7-254">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="654b7-255">Использование рекурсии в операциях, скорее всего, мешает некоторым оптимизациям.</span><span class="sxs-lookup"><span data-stu-id="654b7-255">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="654b7-256">Это может оказать значительное влияние на время выполнения алгоритма.</span><span class="sxs-lookup"><span data-stu-id="654b7-256">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="654b7-257">При выполнении на фактическом устройстве-такте пространство стека может быть ограничено, так что глубокая рекурсия может привести к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="654b7-257">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="654b7-258">В частности, компилятор Q # и среда выполнения не выявляет и не оптимизируют заключительную рекурсию.</span><span class="sxs-lookup"><span data-stu-id="654b7-258">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="654b7-259">Кортежные выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-259">Tuple Expressions</span></span>

<span data-ttu-id="654b7-260">Литерал кортежа — это последовательность выражений элементов соответствующего типа, разделенных запятыми, заключенная в `(` и. `)`</span><span class="sxs-lookup"><span data-stu-id="654b7-260">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="654b7-261">Например, `(1, One)` является `(Int, Result)` выражением.</span><span class="sxs-lookup"><span data-stu-id="654b7-261">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="654b7-262">Кроме литералов, единственными кортежными выражениями являются символы, привязанные к значениям кортежа, элементы массива кортежей и вызываемые вызовы, возвращающие кортежи.</span><span class="sxs-lookup"><span data-stu-id="654b7-262">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="654b7-263">Выражения определяемого пользователем типа</span><span class="sxs-lookup"><span data-stu-id="654b7-263">User-Defined Type Expressions</span></span>

<span data-ttu-id="654b7-264">Литерал определяемого пользователем типа состоит из имени типа, за которым следует литерал кортежа базового типа кортежа типа.</span><span class="sxs-lookup"><span data-stu-id="654b7-264">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="654b7-265">Например, если `IntPair` является определяемым пользователем типом, основанным на `(Int, Int)`, то `IntPair(2,3)` будет допустимым литералом этого типа.</span><span class="sxs-lookup"><span data-stu-id="654b7-265">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2,3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="654b7-266">Кроме литералов, единственными выражениями определяемого пользователем типа являются символы, привязанные к значениям этого типа, элементы массива массивов этого типа и вызываемые вызовы, возвращающие этот тип.</span><span class="sxs-lookup"><span data-stu-id="654b7-266">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="654b7-267">Разносить выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-267">Unwrap Expressions</span></span>

<span data-ttu-id="654b7-268">В Q # оператор Unwrap является восклицательным знаком в конце `!`.</span><span class="sxs-lookup"><span data-stu-id="654b7-268">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="654b7-269">Например, `IntPair` если является определяемым пользователем типом с базовым типом `(Int, Int)`и `s` является переменной со значением `IntPair(2,3)`, то `s!` это будет. `(2,3)`</span><span class="sxs-lookup"><span data-stu-id="654b7-269">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2,3)`, then `s!` would be `(2,3)`.</span></span>

<span data-ttu-id="654b7-270">Для определяемых пользователем типов, определенных с точки зрения других определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="654b7-270">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="654b7-271">Оператор Unwrap может повторяться; Например, `s!!` указывает значение удвоенного неупакованного значения `s`.</span><span class="sxs-lookup"><span data-stu-id="654b7-271">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="654b7-272">Таким образом, `WrappedPair` если является определяемым пользователем типом с базовым `IntPair`типом, `t` а является переменной со значением `WrappedPair(IntPair(1,2))`, то `t!!` будет `(1,2)`.</span><span class="sxs-lookup"><span data-stu-id="654b7-272">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="654b7-273">Оператор `!` имеет более высокий приоритет, чем все остальные операторы, `[]` Кроме для индексирования и среза массива.</span><span class="sxs-lookup"><span data-stu-id="654b7-273">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="654b7-274">`!`и `[]` установите привязку с позиционированием. то есть, `a[i]![3]` должен быть считан как `((a[i])!)[3]`: взять элемент `i`"th" `a`, распаковать его, а затем получить третий элемент неупакованного значения (который должен быть массивом).</span><span class="sxs-lookup"><span data-stu-id="654b7-274">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="654b7-275">Приоритет `!` оператора имеет одно влияние, которое может быть неочевидным.</span><span class="sxs-lookup"><span data-stu-id="654b7-275">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="654b7-276">Если функция или операция возвращает значение, которое затем извлекается, функция или вызов операции должны быть заключены в круглые скобки, чтобы кортеж аргументов привязывается к вызову, а не к развернутому.</span><span class="sxs-lookup"><span data-stu-id="654b7-276">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="654b7-277">Пример:</span><span class="sxs-lookup"><span data-stu-id="654b7-277">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="654b7-278">Выражения массива</span><span class="sxs-lookup"><span data-stu-id="654b7-278">Array Expressions</span></span>

<span data-ttu-id="654b7-279">Литерал массива — это последовательность из одного или нескольких выражений элементов, разделенных запятыми, заключенная `[` в `]`и.</span><span class="sxs-lookup"><span data-stu-id="654b7-279">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="654b7-280">Все элементы должны быть совместимы с одним и тем же типом.</span><span class="sxs-lookup"><span data-stu-id="654b7-280">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="654b7-281">Если тип общего элемента является операцией или типом функции, все элементы должны иметь одинаковые входные и выходные типы.</span><span class="sxs-lookup"><span data-stu-id="654b7-281">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="654b7-282">Тип элемента массива будет поддерживать любые операторов, поддерживаемые всеми элементами.</span><span class="sxs-lookup"><span data-stu-id="654b7-282">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="654b7-283">Например, `Op1`если, `Op2`, и `Op3` все являются `Qubit[] => Unit`, но `Op1` поддерживают `Adjoint` `Op2` `Controlled`, поддерживают и `Op3` поддерживают оба:</span><span class="sxs-lookup"><span data-stu-id="654b7-283">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="654b7-284">`[Op1, Op2]`является массивом `(Qubit[] => Unit)` операций.</span><span class="sxs-lookup"><span data-stu-id="654b7-284">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="654b7-285">`[Op1, Op3]`является массивом `(Qubit[] => Unit is Adj)` операций.</span><span class="sxs-lookup"><span data-stu-id="654b7-285">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="654b7-286">`[Op2, Op3]`является массивом `(Qubit[] => Unit is Ctl)` операций.</span><span class="sxs-lookup"><span data-stu-id="654b7-286">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="654b7-287">Пустые литералы `[]`массива не допускаются.</span><span class="sxs-lookup"><span data-stu-id="654b7-287">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="654b7-288">Вместо этого `new ★[0]`с помощью `★` , где является заполнителем для подходящего типа, позволяет создать требуемый массив нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="654b7-288">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="654b7-289">При наличии двух массивов одного типа бинарный `+` оператор может использоваться для формирования нового массива, который объединяет два массива.</span><span class="sxs-lookup"><span data-stu-id="654b7-289">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="654b7-290">Например, `[1,2,3] + [4,5,6]` имеет `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="654b7-290">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="654b7-291">Создание массива</span><span class="sxs-lookup"><span data-stu-id="654b7-291">Array Creation</span></span>

<span data-ttu-id="654b7-292">При наличии типа и `Int` выражения `new` оператор может использоваться для выделения нового массива заданного размера.</span><span class="sxs-lookup"><span data-stu-id="654b7-292">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="654b7-293">Например, `new Int[i+1]` будет выделять новый `Int` массив `i+1` элементами.</span><span class="sxs-lookup"><span data-stu-id="654b7-293">For instance, `new Int[i+1]` would allocate a new `Int` array with `i+1` elements.</span></span>

<span data-ttu-id="654b7-294">Элементы нового массива инициализируются значением по умолчанию, зависящим от типа.</span><span class="sxs-lookup"><span data-stu-id="654b7-294">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="654b7-295">В большинстве случаев это разновидность нуля.</span><span class="sxs-lookup"><span data-stu-id="654b7-295">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="654b7-296">Для Кубитс и вызываемых объектов, которые являются ссылками на сущности, не существует разумного значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="654b7-296">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="654b7-297">Таким же для этих типов по умолчанию используется недопустимая ссылка, которую нельзя использовать, не вызывая ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="654b7-297">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="654b7-298">Это похоже на пустую ссылку на таких языках, как C# или Java.</span><span class="sxs-lookup"><span data-stu-id="654b7-298">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="654b7-299">Массивы, содержащие Кубитс или вызываемые, должны быть правильно инициализированы значениями, отличными от значений по умолчанию, прежде чем их элементы могут быть безопасно использованы.</span><span class="sxs-lookup"><span data-stu-id="654b7-299">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="654b7-300">Подходящие процедуры инициализации можно найти в <xref:microsoft.quantum.arrays>.</span><span class="sxs-lookup"><span data-stu-id="654b7-300">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="654b7-301">Значения по умолчанию для каждого типа:</span><span class="sxs-lookup"><span data-stu-id="654b7-301">The default values for each type are:</span></span>

<span data-ttu-id="654b7-302">Тип</span><span class="sxs-lookup"><span data-stu-id="654b7-302">Type</span></span> | <span data-ttu-id="654b7-303">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="654b7-303">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="654b7-304">_Недопустимый кубит_</span><span class="sxs-lookup"><span data-stu-id="654b7-304">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="654b7-305">Пустой диапазон,`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="654b7-305">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="654b7-306">_Недопустимый вызываемый_</span><span class="sxs-lookup"><span data-stu-id="654b7-306">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="654b7-307">Типы кортежей инициализируются элементом по элементу.</span><span class="sxs-lookup"><span data-stu-id="654b7-307">Tuple types are initialized element-by-element.</span></span>


### <a name="jagged-arrays"></a><span data-ttu-id="654b7-308">Массивы массивов</span><span class="sxs-lookup"><span data-stu-id="654b7-308">Jagged Arrays</span></span>

<span data-ttu-id="654b7-309">Массив массива, иногда называемый «массивом массивов», является массивом, элементы которого являются массивами.</span><span class="sxs-lookup"><span data-stu-id="654b7-309">A jagged array, sometimes called an "array of arrays", is an array whose elements are arrays.</span></span> <span data-ttu-id="654b7-310">Элементы массива массивов могут иметь разные размеры.</span><span class="sxs-lookup"><span data-stu-id="654b7-310">The elements of a jagged array can be of different sizes.</span></span> <span data-ttu-id="654b7-311">В следующем примере показано объявление и инициализация массива массивов, представляющего таблицу умножения.</span><span class="sxs-lookup"><span data-stu-id="654b7-311">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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


### <a name="array-slices"></a><span data-ttu-id="654b7-312">Срезы массива</span><span class="sxs-lookup"><span data-stu-id="654b7-312">Array Slices</span></span>

<span data-ttu-id="654b7-313">При наличии выражения массива и `Range` выражения можно формировать новое выражение, используя оператор среза массива `[` и `]` .</span><span class="sxs-lookup"><span data-stu-id="654b7-313">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="654b7-314">Новое выражение будет иметь тот же тип, что и массив, и будет содержать элементы массива `Range`, индексируемые элементами, в порядке, определенном. `Range`</span><span class="sxs-lookup"><span data-stu-id="654b7-314">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="654b7-315">Например `a` , если привязан к массиву `Double`s, то `a[3..-1..0]` является `Double[]` выражением, содержащим первые четыре элемента, `a` но в порядке, в котором они отображаются в. `a`</span><span class="sxs-lookup"><span data-stu-id="654b7-315">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="654b7-316">Если параметр `Range` пуст, результирующий срез массива будет иметь нулевую длину.</span><span class="sxs-lookup"><span data-stu-id="654b7-316">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="654b7-317">Если выражение массива не является простым идентификатором, его необходимо заключить в круглые скобки для среза.</span><span class="sxs-lookup"><span data-stu-id="654b7-317">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="654b7-318">Например, если `a` и `b` являются массивами `Int`s, срез из объединения будет выражаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="654b7-318">For instance, if `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

<span data-ttu-id="654b7-319">Все массивы в Q # отсчитываются от нуля.</span><span class="sxs-lookup"><span data-stu-id="654b7-319">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="654b7-320">То есть первый элемент массива `a` всегда `a[0]`имеет значение.</span><span class="sxs-lookup"><span data-stu-id="654b7-320">That is, the first element of an array `a` is always `a[0]`.</span></span>

<span data-ttu-id="654b7-321">Начиная с нашего выпуска 0,8 мы поддерживаем контекстные выражения для среза диапазона.</span><span class="sxs-lookup"><span data-stu-id="654b7-321">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="654b7-322">В частности, начальные и конечные значения диапазона могут быть опущены в контексте выражения среза диапазона.</span><span class="sxs-lookup"><span data-stu-id="654b7-322">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="654b7-323">В этом случае компилятор применит следующие правила, чтобы определить предполагаемые разделители для диапазона.</span><span class="sxs-lookup"><span data-stu-id="654b7-323">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="654b7-324">Например, если начальное значение диапазона опущено, то выводимое начальное значение</span><span class="sxs-lookup"><span data-stu-id="654b7-324">For example, if the range start value is omitted, then the inferred start value</span></span> 
- <span data-ttu-id="654b7-325">равно нулю, если шаг не указан или указанный шаг является положительным;</span><span class="sxs-lookup"><span data-stu-id="654b7-325">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="654b7-326">Длина фрагментированного массива минус один, если указанный шаг является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="654b7-326">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="654b7-327">Если значение конца диапазона опущено, то выводимое конечное значение</span><span class="sxs-lookup"><span data-stu-id="654b7-327">If the range end value is omitted, then the inferred end value</span></span> 
- <span data-ttu-id="654b7-328">Длина фрагментированного массива минус один, если шаг не указан или указанный шаг является положительным;</span><span class="sxs-lookup"><span data-stu-id="654b7-328">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="654b7-329">равно нулю, если указанный шаг является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="654b7-329">is zero if the specified step is negative.</span></span> 

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

## <a name="array-element-expressions"></a><span data-ttu-id="654b7-330">Выражения элементов массива</span><span class="sxs-lookup"><span data-stu-id="654b7-330">Array Element Expressions</span></span>

<span data-ttu-id="654b7-331">При наличии выражения массива и `Int` выражения можно формировать новое выражение с помощью оператора `[` и `]` элемента массива.</span><span class="sxs-lookup"><span data-stu-id="654b7-331">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="654b7-332">Новое выражение будет иметь тот же тип, что и тип элемента массива.</span><span class="sxs-lookup"><span data-stu-id="654b7-332">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="654b7-333">Например, `a` если привязан к массиву `Double`s, то `a[4]` является `Double` выражением.</span><span class="sxs-lookup"><span data-stu-id="654b7-333">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="654b7-334">Если выражение массива не является простым идентификатором, его необходимо заключить в круглые скобки, чтобы выбрать элемент.</span><span class="sxs-lookup"><span data-stu-id="654b7-334">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to select an element.</span></span>
<span data-ttu-id="654b7-335">Например, если `a` и `b` являются массивами `Int`s, элемент из объединения будет выражаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="654b7-335">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[13]
```

<span data-ttu-id="654b7-336">Все массивы в Q # отсчитываются от нуля.</span><span class="sxs-lookup"><span data-stu-id="654b7-336">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="654b7-337">То есть первый элемент массива `a` всегда `a[0]`имеет значение.</span><span class="sxs-lookup"><span data-stu-id="654b7-337">That is, the first element of an array `a` is always `a[0]`.</span></span>


## <a name="copy-and-update-expressions"></a><span data-ttu-id="654b7-338">Выражения копирования и обновления</span><span class="sxs-lookup"><span data-stu-id="654b7-338">Copy-and-Update Expressions</span></span>

<span data-ttu-id="654b7-339">Новые массивы можно создавать из существующих с помощью выражений копирования и обновления.</span><span class="sxs-lookup"><span data-stu-id="654b7-339">New arrays can be created from existing ones via copy-and-update expressions.</span></span>
<span data-ttu-id="654b7-340">Выражение копирования `expression1 w/ expression2 <- expression3`и обновления является выражением формы, где `expression1` должно иметь тип `T[]` для какого-либо типа. `T`</span><span class="sxs-lookup"><span data-stu-id="654b7-340">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span> <span data-ttu-id="654b7-341">Второй `expression2` определяет индексы элементов, которые необходимо изменить, по сравнению с массивом в `expression1` и должны иметь тип `Int` или. `Range`</span><span class="sxs-lookup"><span data-stu-id="654b7-341">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span> <span data-ttu-id="654b7-342">Если `expression2` имеет тип `Int`, `expression3` должен иметь тип. `T`</span><span class="sxs-lookup"><span data-stu-id="654b7-342">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="654b7-343">Если `expression2` имеет тип `Range`, `expression3` должен иметь тип. `T[]`</span><span class="sxs-lookup"><span data-stu-id="654b7-343">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="654b7-344">Выражение `arr w/ idx <- value` копирования и обновления формирует новый массив со всеми элементами, заданными в соответствующем элементе в `arr`, за исключением элементов в `idx`, для которых заданы единицы в. `value`</span><span class="sxs-lookup"><span data-stu-id="654b7-344">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="654b7-345">Например, если `arr` содержит массив `[0,1,2,3]`, то</span><span class="sxs-lookup"><span data-stu-id="654b7-345">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="654b7-346">`arr w/ 0 <- 10`является массивом `[10,1,2,3]`.</span><span class="sxs-lookup"><span data-stu-id="654b7-346">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="654b7-347">`arr w/ 2 <- 10`является массивом `[0,1,10,3]`.</span><span class="sxs-lookup"><span data-stu-id="654b7-347">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="654b7-348">`arr w/ 0..2..3 <- [10,12]`является массивом `[10,1,12,3]`.</span><span class="sxs-lookup"><span data-stu-id="654b7-348">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

<span data-ttu-id="654b7-349">Аналогичные выражения существуют для именованных элементов в определяемых пользователем типах.</span><span class="sxs-lookup"><span data-stu-id="654b7-349">Similar expressions exist for named items in user-defined types.</span></span> <span data-ttu-id="654b7-350">Рассмотрим, например, тип</span><span class="sxs-lookup"><span data-stu-id="654b7-350">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="654b7-351">Если `c` `Complex(1.,-1.)`параметр содержит значение типа, то `c w/ Re <- 0.` является выражением типа `Complex` , результатом вычисления которого является. `Complex(0.,-1.)`</span><span class="sxs-lookup"><span data-stu-id="654b7-351">If `c` contains the value of type `Complex(1.,-1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0.,-1.)`.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="654b7-352">Условные выражения</span><span class="sxs-lookup"><span data-stu-id="654b7-352">Conditional Expressions</span></span>

<span data-ttu-id="654b7-353">Учитывая два других выражения одного и того же типа и логического выражения, условное выражение может быть сформировано с помощью вопросительного знака `?` и вертикальной черты. `|`</span><span class="sxs-lookup"><span data-stu-id="654b7-353">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="654b7-354">Например, `a==b ? c | d`.</span><span class="sxs-lookup"><span data-stu-id="654b7-354">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="654b7-355">В этом примере значение условного выражения будет `c` `a==b` равно true, а `d` если — false.</span><span class="sxs-lookup"><span data-stu-id="654b7-355">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

<span data-ttu-id="654b7-356">Эти два выражения могут возвращать операции с одинаковыми входными и выходными данными, но поддерживают разные операторов.</span><span class="sxs-lookup"><span data-stu-id="654b7-356">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="654b7-357">В этом случае тип условного выражения является операцией с входными и выходными данными, которые поддерживают любые операторов, поддерживаемые обоими выражениями.</span><span class="sxs-lookup"><span data-stu-id="654b7-357">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="654b7-358">Например, `Op1`если, `Op2`, и `Op3` все являются `Qubit[]=>Unit`, но `Op1` поддерживают `Adjoint` `Op2` `Controlled`, поддерживают и `Op3` поддерживают оба:</span><span class="sxs-lookup"><span data-stu-id="654b7-358">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="654b7-359">`flag ? Op1 | Op2`является `(Qubit[] => Unit)` операцией.</span><span class="sxs-lookup"><span data-stu-id="654b7-359">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="654b7-360">`flag ? Op1 | Op3`является `(Qubit[] => Unit is Adj)` операцией.</span><span class="sxs-lookup"><span data-stu-id="654b7-360">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="654b7-361">`flag ? Op2 | Op3`является `(Qubit[] => Unit is Ctl)` операцией.</span><span class="sxs-lookup"><span data-stu-id="654b7-361">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="654b7-362">Если одно из двух возможных результатов содержит вызов функции или операции, этот вызов будет выполняться только в том случае, если результатом является значение, которое будет значением вызова.</span><span class="sxs-lookup"><span data-stu-id="654b7-362">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="654b7-363">Например, `a==b ? C(qs) | D(qs)`если `a==b` имеет значение true, то `C` операция будет вызвана, и если значение равно false, будет вызываться только. `D`</span><span class="sxs-lookup"><span data-stu-id="654b7-363">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="654b7-364">Это похоже на сокращенное вычисление на других языках.</span><span class="sxs-lookup"><span data-stu-id="654b7-364">This is similar to short-circuiting in other languages.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="654b7-365">Приоритет операторов</span><span class="sxs-lookup"><span data-stu-id="654b7-365">Operator Precedence</span></span>

<span data-ttu-id="654b7-366">Все бинарные операторы являются правой ассоциативными, за `^`исключением.</span><span class="sxs-lookup"><span data-stu-id="654b7-366">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="654b7-367">Квадратные `[` скобки и `]`, для среза и индексирования массива, выполните привязку перед любым оператором.</span><span class="sxs-lookup"><span data-stu-id="654b7-367">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="654b7-368">Операторов `Adjoint` и `Controlled` BIND после индексирования массива, но перед всеми другими операторами.</span><span class="sxs-lookup"><span data-stu-id="654b7-368">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="654b7-369">Круглые скобки для операции и вызова функции также привязываются перед любым оператором, но после индексирования массива и операторов.</span><span class="sxs-lookup"><span data-stu-id="654b7-369">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="654b7-370">Операторы в порядке приоритета, от самого высокого до самого низкого:</span><span class="sxs-lookup"><span data-stu-id="654b7-370">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="654b7-371">Оператор</span><span class="sxs-lookup"><span data-stu-id="654b7-371">Operator</span></span> | <span data-ttu-id="654b7-372">Арность</span><span class="sxs-lookup"><span data-stu-id="654b7-372">Arity</span></span> | <span data-ttu-id="654b7-373">Описание</span><span class="sxs-lookup"><span data-stu-id="654b7-373">Description</span></span> | <span data-ttu-id="654b7-374">Типы операндов</span><span class="sxs-lookup"><span data-stu-id="654b7-374">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="654b7-375">конечные`!`</span><span class="sxs-lookup"><span data-stu-id="654b7-375">trailing `!`</span></span> | <span data-ttu-id="654b7-376">Унарный</span><span class="sxs-lookup"><span data-stu-id="654b7-376">Unary</span></span> | <span data-ttu-id="654b7-377">разворачивание;</span><span class="sxs-lookup"><span data-stu-id="654b7-377">Unwrap</span></span> | <span data-ttu-id="654b7-378">Любой определяемый пользователем тип</span><span class="sxs-lookup"><span data-stu-id="654b7-378">Any user-defined type</span></span>
 <span data-ttu-id="654b7-379">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="654b7-379">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="654b7-380">Унарный</span><span class="sxs-lookup"><span data-stu-id="654b7-380">Unary</span></span> | <span data-ttu-id="654b7-381">Числовое отрицательное, побитовое дополнение, логическое отрицание</span><span class="sxs-lookup"><span data-stu-id="654b7-381">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="654b7-382">`Int`, `BigInt` или `Double` для `-`, `Int` или `BigInt` для `~~~` `Bool` для`not`</span><span class="sxs-lookup"><span data-stu-id="654b7-382">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="654b7-383">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-383">Binary</span></span> | <span data-ttu-id="654b7-384">Целочисленное энергопотребление</span><span class="sxs-lookup"><span data-stu-id="654b7-384">Integer power</span></span> | <span data-ttu-id="654b7-385">`Int`или `BigInt` для основания, `Int` для показателя степени</span><span class="sxs-lookup"><span data-stu-id="654b7-385">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="654b7-386">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="654b7-386">`/`, `*`, `%`</span></span> | <span data-ttu-id="654b7-387">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-387">Binary</span></span> | <span data-ttu-id="654b7-388">Деление, умножение, целочисленный модуль</span><span class="sxs-lookup"><span data-stu-id="654b7-388">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="654b7-389">`Int`, `BigInt` или `Double` для `/` и `*`, `Int` или `BigInt` для`%`</span><span class="sxs-lookup"><span data-stu-id="654b7-389">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="654b7-390">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="654b7-390">`+`, `-`</span></span> | <span data-ttu-id="654b7-391">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-391">Binary</span></span> | <span data-ttu-id="654b7-392">Сложение или объединение строк и массивов, вычитание</span><span class="sxs-lookup"><span data-stu-id="654b7-392">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="654b7-393">`Int`, `BigInt` или `Double`, кроме `String` того, или любого типа массива для`+`</span><span class="sxs-lookup"><span data-stu-id="654b7-393">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="654b7-394">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="654b7-394">`<<<`, `>>>`</span></span> | <span data-ttu-id="654b7-395">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-395">Binary</span></span> | <span data-ttu-id="654b7-396">Сдвиг влево, сдвиг вправо</span><span class="sxs-lookup"><span data-stu-id="654b7-396">Left shift, right shift</span></span> | <span data-ttu-id="654b7-397">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="654b7-397">`Int` or `BigInt`</span></span>
 <span data-ttu-id="654b7-398">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="654b7-398">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="654b7-399">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-399">Binary</span></span> | <span data-ttu-id="654b7-400">Сравнения "меньше чем", "меньше или равно", "больше чем", "больше или равно"</span><span class="sxs-lookup"><span data-stu-id="654b7-400">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="654b7-401">`Int`, `BigInt` или`Double`</span><span class="sxs-lookup"><span data-stu-id="654b7-401">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="654b7-402">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="654b7-402">`==`, `!=`</span></span> | <span data-ttu-id="654b7-403">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-403">Binary</span></span> | <span data-ttu-id="654b7-404">сравнения «равно» и «не равно»</span><span class="sxs-lookup"><span data-stu-id="654b7-404">equal, not-equal comparisons</span></span> | <span data-ttu-id="654b7-405">любой тип-примитив</span><span class="sxs-lookup"><span data-stu-id="654b7-405">any primitive type</span></span>
 `&&&` | <span data-ttu-id="654b7-406">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-406">Binary</span></span> | <span data-ttu-id="654b7-407">Побитовое И</span><span class="sxs-lookup"><span data-stu-id="654b7-407">Bitwise AND</span></span> | <span data-ttu-id="654b7-408">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="654b7-408">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="654b7-409">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-409">Binary</span></span> | <span data-ttu-id="654b7-410">Побитовое исключающее ИЛИ</span><span class="sxs-lookup"><span data-stu-id="654b7-410">Bitwise XOR</span></span> | <span data-ttu-id="654b7-411">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="654b7-411">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="654b7-412">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-412">Binary</span></span> | <span data-ttu-id="654b7-413">Побитовое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="654b7-413">Bitwise OR</span></span> | <span data-ttu-id="654b7-414">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="654b7-414">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="654b7-415">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-415">Binary</span></span> | <span data-ttu-id="654b7-416">Логическое И</span><span class="sxs-lookup"><span data-stu-id="654b7-416">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="654b7-417">Двоичные данные</span><span class="sxs-lookup"><span data-stu-id="654b7-417">Binary</span></span> | <span data-ttu-id="654b7-418">Логическое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="654b7-418">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="654b7-419">Двоичный/Ternary</span><span class="sxs-lookup"><span data-stu-id="654b7-419">Binary/Ternary</span></span> | <span data-ttu-id="654b7-420">Оператор Range</span><span class="sxs-lookup"><span data-stu-id="654b7-420">Range operator</span></span> | `Int`
 <span data-ttu-id="654b7-421">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="654b7-421">`?` `|`</span></span> | <span data-ttu-id="654b7-422">Ternary</span><span class="sxs-lookup"><span data-stu-id="654b7-422">Ternary</span></span> | <span data-ttu-id="654b7-423">Условная логика</span><span class="sxs-lookup"><span data-stu-id="654b7-423">Conditional</span></span> | <span data-ttu-id="654b7-424">`Bool`для левой стороны</span><span class="sxs-lookup"><span data-stu-id="654b7-424">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="654b7-425">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="654b7-425">`w/` `<-`</span></span> | <span data-ttu-id="654b7-426">Ternary</span><span class="sxs-lookup"><span data-stu-id="654b7-426">Ternary</span></span> | <span data-ttu-id="654b7-427">Копирование и обновление</span><span class="sxs-lookup"><span data-stu-id="654b7-427">Copy-and-update</span></span> | <span data-ttu-id="654b7-428">см. раздел [выражения копирования и обновления](#copy-and-update-expressions) .</span><span class="sxs-lookup"><span data-stu-id="654b7-428">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>
