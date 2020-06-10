---
title: 'Выражения типа в Q #'
description: 'Узнайте, как указывать, ссылаться и объединять константы, переменные, операторы, операции и функции в качестве выражений в Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: b32644382bb88fb11da00d0d7d78bbd797a0eaaa
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2020
ms.locfileid: "84629997"
---
# <a name="type-expressions-in-q"></a><span data-ttu-id="6c3a7-103">Выражения типа в Q #</span><span class="sxs-lookup"><span data-stu-id="6c3a7-103">Type Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="6c3a7-104">Числовые выражения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-104">Numeric Expressions</span></span>

<span data-ttu-id="6c3a7-105">Числовые выражения — это выражения типа `Int` , `BigInt` или `Double` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="6c3a7-106">То есть это либо целочисленное, либо числовое число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="6c3a7-107">`Int`литералы в Q # записываются просто как последовательность цифр.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-107">`Int` literals in Q# are written simply as a sequence of digits.</span></span>
<span data-ttu-id="6c3a7-108">Шестнадцатеричные и двоичные целые числа поддерживаются `0x` с `0b` префиксом и соответственно.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-108">Hexadecimal and binary integers are supported with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="6c3a7-109">`BigInt`литералы в Q # записываются с помощью замыкающего `l` `L` суффикса или.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-109">`BigInt` literals in Q# are written with a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="6c3a7-110">Шестнадцатеричные большие целые числа поддерживаются с префиксом "0x".</span><span class="sxs-lookup"><span data-stu-id="6c3a7-110">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="6c3a7-111">Таким образом, все следующие допустимые варианты использования `BigInt` литералов:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="6c3a7-112">`Double`литералы в Q # — это числа с плавающей запятой, записанные с использованием десятичных цифр.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="6c3a7-113">Они могут быть записаны с десятичной запятой, `.` и (или) экспоненциальной частью, обозначенной как "e" или "e" (после чего допустимы только возможные отрицательные знаки и знаки после запятой).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-113">They can be written with a decimal point, `.`, and/or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="6c3a7-114">Ниже приведены допустимые `Double` литералы: `0.0` , `1.2e5` , `1e-5` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="6c3a7-115">При наличии выражения массива любого типа элементов `Int` выражение может быть сформировано с помощью [`Length`](xref:microsoft.quantum.core.length) встроенной функции с выражением массива, заключенным в круглые скобки, `(` и `)` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-115">Given an array expression of any element type, an `Int` expression may be formed using the [`Length`](xref:microsoft.quantum.core.length) built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="6c3a7-116">Например, если `a` привязан к массиву, то `Length(a)` является целочисленным выражением.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-116">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="6c3a7-117">Если `b` является массивом массивов целых чисел, то `Int[][]` `Length(b)` — число подмассивов в `b` , а `Length(b[1])` — число целых чисел во втором подмассиве в `b` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="6c3a7-118">При наличии двух числовых выражений одного типа бинарные операторы,, `+` `-` `*` и `/` могут использоваться для формирования нового числового выражения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="6c3a7-119">Тип нового выражения будет таким же, как и типы составных выражений.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-119">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="6c3a7-120">При наличии двух целочисленных выражений бинарный оператор `^` (Power) может использоваться для формирования нового целочисленного выражения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-120">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="6c3a7-121">Аналогичным образом `^` для формирования нового двойного выражения можно использовать два выражения типа Double.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-121">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="6c3a7-122">Наконец, `^` можно использовать с большим целым числом слева и целым числом справа для формирования нового выражения больших целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-122">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="6c3a7-123">В этом случае второй параметр должен соответствовать 32 бит; Если нет, возникнет ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-123">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="6c3a7-124">При наличии двух целочисленных или больших целочисленных выражений можно формировать новое целочисленное или большое целочисленное выражение с помощью `%` операторов (модуль), `&&&` (побитовое и), `|||` (побитовое или) или `^^^` (побитовое исключающее).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-124">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="6c3a7-125">При наличии целочисленного или длинного целочисленного выражения слева, а также целочисленного выражения справа можно `<<<` использовать операторы (арифметические сдвиги влево) или `>>>` (арифметические сдвиги вправо) для создания нового выражения с тем же типом, что и у левого выражения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-125">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="6c3a7-126">Второй параметр (сумма сдвига) для операции сдвига должен быть больше или равен нулю; поведение для отрицательных сумм сдвига не определено.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="6c3a7-127">Сумма сдвига для операции сдвига также должна соответствовать 32 бит; Если нет, возникнет ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-127">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="6c3a7-128">Если число для сдвига является целым числом, то величина сдвига интерпретируется, `mod 64` то есть сдвиг 1 и сдвиг 65 имеют одинаковый результат.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-128">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="6c3a7-129">Для целочисленных и больших целочисленных значений сдвиги являются арифметическими.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="6c3a7-130">Сдвиг отрицательного значения влево или вправо приведет к отрицательному числу.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-130">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="6c3a7-131">Это значит, что сдвиг на один шаг влево или вправо точно так же, как умножение или деление на 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-131">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="6c3a7-132">Целочисленный разделитель и модуль целых чисел соответствуют тому же поведению для отрицательных чисел, что и в C#.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="6c3a7-133">То есть `a % b` всегда будет иметь тот же знак, что `a` и, и `b * (a / b) + a % b` всегда будет равно `a` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-133">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="6c3a7-134">Пример:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-134">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="6c3a7-135">5</span><span class="sxs-lookup"><span data-stu-id="6c3a7-135">5</span></span> | <span data-ttu-id="6c3a7-136">2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-136">2</span></span> | <span data-ttu-id="6c3a7-137">2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-137">2</span></span> | <span data-ttu-id="6c3a7-138">1</span><span class="sxs-lookup"><span data-stu-id="6c3a7-138">1</span></span>
 <span data-ttu-id="6c3a7-139">5</span><span class="sxs-lookup"><span data-stu-id="6c3a7-139">5</span></span> | <span data-ttu-id="6c3a7-140">-2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-140">-2</span></span> | <span data-ttu-id="6c3a7-141">-2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-141">-2</span></span> | <span data-ttu-id="6c3a7-142">1</span><span class="sxs-lookup"><span data-stu-id="6c3a7-142">1</span></span>
 <span data-ttu-id="6c3a7-143">-5</span><span class="sxs-lookup"><span data-stu-id="6c3a7-143">-5</span></span> | <span data-ttu-id="6c3a7-144">2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-144">2</span></span> | <span data-ttu-id="6c3a7-145">-2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-145">-2</span></span> | <span data-ttu-id="6c3a7-146">-1</span><span class="sxs-lookup"><span data-stu-id="6c3a7-146">-1</span></span>
 <span data-ttu-id="6c3a7-147">-5</span><span class="sxs-lookup"><span data-stu-id="6c3a7-147">-5</span></span> | <span data-ttu-id="6c3a7-148">-2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-148">-2</span></span> | <span data-ttu-id="6c3a7-149">2</span><span class="sxs-lookup"><span data-stu-id="6c3a7-149">2</span></span> | <span data-ttu-id="6c3a7-150">-1</span><span class="sxs-lookup"><span data-stu-id="6c3a7-150">-1</span></span>

<span data-ttu-id="6c3a7-151">Подразделение больших целых чисел и модуль работают одинаково.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-151">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="6c3a7-152">При наличии любого числового выражения новое выражение может быть сформировано с помощью `-` унарного оператора.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-152">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="6c3a7-153">Новое выражение будет иметь тот же тип, что и составное выражение.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-153">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="6c3a7-154">При наличии целочисленного или длинного целочисленного выражения новое выражение того же типа может быть сформировано с помощью `~~~` унарного оператора (побитовое дополнение).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-154">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="6c3a7-155">Логические выражения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-155">Boolean Expressions</span></span>

<span data-ttu-id="6c3a7-156">Двумя `Bool` литеральными значениями являются `true` и `false` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="6c3a7-157">При наличии двух выражений одного и того же примитивного типа `==` `!=` для создания выражения можно использовать бинарные операторы и `Bool` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="6c3a7-158">Выражение будет иметь значение true, если два выражения равны, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-158">The expression will be true if the two expressions are equal, and false if not.</span></span>

<span data-ttu-id="6c3a7-159">Значения определяемых пользователем типов могут не сравниваться, можно сравнивать только их неупакованные значения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="6c3a7-160">Например, с помощью оператора "Unwrap" `!` (подробно описывается в [типах в Q #](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="6c3a7-161">Сравнение на равенство для `Qubit` значений — равенство по идентификатору, то есть, определяет, совпадают ли два выражения с одинаковым кубит.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="6c3a7-162">Состояние двух Кубитс не сравнивается, обращается, измеряется или изменяется с помощью этого сравнения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-162">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="6c3a7-163">Сравнение значений на равенство `Double` может привести к неверному результату из-за эффектов округления.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="6c3a7-164">Например, `49.0 * (1.0/49.0) != 1.0` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-164">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="6c3a7-165">При наличии двух числовых выражений бинарные операторы, `>` , `<` `>=` и `<=` могут использоваться для создания нового логического выражения, которое имеет значение true, если первое выражение соответственно больше, меньше, больше или равно или меньше или равно второму выражению.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="6c3a7-166">При наличии двух логических выражений `and` `or` бинарные операторы и можно использовать для создания нового логического выражения, которое имеет значение true, если оба выражения (отв. оба или оба) имеют значение true.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-166">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="6c3a7-167">При наличии любого логического выражения `not` унарный оператор может использоваться для создания нового логического выражения, которое имеет значение true, если составное выражение имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-167">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="6c3a7-168">Строковые выражения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-168">String Expressions</span></span>

<span data-ttu-id="6c3a7-169">Q # позволяет использовать строки в `fail` инструкции (объясняются в [потоке управления](xref:microsoft.quantum.guide.controlflow#fail-statement)) и в [`Message`](xref:microsoft.quantum.intrinsic.message) стандартной функции.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-169">Q# allows strings to be used in the `fail` statement (explained at [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:microsoft.quantum.intrinsic.message) standard function.</span></span>
<span data-ttu-id="6c3a7-170">Конкретное поведение второго зависит от используемого симулятора, но обычно записывает сообщение в консоль узла при вызове во время программы Q #.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-170">The specific behavior of the latter depends on the simulator being used, but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="6c3a7-171">Строки в Q # — это литералы или интерполяции строк.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-171">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="6c3a7-172">Строковые литералы похожи на простые строковые литералы в большинстве языков: последовательность символов Юникода, заключенная в двойные кавычки `"` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-172">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="6c3a7-173">Внутри строки символ обратной косой черты `\` может использоваться для экранирования символа двойной кавычки, а также для вставки новой строки как `\n` , возврата каретки в виде `\r` и табуляции как `\t` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-173">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="6c3a7-174">Например:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-174">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="6c3a7-175">Интерполированные строки</span><span class="sxs-lookup"><span data-stu-id="6c3a7-175">Interpolated strings</span></span>

<span data-ttu-id="6c3a7-176">Синтаксис Q # для интерполяции строк является подмножеством синтаксиса C#, но мы обведем основные моменты, так как они относятся к Q #.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-176">The Q# syntax for string interpolations is a subset of the C# syntax, but we summarize here the key points as they pertain to Q#.</span></span>
<span data-ttu-id="6c3a7-177">Ниже описаны основные различия.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-177">The main distinctions are discussed below.</span></span>

<span data-ttu-id="6c3a7-178">Для определения строкового литерала в качестве интерполированной строки добавьте к началу символ `$`.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-178">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span>
<span data-ttu-id="6c3a7-179">Пробелы между `$` и должны `"` начинать строковые литералы.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-179">You cannot have any white space between the `$`and the `"` that starts a string literal.</span></span>

<span data-ttu-id="6c3a7-180">Ниже приведен простой пример использования [`Message`](xref:microsoft.quantum.intrinsic.message) функции для записи результата измерения в консоль вместе с другими выражениями Q #.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-180">The following is a basic example using the [`Message`](xref:microsoft.quantum.intrinsic.message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
<span data-ttu-id="6c3a7-181">Любое допустимое выражение Q # может присутствовать в интерполяции строки.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-181">Any valid Q# expression may appear in an interpolated string.</span></span>

<span data-ttu-id="6c3a7-182">Дополнительные сведения о синтаксисе C# можно найти в [*интерполяции строк*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-182">Further details on the C# syntax can be found at [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>
<span data-ttu-id="6c3a7-183">Самое важное отличие заключается в том, что Q # не поддерживает буквальные строки с интерполяцией (многострочные).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-183">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="6c3a7-184">Выражения внутри строки с интерполяцией следуют синтаксису Q #, а не синтаксису C#.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-184">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="6c3a7-185">Выражения диапазона</span><span class="sxs-lookup"><span data-stu-id="6c3a7-185">Range Expressions</span></span>

<span data-ttu-id="6c3a7-186">Учитывая все три `Int` выражения `start` , `step` , и `stop` , `start .. step .. stop` — это выражение диапазона, первый элемент которого имеет значение, второй элемент —, `start` `start+step` третий элемент — и `start+step+step` т. д., пока `stop` не будет передан.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-186">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="6c3a7-187">Диапазон может быть пустым, если, например, `step` положительным и `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-187">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="6c3a7-188">Последний элемент в диапазоне будет иметь значение `stop` , если разница между `start` и `stop` является целочисленным кратным, `step` то есть диапазон является инклюзивным на обоих концах.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-188">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="6c3a7-189">При наличии двух `Int` выражений `start` и `stop` `start .. stop` является выражением диапазона, равным `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-189">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="6c3a7-190">Обратите внимание, что подразумеваемым `step` является + 1, даже если `stop` значение меньше `start` ; в этом случае диапазон пуст.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-190">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="6c3a7-191">Ниже приведены некоторые примеры диапазонов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-191">Some example ranges are:</span></span>

- <span data-ttu-id="6c3a7-192">`1..3`диапазон значений 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-192">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="6c3a7-193">`2..2..5`диапазон 2, 4.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-193">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="6c3a7-194">`2..2..6`— диапазон 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-194">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="6c3a7-195">`6..-2..2`— диапазон 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-195">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="6c3a7-196">`2..1`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-196">`2..1` is the empty range.</span></span>
- <span data-ttu-id="6c3a7-197">`2..6..7`— диапазон 2.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-197">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="6c3a7-198">`2..2..1`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-198">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="6c3a7-199">`1..-1..2`является пустым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-199">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="6c3a7-200">Выражения кубит</span><span class="sxs-lookup"><span data-stu-id="6c3a7-200">Qubit Expressions</span></span>

<span data-ttu-id="6c3a7-201">Единственными `Qubit` выражениями являются символы, привязанные к `Qubit` значениям или элементам массива `Qubit` массивов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-201">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="6c3a7-202">`Qubit`Литералы отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-202">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="6c3a7-203">Выражения Паули</span><span class="sxs-lookup"><span data-stu-id="6c3a7-203">Pauli Expressions</span></span>

<span data-ttu-id="6c3a7-204">Все четыре `Pauli` значения,,, `PauliI` `PauliX` `PauliY` и `PauliZ` , являются допустимыми `Pauli` выражениями.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-204">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="6c3a7-205">Кроме того, единственными `Pauli` выражениями являются символы, привязанные к `Pauli` значениям или элементам массива `Pauli` массивов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-205">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="6c3a7-206">Выражения результатов</span><span class="sxs-lookup"><span data-stu-id="6c3a7-206">Result Expressions</span></span>

<span data-ttu-id="6c3a7-207">Два `Result` значения, `One` и `Zero` , являются допустимыми `Result` выражениями.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-207">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="6c3a7-208">Кроме того, единственными `Result` выражениями являются символы, привязанные к `Result` значениям или элементам массива `Result` массивов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-208">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="6c3a7-209">В частности, обратите внимание, что `One` не совпадает с целым числом `1` и прямое преобразование между ними отсутствует.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-209">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="6c3a7-210">Это справедливо `Zero` и для и `0` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-210">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="6c3a7-211">Кортежные выражения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-211">Tuple Expressions</span></span>

<span data-ttu-id="6c3a7-212">Литерал кортежа — это последовательность выражений элементов соответствующего типа, разделенных запятыми, заключенная в `(` и `)` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-212">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="6c3a7-213">Например, `(1, One)` является `(Int, Result)` выражением.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-213">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="6c3a7-214">Кроме литералов, единственными кортежными выражениями являются символы, привязанные к значениям кортежа, элементы массива кортежей и вызываемые вызовы, возвращающие кортежи.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-214">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="6c3a7-215">Выражения определяемого пользователем типа</span><span class="sxs-lookup"><span data-stu-id="6c3a7-215">User-Defined Type Expressions</span></span>

<span data-ttu-id="6c3a7-216">Литерал определяемого пользователем типа состоит из имени типа, за которым следует литерал кортежа базового типа кортежа типа.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-216">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="6c3a7-217">Например, если `IntPair` является определяемым пользователем типом, основанным на `(Int, Int)` , то будет `IntPair(2, 3)` допустимым литералом этого типа.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-217">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="6c3a7-218">Кроме литералов, единственными выражениями определяемого пользователем типа являются символы, привязанные к значениям этого типа, элементы массива массивов этого типа и вызываемые вызовы, возвращающие этот тип.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-218">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="6c3a7-219">Разносить выражения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-219">Unwrap Expressions</span></span>

<span data-ttu-id="6c3a7-220">В Q # оператор Unwrap является восклицательным знаком в конце `!` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-220">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="6c3a7-221">Например, если `IntPair` является определяемым пользователем типом с базовым типом `(Int, Int)` и является `s` переменной со значением `IntPair(2, 3)` , то `s!` `(2, 3)` это будет.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-221">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2, 3)`, then `s!` would be `(2, 3)`.</span></span>

<span data-ttu-id="6c3a7-222">Для определяемых пользователем типов, определенных с точки зрения других определяемых пользователем типов, оператор Unwrap может повторяться; Например, `s!!` указывает значение удвоенного неупакованного значения `s` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-222">For user-defined types defined in terms of other user-defined types, the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="6c3a7-223">Таким образом, если `WrappedPair` является определяемым пользователем типом с базовым типом `IntPair` , а `t` является переменной со значением `WrappedPair(IntPair(1,2))` , то будет `t!!` `(1,2)` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-223">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="6c3a7-224">`!`Оператор имеет более высокий приоритет, чем все остальные операторы `[]` , кроме для индексирования и среза массива.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-224">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="6c3a7-225">`!`и `[]` необходимо выполнить привязку с позиционированием, то есть `a[i]![3]` должны быть считаны следующим образом `((a[i])!)[3]` : взять `i` элемент "th" `a` , распаковать его, а затем получить третий элемент неупакованного значения (который должен быть массивом).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-225">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="6c3a7-226">Приоритет `!` оператора имеет одно влияние, которое может быть неочевидным.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-226">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="6c3a7-227">Если функция или операция возвращает значение, которое затем извлекается, функция или вызов операции должны быть заключены в круглые скобки, чтобы кортеж аргументов привязывается к вызову, а не к развернутому.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-227">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="6c3a7-228">Пример:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-228">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="6c3a7-229">Выражения массива</span><span class="sxs-lookup"><span data-stu-id="6c3a7-229">Array Expressions</span></span>

<span data-ttu-id="6c3a7-230">Литерал массива — это последовательность из одного или нескольких выражений элементов, разделенных запятыми, заключенная в `[` и `]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-230">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="6c3a7-231">Все элементы должны быть совместимы с одним и тем же типом.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-231">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="6c3a7-232">При наличии двух массивов одного типа бинарный `+` оператор может использоваться для формирования нового массива, который объединяет два массива.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-232">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="6c3a7-233">Например, `[1,2,3] + [4,5,6]` имеет `[1,2,3,4,5,6]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-233">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="6c3a7-234">Создание массива</span><span class="sxs-lookup"><span data-stu-id="6c3a7-234">Array Creation</span></span>

<span data-ttu-id="6c3a7-235">При наличии типа и `Int` выражения `new` оператор может использоваться для выделения нового массива заданного размера.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-235">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="6c3a7-236">Например, `new Int[i + 1]` будет выделять новый `Int` массив `i + 1` элементами.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-236">For instance, `new Int[i + 1]` would allocate a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="6c3a7-237">Пустые литералы массива `[]` не допускаются.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-237">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="6c3a7-238">Вместо этого с помощью `new ★[0]` , где `★` является заполнителем для подходящего типа, позволяет создать требуемый массив нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-238">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="6c3a7-239">Элементы нового массива инициализируются значением по умолчанию, зависящим от типа.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-239">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="6c3a7-240">В большинстве случаев это разновидность нуля.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-240">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="6c3a7-241">Для Кубитс и вызываемых объектов, которые являются ссылками на сущности, не существует разумного значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-241">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="6c3a7-242">Таким же для этих типов по умолчанию используется недопустимая ссылка, которую нельзя использовать, не вызывая ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-242">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="6c3a7-243">Это похоже на пустую ссылку на таких языках, как C# или Java.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-243">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="6c3a7-244">Массивы, содержащие Кубитс или вызываемые, должны быть правильно инициализированы значениями, отличными от значений по умолчанию, прежде чем их элементы могут быть безопасно использованы.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-244">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="6c3a7-245">Подходящие процедуры инициализации можно найти в <xref:microsoft.quantum.arrays> .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-245">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="6c3a7-246">Значения по умолчанию для каждого типа:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-246">The default values for each type are:</span></span>

<span data-ttu-id="6c3a7-247">Тип</span><span class="sxs-lookup"><span data-stu-id="6c3a7-247">Type</span></span> | <span data-ttu-id="6c3a7-248">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="6c3a7-248">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="6c3a7-249">_Недопустимый кубит_</span><span class="sxs-lookup"><span data-stu-id="6c3a7-249">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="6c3a7-250">Пустой диапазон,`1..1..0`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-250">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="6c3a7-251">_Недопустимый вызываемый_</span><span class="sxs-lookup"><span data-stu-id="6c3a7-251">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="6c3a7-252">Типы кортежей инициализируются элементом по элементу.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-252">Tuple types are initialized element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="6c3a7-253">Элементы массива</span><span class="sxs-lookup"><span data-stu-id="6c3a7-253">Array Elements</span></span>

<span data-ttu-id="6c3a7-254">При наличии выражения массива и `Int` выражения можно формировать новое выражение с помощью `[` `]` оператора и элемента массива.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-254">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="6c3a7-255">Новое выражение будет иметь тот же тип, что и тип элемента массива.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-255">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="6c3a7-256">Например, если `a` привязан к массиву `Double` s, то `a[4]` является `Double` выражением.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-256">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="6c3a7-257">Если выражение массива не является простым идентификатором, его необходимо заключить в круглые скобки, чтобы выбрать элемент.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-257">If the array expression is not a simple identifier, it must be enclosed in parentheses in order to select an element.</span></span>
<span data-ttu-id="6c3a7-258">Например, если `a` и `b` являются массивами `Int` s, элемент из объединения будет выражаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-258">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="6c3a7-259">Все массивы в Q # отсчитываются от нуля.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-259">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="6c3a7-260">То есть первый элемент массива `a` всегда имеет значение `a[0]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-260">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="6c3a7-261">Срезы массива</span><span class="sxs-lookup"><span data-stu-id="6c3a7-261">Array Slices</span></span>

<span data-ttu-id="6c3a7-262">При наличии выражения массива и `Range` выражения можно формировать новое выражение, используя `[` `]` оператор среза массива и.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-262">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="6c3a7-263">Новое выражение будет иметь тот же тип, что и массив, и будет содержать элементы массива, индексируемые элементами `Range` , в порядке, определенном `Range` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-263">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="6c3a7-264">Например, если `a` привязан к массиву `Double` s, то `a[3..-1..0]` является `Double[]` выражением, содержащим первые четыре элемента, `a` но в порядке, в котором они отображаются в `a` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-264">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="6c3a7-265">Если параметр `Range` пуст, результирующий срез массива будет иметь нулевую длину.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-265">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="6c3a7-266">Как и для ссылок на элементы массива, если выражение массива не является простым идентификатором, оно должно быть заключено в круглые скобки для среза.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-266">Just as with referencing array elements, if the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="6c3a7-267">Если `a` и `b` являются массивами типа `Int` s, срез из объединения будет выражаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-267">If `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="6c3a7-268">Выводимые начальные и конечные значения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-268">Inferred start/end values</span></span>

<span data-ttu-id="6c3a7-269">Начиная с нашего выпуска 0,8 мы поддерживаем контекстные выражения для среза диапазона.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-269">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="6c3a7-270">В частности, начальные и конечные значения диапазона могут быть опущены в контексте выражения среза диапазона.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-270">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="6c3a7-271">В этом случае компилятор применит следующие правила, чтобы определить предполагаемые разделители для диапазона.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-271">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="6c3a7-272">Например, если начальное значение диапазона опущено, то выводимое начальное значение</span><span class="sxs-lookup"><span data-stu-id="6c3a7-272">For example, if the range start value is omitted,  then the inferred start value</span></span> 
- <span data-ttu-id="6c3a7-273">равно нулю, если шаг не указан или указанный шаг является положительным;</span><span class="sxs-lookup"><span data-stu-id="6c3a7-273">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="6c3a7-274">Длина фрагментированного массива минус один, если указанный шаг является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-274">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="6c3a7-275">Если значение конца диапазона опущено, то выводимое конечное значение</span><span class="sxs-lookup"><span data-stu-id="6c3a7-275">If the range end value is omitted,  then the inferred end value</span></span> 
- <span data-ttu-id="6c3a7-276">Длина фрагментированного массива минус один, если шаг не указан или указанный шаг является положительным;</span><span class="sxs-lookup"><span data-stu-id="6c3a7-276">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="6c3a7-277">равно нулю, если указанный шаг является отрицательным.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-277">is zero if the specified step is negative.</span></span> 

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

### <a name="copy-and-update-expressions"></a><span data-ttu-id="6c3a7-278">Выражения копирования и обновления</span><span class="sxs-lookup"><span data-stu-id="6c3a7-278">Copy-and-Update Expressions</span></span>

<span data-ttu-id="6c3a7-279">Так как все типы Q # являются типами значений — с Кубитс, принимающей более специальную роль — формально — «копия» создается, когда значение привязывается к символу, или при повторной привязке символа.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-279">Since all Q# types are value types — with the qubits taking a somewhat special role —formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="6c3a7-280">То есть, поведение Q # аналогично тому, как если бы копия была создана при назначении.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-280">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span>
<span data-ttu-id="6c3a7-281">Разумеется, на практике при необходимости воссоздаются только соответствующие части.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-281">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

<span data-ttu-id="6c3a7-282">В частности, это также касается массивов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-282">This in particular also includes arrays.</span></span>
<span data-ttu-id="6c3a7-283">В частности, невозможно обновить элементы массива.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-283">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="6c3a7-284">Чтобы изменить существующий массив, необходимо использовать механизм *копирования и обновления* .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-284">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="6c3a7-285">Новые массивы можно создавать из существующих с помощью выражений *копирования и обновления* .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-285">New arrays can be created from existing ones via *copy-and-update* expressions.</span></span>
<span data-ttu-id="6c3a7-286">Выражение копирования и обновления является выражением формы `expression1 w/ expression2 <- expression3` , где должно `expression1` иметь тип `T[]` для какого-либо типа `T` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-286">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span>
<span data-ttu-id="6c3a7-287">Второй `expression2` определяет индексы элементов, которые необходимо изменить, по сравнению с массивом в `expression1` и должны иметь тип `Int` или `Range` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-287">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span>
<span data-ttu-id="6c3a7-288">Если `expression2` имеет тип `Int` , должен `expression3` иметь тип `T` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-288">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="6c3a7-289">Если `expression2` имеет тип `Range` , должен `expression3` иметь тип `T[]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-289">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="6c3a7-290">Выражение копирования и обновления `arr w/ idx <- value` формирует новый массив со всеми элементами, заданными в соответствующем элементе в `arr` , за исключением элементов в `idx` , для которых заданы единицы в `value` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-290">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="6c3a7-291">Например, если `arr` содержит массив `[0,1,2,3]` , то</span><span class="sxs-lookup"><span data-stu-id="6c3a7-291">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="6c3a7-292">`arr w/ 0 <- 10`является массивом `[10,1,2,3]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-292">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="6c3a7-293">`arr w/ 2 <- 10`является массивом `[0,1,10,3]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-293">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="6c3a7-294">`arr w/ 0..2..3 <- [10,12]`является массивом `[10,1,12,3]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-294">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="6c3a7-295">Выражения копирования и обновления для именованных элементов</span><span class="sxs-lookup"><span data-stu-id="6c3a7-295">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="6c3a7-296">Аналогичные выражения существуют для именованных элементов в определяемых пользователем типах.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-296">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="6c3a7-297">Рассмотрим, например, тип</span><span class="sxs-lookup"><span data-stu-id="6c3a7-297">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="6c3a7-298">Если `c` параметр содержит значение типа `Complex(1., -1.)` , то `c w/ Re <- 0.` является выражением типа `Complex` , результатом вычисления которого является `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-298">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="6c3a7-299">Массивы массивов</span><span class="sxs-lookup"><span data-stu-id="6c3a7-299">Jagged Arrays</span></span>

<span data-ttu-id="6c3a7-300">Массив массива, иногда называемый «массивом массивов», представляет собой массив, элементы которого являются массивами.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-300">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="6c3a7-301">Элементы массива массивов могут иметь разные размеры.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-301">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="6c3a7-302">В следующем примере показано объявление и инициализация массива массивов, представляющего таблицу умножения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-302">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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

### <a name="arrays-of-callables"></a><span data-ttu-id="6c3a7-303">Массивы вызываемых элементов</span><span class="sxs-lookup"><span data-stu-id="6c3a7-303">Arrays of callables</span></span> 

<span data-ttu-id="6c3a7-304">Обратите внимание, что дополнительные сведения о вызываемых типах можно найти ниже, а также на следующей странице, [операциях и функциях в Q #](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-304">Note that more details on callable types can be found below, as well as on the next page, [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

<span data-ttu-id="6c3a7-305">Если тип общего элемента является операцией или типом функции, все элементы должны иметь одинаковые входные и выходные типы.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-305">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="6c3a7-306">Тип элемента массива будет поддерживать любые операторов, поддерживаемые всеми элементами.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-306">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="6c3a7-307">Например, если `Op1` , `Op2` , и `Op3` все являются `Qubit[] => Unit` , но поддерживают, поддерживают `Op1` `Adjoint` `Op2` `Controlled` и `Op3` поддерживают оба:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-307">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="6c3a7-308">`[Op1, Op2]`является массивом `(Qubit[] => Unit)` операций.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-308">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="6c3a7-309">`[Op1, Op3]`является массивом `(Qubit[] => Unit is Adj)` операций.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-309">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="6c3a7-310">`[Op2, Op3]`является массивом `(Qubit[] => Unit is Ctl)` операций.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-310">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="6c3a7-311">Однако, хотя `(Qubit[] => Unit is Adj)` `(Qubit[] => Unit is Ctl)` операции и имеют общий базовый тип `(Qubit[] => Unit)` , обратите внимание, что *of* массивы этих операторов не имеют общего базового типа.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-311">However, while `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` operations have the common base type of `(Qubit[] => Unit)`, note that arrays *of* these operators do not share a common base type.</span></span> <span data-ttu-id="6c3a7-312">Например, `[[Op1], [Op2]]` в настоящее время вызовет ошибку, так как пытается создать массив несовместимых типов массивов `(Qubit[] => Unit is Adj)[]` и `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-312">For example, `[[Op1], [Op2]]` would currently raise an error because it is attempting to create an array of the incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>


## <a name="conditional-expressions"></a><span data-ttu-id="6c3a7-313">Условные выражения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-313">Conditional Expressions</span></span>

<span data-ttu-id="6c3a7-314">Учитывая два других выражения одного и того же типа и логического выражения, условное выражение может быть сформировано с помощью вопросительного знака `?` и вертикальной черты `|` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-314">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="6c3a7-315">Например, `a==b ? c | d` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-315">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="6c3a7-316">В этом примере значение условного выражения будет равно `c` `a==b` true, а `d` Если — false.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-316">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="6c3a7-317">Условные выражения с вызываемыми</span><span class="sxs-lookup"><span data-stu-id="6c3a7-317">Conditional expressions with callables</span></span>

<span data-ttu-id="6c3a7-318">Эти два выражения могут возвращать операции с одинаковыми входными и выходными данными, но поддерживают разные операторов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-318">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="6c3a7-319">В этом случае тип условного выражения является операцией с входными и выходными данными, которые поддерживают любые операторов, поддерживаемые обоими выражениями.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-319">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="6c3a7-320">Например, если `Op1` , `Op2` , и `Op3` все являются `Qubit[]=>Unit` , но поддерживают, поддерживают `Op1` `Adjoint` `Op2` `Controlled` и `Op3` поддерживают оба:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-320">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="6c3a7-321">`flag ? Op1 | Op2`является `(Qubit[] => Unit)` операцией.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-321">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="6c3a7-322">`flag ? Op1 | Op3`является `(Qubit[] => Unit is Adj)` операцией.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-322">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="6c3a7-323">`flag ? Op2 | Op3`является `(Qubit[] => Unit is Ctl)` операцией.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-323">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="6c3a7-324">Если одно из двух возможных результатов содержит вызов функции или операции, этот вызов будет выполняться только в том случае, если результатом является значение, которое будет значением вызова.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-324">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="6c3a7-325">Например, `a==b ? C(qs) | D(qs)` Если `a==b` имеет значение true, то `C` операция будет вызвана, и если значение равно false, `D` будет вызываться только.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-325">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="6c3a7-326">Это похоже на сокращенное вычисление на других языках.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-326">This is similar to short-circuiting in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="6c3a7-327">Вызываемые выражения</span><span class="sxs-lookup"><span data-stu-id="6c3a7-327">Callable Expressions</span></span>

<span data-ttu-id="6c3a7-328">Вызываемый литерал — это имя операции или функции, определенной в области компиляции.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-328">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="6c3a7-329">Например, `X` — это литерал операции, который ссылается на стандартную `X` операцию библиотеки и `Message` является литералом функции, который ссылается на стандартную библиотеку `Message` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-329">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="6c3a7-330">Если операция поддерживает `Adjoint` функтор, то `Adjoint op` это выражение операции.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-330">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="6c3a7-331">Аналогично, если операция поддерживает `Controlled` функтор, то `Controlled op` это выражение операции.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-331">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="6c3a7-332">Типы этих выражений задаются при [выполнении специализаций операции вызова](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span><span class="sxs-lookup"><span data-stu-id="6c3a7-332">The types of these expressions are specified at [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="6c3a7-333">Операторов ( `Adjoint` и `Controlled` ) привязываются более тесно, чем все другие операторы, за исключением оператора Unwrap `!` и индексации массива с [] '.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-333">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with []\`.</span></span>
<span data-ttu-id="6c3a7-334">Таким образом, все следующие юридические, предполагая, что операции поддерживают операторов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-334">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="6c3a7-335">Вызываемые выражения типа с параметрами</span><span class="sxs-lookup"><span data-stu-id="6c3a7-335">Type-parameterized callable expressions</span></span>

<span data-ttu-id="6c3a7-336">В качестве значения можно использовать вызываемый литерал, например, чтобы присвоить значение переменной или передать другому вызываемому.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-336">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="6c3a7-337">В этом случае, если вызываемый [тип имеет параметры типа](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), они должны быть предоставлены как часть вызываемого значения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-337">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), they must be provided as part of the callable value.</span></span>
<span data-ttu-id="6c3a7-338">Вызываемое значение не может иметь неопределенные параметры типа.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-338">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="6c3a7-339">Например, если `Fun` является функцией с сигнатурой `'T1->Unit` :</span><span class="sxs-lookup"><span data-stu-id="6c3a7-339">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="6c3a7-340">Выражения вызываемого вызова</span><span class="sxs-lookup"><span data-stu-id="6c3a7-340">Callable Invocation Expressions</span></span>

<span data-ttu-id="6c3a7-341">При наличии вызываемого выражения (операции или функции) и кортежного выражения входного типа сигнатуры вызываемого метода выражение вызова может быть сформировано путем добавления кортежного выражения к вызываемому выражению.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-341">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="6c3a7-342">Тип выражения вызова является выходным типом сигнатуры вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-342">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="6c3a7-343">Например, если `Op` является операцией с сигнатурой `((Int, Qubit) => Double)` , `Op(3, qubit1)` является выражением типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-343">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="6c3a7-344">Аналогично, если `Sin` является функцией с сигнатурой `(Double -> Double)` , `Sin(0.1)` является выражением типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-344">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="6c3a7-345">Наконец, если `Builder` является функцией с сигнатурой `(Int -> (Int -> Int))` , функция преобразуется `Builder(3)` в тип в int.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-345">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="6c3a7-346">Для вызова результата выражения с вызываемым значением требуется еще одна пара круглых скобок вокруг вызываемого выражения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-346">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="6c3a7-347">Таким образом, чтобы вызвать результат вызова `Builder` из предыдущего абзаца, правильным синтаксисом является:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-347">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="6c3a7-348">При вызове вызываемого [типа с параметрами](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) , фактические параметры типа могут быть указаны в угловых скобках `<` и `>` после вызываемого выражения.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-348">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="6c3a7-349">Обычно это не требуется, так как компилятор Q # будет вычислять фактические типы.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-349">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="6c3a7-350">Однако *он необходим* для [частичного приложения](xref:microsoft.quantum.guide.operationsfunctions#partial-application) , если аргумент с параметризованным типом не указан.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-350">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="6c3a7-351">Кроме того, она иногда полезна при передаче операций с разными функтор, которые поддерживаются для вызова.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-351">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="6c3a7-352">Например, если имеет сигнатуру и имеет сигнатуру и имеет сигнатуру, то `Func` `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)` для вызова `Func` с помощью в `Op1` качестве первого аргумента, `Op2` а также в `Op3` качестве третьей:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-352">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="6c3a7-353">Спецификация типа является обязательной `Op3` , поскольку и `Op1` имеет разные типы, поэтому компилятор будет считать его неоднозначным без спецификации.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-353">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="6c3a7-354">Приоритет операторов</span><span class="sxs-lookup"><span data-stu-id="6c3a7-354">Operator Precedence</span></span>

<span data-ttu-id="6c3a7-355">Все бинарные операторы являются правой ассоциативными, за исключением `^` .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-355">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="6c3a7-356">Квадратные скобки `[` и `]` , для среза и индексирования массива, выполните привязку перед любым оператором.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-356">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="6c3a7-357">Операторов `Adjoint` и `Controlled` BIND после индексирования массива, но перед всеми другими операторами.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-357">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="6c3a7-358">Круглые скобки для операции и вызова функции также привязываются перед любым оператором, но после индексирования массива и операторов.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-358">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="6c3a7-359">Операторы в порядке приоритета, от самого высокого до самого низкого:</span><span class="sxs-lookup"><span data-stu-id="6c3a7-359">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="6c3a7-360">Оператор</span><span class="sxs-lookup"><span data-stu-id="6c3a7-360">Operator</span></span> | <span data-ttu-id="6c3a7-361">Арность</span><span class="sxs-lookup"><span data-stu-id="6c3a7-361">Arity</span></span> | <span data-ttu-id="6c3a7-362">Описание</span><span class="sxs-lookup"><span data-stu-id="6c3a7-362">Description</span></span> | <span data-ttu-id="6c3a7-363">Типы операндов</span><span class="sxs-lookup"><span data-stu-id="6c3a7-363">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="6c3a7-364">конечные`!`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-364">trailing `!`</span></span> | <span data-ttu-id="6c3a7-365">Унарный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-365">Unary</span></span> | <span data-ttu-id="6c3a7-366">разворачивание;</span><span class="sxs-lookup"><span data-stu-id="6c3a7-366">Unwrap</span></span> | <span data-ttu-id="6c3a7-367">Любой определяемый пользователем тип</span><span class="sxs-lookup"><span data-stu-id="6c3a7-367">Any user-defined type</span></span>
 <span data-ttu-id="6c3a7-368">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-368">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="6c3a7-369">Унарный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-369">Unary</span></span> | <span data-ttu-id="6c3a7-370">Числовое отрицательное, побитовое дополнение, логическое отрицание</span><span class="sxs-lookup"><span data-stu-id="6c3a7-370">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="6c3a7-371">`Int`, `BigInt` или `Double` для `-` , `Int` или `BigInt` для `~~~` `Bool` для`not`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-371">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="6c3a7-372">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-372">Binary</span></span> | <span data-ttu-id="6c3a7-373">Целочисленное энергопотребление</span><span class="sxs-lookup"><span data-stu-id="6c3a7-373">Integer power</span></span> | <span data-ttu-id="6c3a7-374">`Int`или `BigInt` для основания, `Int` для показателя степени</span><span class="sxs-lookup"><span data-stu-id="6c3a7-374">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="6c3a7-375">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-375">`/`, `*`, `%`</span></span> | <span data-ttu-id="6c3a7-376">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-376">Binary</span></span> | <span data-ttu-id="6c3a7-377">Деление, умножение, целочисленный модуль</span><span class="sxs-lookup"><span data-stu-id="6c3a7-377">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="6c3a7-378">`Int`, `BigInt` или `Double` для `/` и `*` , `Int` или `BigInt` для`%`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-378">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="6c3a7-379">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-379">`+`, `-`</span></span> | <span data-ttu-id="6c3a7-380">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-380">Binary</span></span> | <span data-ttu-id="6c3a7-381">Сложение или объединение строк и массивов, вычитание</span><span class="sxs-lookup"><span data-stu-id="6c3a7-381">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="6c3a7-382">`Int`, `BigInt` или `Double` , Кроме того, `String` или любого типа массива для`+`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-382">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="6c3a7-383">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-383">`<<<`, `>>>`</span></span> | <span data-ttu-id="6c3a7-384">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-384">Binary</span></span> | <span data-ttu-id="6c3a7-385">Сдвиг влево, сдвиг вправо</span><span class="sxs-lookup"><span data-stu-id="6c3a7-385">Left shift, right shift</span></span> | <span data-ttu-id="6c3a7-386">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-386">`Int` or `BigInt`</span></span>
 <span data-ttu-id="6c3a7-387">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-387">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="6c3a7-388">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-388">Binary</span></span> | <span data-ttu-id="6c3a7-389">Сравнения "меньше чем", "меньше или равно", "больше чем", "больше или равно"</span><span class="sxs-lookup"><span data-stu-id="6c3a7-389">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="6c3a7-390">`Int`, `BigInt` или`Double`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-390">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="6c3a7-391">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-391">`==`, `!=`</span></span> | <span data-ttu-id="6c3a7-392">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-392">Binary</span></span> | <span data-ttu-id="6c3a7-393">сравнения «равно» и «не равно»</span><span class="sxs-lookup"><span data-stu-id="6c3a7-393">equal, not-equal comparisons</span></span> | <span data-ttu-id="6c3a7-394">любой тип-примитив</span><span class="sxs-lookup"><span data-stu-id="6c3a7-394">any primitive type</span></span>
 `&&&` | <span data-ttu-id="6c3a7-395">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-395">Binary</span></span> | <span data-ttu-id="6c3a7-396">Побитовое И</span><span class="sxs-lookup"><span data-stu-id="6c3a7-396">Bitwise AND</span></span> | <span data-ttu-id="6c3a7-397">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-397">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="6c3a7-398">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-398">Binary</span></span> | <span data-ttu-id="6c3a7-399">Побитовое исключающее ИЛИ</span><span class="sxs-lookup"><span data-stu-id="6c3a7-399">Bitwise XOR</span></span> | <span data-ttu-id="6c3a7-400">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-400">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="6c3a7-401">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-401">Binary</span></span> | <span data-ttu-id="6c3a7-402">Побитовое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="6c3a7-402">Bitwise OR</span></span> | <span data-ttu-id="6c3a7-403">`Int` или `BigInt`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-403">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="6c3a7-404">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-404">Binary</span></span> | <span data-ttu-id="6c3a7-405">Логическое И</span><span class="sxs-lookup"><span data-stu-id="6c3a7-405">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="6c3a7-406">Двоичный</span><span class="sxs-lookup"><span data-stu-id="6c3a7-406">Binary</span></span> | <span data-ttu-id="6c3a7-407">Логическое ИЛИ</span><span class="sxs-lookup"><span data-stu-id="6c3a7-407">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="6c3a7-408">Двоичный/Ternary</span><span class="sxs-lookup"><span data-stu-id="6c3a7-408">Binary/Ternary</span></span> | <span data-ttu-id="6c3a7-409">Оператор Range</span><span class="sxs-lookup"><span data-stu-id="6c3a7-409">Range operator</span></span> | `Int`
 <span data-ttu-id="6c3a7-410">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-410">`?` `|`</span></span> | <span data-ttu-id="6c3a7-411">Ternary</span><span class="sxs-lookup"><span data-stu-id="6c3a7-411">Ternary</span></span> | <span data-ttu-id="6c3a7-412">Условная логика</span><span class="sxs-lookup"><span data-stu-id="6c3a7-412">Conditional</span></span> | <span data-ttu-id="6c3a7-413">`Bool`для левой стороны</span><span class="sxs-lookup"><span data-stu-id="6c3a7-413">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="6c3a7-414">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="6c3a7-414">`w/` `<-`</span></span> | <span data-ttu-id="6c3a7-415">Ternary</span><span class="sxs-lookup"><span data-stu-id="6c3a7-415">Ternary</span></span> | <span data-ttu-id="6c3a7-416">Копирование и обновление</span><span class="sxs-lookup"><span data-stu-id="6c3a7-416">Copy-and-update</span></span> | <span data-ttu-id="6c3a7-417">см. раздел [выражения копирования и обновления](#copy-and-update-expressions) .</span><span class="sxs-lookup"><span data-stu-id="6c3a7-417">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="6c3a7-418">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6c3a7-418">Next steps</span></span>

<span data-ttu-id="6c3a7-419">Теперь, когда вы можете работать с выражениями в Q #, вы можете заголовкить [операции и функции в q #](xref:microsoft.quantum.guide.operationsfunctions) , чтобы научиться определять и вызывать операции и функции.</span><span class="sxs-lookup"><span data-stu-id="6c3a7-419">Now that you can work with expressions in Q#, you can head to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
