---
title: 'Типы в Q #'
description: 'Сведения о различных типах, используемых в языке программирования Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: 58370193bd62e306197a9e07c28f8611f043e55c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431144"
---
# <a name="types-in-q"></a><span data-ttu-id="c847a-103">Типы в Q #</span><span class="sxs-lookup"><span data-stu-id="c847a-103">Types in Q#</span></span>

<span data-ttu-id="c847a-104">На этой странице размещается модель Q # Type и описывается синтаксис для указания типов и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="c847a-104">This page lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="c847a-105">На следующей странице [введите Expressions](xref:microsoft.quantum.guide.expressions), а затем — сведения о создании выражений этих типов и работе с ними.</span><span class="sxs-lookup"><span data-stu-id="c847a-105">The next page, [Type Expressions](xref:microsoft.quantum.guide.expressions), details how to create and operate on expressions of these types.</span></span>

<span data-ttu-id="c847a-106">Обратите внимание, что Q # является *строго типизированным* языком, поэтому Аккуратное использование этих типов может помочь компилятору обеспечить строгую гарантию для программ Q # во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="c847a-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="c847a-107">Чтобы обеспечить максимально возможную гарантию, преобразования между типами в Q # должны быть явными с помощью вызовов функций, которые выражают это преобразование.</span><span class="sxs-lookup"><span data-stu-id="c847a-107">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="c847a-108">Ряд таких функций предоставляется как часть <xref:microsoft.quantum.convert> пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c847a-108">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="c847a-109">С другой стороны, операции приведения к совместимым типам происходят неявно.</span><span class="sxs-lookup"><span data-stu-id="c847a-109">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="c847a-110">Q # предоставляет оба типа-примитива, которые можно использовать напрямую, и различные способы создания новых типов из других типов.</span><span class="sxs-lookup"><span data-stu-id="c847a-110">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="c847a-111">В оставшейся части этого раздела мы рассмотрим каждую из них.</span><span class="sxs-lookup"><span data-stu-id="c847a-111">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="c847a-112">Примитивные типы</span><span class="sxs-lookup"><span data-stu-id="c847a-112">Primitive Types</span></span>

<span data-ttu-id="c847a-113">Язык Q # предоставляет несколько *простых типов*, из которых можно создавать другие типы:</span><span class="sxs-lookup"><span data-stu-id="c847a-113">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="c847a-114">`Int`Тип представляет 64-разрядное целое число со знаком, например: `2` , `107` , `-5` .</span><span class="sxs-lookup"><span data-stu-id="c847a-114">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="c847a-115">`BigInt`Тип представляет целое число со знаком произвольного размера, например `2L` , `107L` , `-5L` .</span><span class="sxs-lookup"><span data-stu-id="c847a-115">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="c847a-116">Этот тип основан на .NET<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="c847a-116">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="c847a-117">Тип.</span><span class="sxs-lookup"><span data-stu-id="c847a-117">type.</span></span>
- <span data-ttu-id="c847a-118">`Double`Тип представляет число с плавающей запятой двойной точности, например: `0.0` , `-1.3` , `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="c847a-118">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="c847a-119">`Bool`Тип представляет логическое значение, которое может быть либо `true` `false` .</span><span class="sxs-lookup"><span data-stu-id="c847a-119">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="c847a-120">`Range`Тип представляет последовательность целых чисел, обозначенную параметром `start..step..stop` , где обозначаются параметры.</span><span class="sxs-lookup"><span data-stu-id="c847a-120">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is options.</span></span> 
   <span data-ttu-id="c847a-121">Это `start .. stop` соответствует `start..1..stop` , и, например, `1..2..7` представляет последовательность $ \{ 1, 3, 5, 7 \} $.</span><span class="sxs-lookup"><span data-stu-id="c847a-121">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="c847a-122">`String`Тип — это последовательность символов Юникода, которая непрозрачна для пользователя после создания.</span><span class="sxs-lookup"><span data-stu-id="c847a-122">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="c847a-123">Этот тип используется для передачи сообщений в классический узел в случае ошибки или диагностического события.</span><span class="sxs-lookup"><span data-stu-id="c847a-123">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="c847a-124">`Unit`Тип — это тип, который допускает только одно значение `()` .</span><span class="sxs-lookup"><span data-stu-id="c847a-124">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="c847a-125">Этот тип используется, чтобы указать, что функция Q # или операция не возвращает никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="c847a-125">This type is used to indicate that Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="c847a-126">`Qubit`Тип представляет тактовый бит или кубит.</span><span class="sxs-lookup"><span data-stu-id="c847a-126">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="c847a-127">`Qubit`непрозрачны для пользователя; единственной операцией с ними, кроме передачи их в другую операцию, является проверка удостоверения (равенство).</span><span class="sxs-lookup"><span data-stu-id="c847a-127">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="c847a-128">В конечном итоге, действия с `Qubit` s реализуются путем вызова внутренних инструкций в процессоре тактовой задержки (или при моделировании).</span><span class="sxs-lookup"><span data-stu-id="c847a-128">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="c847a-129">`Pauli`Тип представляет один из четырех однокубитых операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="c847a-129">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="c847a-130">Этот тип используется для обозначения базовой операции для поворотов и для указания измеряемого наблюдаемого типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-130">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="c847a-131">Это перечислимый тип, имеющий четыре возможных значения: `PauliI` , `PauliX` , `PauliY` и, которые `PauliZ` являются константами типа `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="c847a-131">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="c847a-132">`Result`Тип представляет результат измерения.</span><span class="sxs-lookup"><span data-stu-id="c847a-132">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="c847a-133">Это перечислимый тип с двумя возможными значениями: `One` и `Zero` , которые являются константами типа `Result` .</span><span class="sxs-lookup"><span data-stu-id="c847a-133">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="c847a-134">`Zero`Указывает, что был измерен + 1 еиженвалуе; `One`указывает значение-1 еиженвалуе.</span><span class="sxs-lookup"><span data-stu-id="c847a-134">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>

<span data-ttu-id="c847a-135">Константы,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` и `Zero` являются зарезервированными символами в Q #.</span><span class="sxs-lookup"><span data-stu-id="c847a-135">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="c847a-136">Типы массивов</span><span class="sxs-lookup"><span data-stu-id="c847a-136">Array Types</span></span>

<span data-ttu-id="c847a-137">При наличии любого допустимого типа Q # `'T` существует тип, представляющий массив значений типа `'T` .</span><span class="sxs-lookup"><span data-stu-id="c847a-137">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="c847a-138">Этот тип массива представлен как `'T[]` , например, `Qubit[]` или `Int[][]` .</span><span class="sxs-lookup"><span data-stu-id="c847a-138">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="c847a-139">Например, коллекция целых чисел обозначается `Int[]` , а массив массивов `(Bool, Pauli)` значений обозначается `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="c847a-139">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="c847a-140">Во втором примере обратите внимание, что это может быть массив массивов массива, а не прямоугольный двумерный массив.</span><span class="sxs-lookup"><span data-stu-id="c847a-140">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="c847a-141">Q # не обеспечивает поддержку для прямоугольных многомерных массивов.</span><span class="sxs-lookup"><span data-stu-id="c847a-141">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="c847a-142">Значение массива может быть написано в исходном коде Q # с помощью квадратных скобок вокруг элементов массива, как в `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="c847a-142">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="c847a-143">Тип литерала массива определяется общим базовым типом всех элементов массива.</span><span class="sxs-lookup"><span data-stu-id="c847a-143">The type of an array literal is determined by the common base type of all items in the array.</span></span> 

> [!WARNING]
> <span data-ttu-id="c847a-144">Элементы массива нельзя изменить после создания массива.</span><span class="sxs-lookup"><span data-stu-id="c847a-144">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="c847a-145">Для создания измененного массива можно использовать [Операторы обновления и повторного назначения](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) , а также [выражения копирования и обновления](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) .</span><span class="sxs-lookup"><span data-stu-id="c847a-145">[Update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) and/or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) can be used to construct a modified array.</span></span>

<span data-ttu-id="c847a-146">Кроме того, массив можно создать из его размера с помощью `new` ключевого слова:</span><span class="sxs-lookup"><span data-stu-id="c847a-146">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="c847a-147">В любом случае, после создания массива `Length` можно использовать функцию Core для получения числа элементов в виде `Int` .</span><span class="sxs-lookup"><span data-stu-id="c847a-147">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="c847a-148">Массивы могут быть вложенными в скрипты с помощью квадратных скобок, с подстрочными индексами либо с типом, либо с `Int` типом `Range` , чтобы получить либо отдельные элементы, либо новые массивы, содержащие подмножество элементов массива.</span><span class="sxs-lookup"><span data-stu-id="c847a-148">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="c847a-149">Индексы массивов отсчитываются от нуля:</span><span class="sxs-lookup"><span data-stu-id="c847a-149">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="c847a-150">Типы кортежей</span><span class="sxs-lookup"><span data-stu-id="c847a-150">Tuple Types</span></span>

<span data-ttu-id="c847a-151">При указании одного или нескольких типов, `T0` `T1` ,..., `Tn` можно обозначить новый *тип кортежа* как `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="c847a-151">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="c847a-152">Типы, используемые для создания нового типа кортежа, могут быть кортежами, как в `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="c847a-152">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="c847a-153">Однако такое вложение всегда имеет конечное ограничение, так как типы кортежей не могут быть в каких-либо обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="c847a-153">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="c847a-154">Значения нового типа кортежа являются кортежами, сформированными последовательностями значений из каждого типа в кортеже.</span><span class="sxs-lookup"><span data-stu-id="c847a-154">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="c847a-155">Например, `(3, false)` — это кортеж, тип которого является типом кортежа `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="c847a-155">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="c847a-156">Можно создавать массивы кортежей, кортежи массивов, кортежи подкортежей и т. д.</span><span class="sxs-lookup"><span data-stu-id="c847a-156">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="c847a-157">Начиная с Q # 0,3 `Unit` — это имя *типа* пустого кортежа; `()` используется для пустого *значения*кортежа.</span><span class="sxs-lookup"><span data-stu-id="c847a-157">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="c847a-158">Экземпляры кортежей являются неизменяемыми.</span><span class="sxs-lookup"><span data-stu-id="c847a-158">Tuple instances are immutable.</span></span>
<span data-ttu-id="c847a-159">Q # не предоставляет механизм для изменения содержимого кортежа после его создания.</span><span class="sxs-lookup"><span data-stu-id="c847a-159">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="c847a-160">Кортежи — это мощная концепция, используемая в Q # для объединения значений в одно значение, что упрощает их передачу.</span><span class="sxs-lookup"><span data-stu-id="c847a-160">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="c847a-161">В частности, с помощью нотации кортежа можно выразить, что каждая операция и вызываемый метод принимают ровно один вход и возвращает ровно один результат.</span><span class="sxs-lookup"><span data-stu-id="c847a-161">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="c847a-162">Эквивалентность одноэлементного кортежа</span><span class="sxs-lookup"><span data-stu-id="c847a-162">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="c847a-163">Можно создать одноэлементный кортеж (с одним элементом), `('T1)` например `(5)` или `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="c847a-163">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="c847a-164">Однако Q # обрабатывает одноэлементный кортеж как полностью эквивалентный значению заключенного в него типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-164">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="c847a-165">Это значит, что различия между and и OR между and и `5` `(5)` `5` `(((5)))` `(5, (6))` `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="c847a-165">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="c847a-166">Его можно написать так же `(5)+3` , как и для записи `5+3` , и оба выражения будут иметь значение `8` .</span><span class="sxs-lookup"><span data-stu-id="c847a-166">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>

<span data-ttu-id="c847a-167">Это эквивалентное действие применяется для всех целей, включая присваивание и выражения.</span><span class="sxs-lookup"><span data-stu-id="c847a-167">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="c847a-168">При наличии любого выражения такое же выражение, заключенное в круглые скобки, является выражением того же типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-168">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="c847a-169">Например, `(7)` является `Int` выражением, `([1,2,3])` является выражением типа массива `Int` s и `((1,2))` является выражением с типом `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="c847a-169">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="c847a-170">В частности, это означает, что операция или функция, для которых Входной кортеж или тип выходного кортежа имеет одно поле, можно рассматривать как принимающий один аргумент или возвращая одно значение.</span><span class="sxs-lookup"><span data-stu-id="c847a-170">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="c847a-171">Мы будем называть это свойство _эквивалентностью одноэлементного кортежа_.</span><span class="sxs-lookup"><span data-stu-id="c847a-171">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="c847a-172">Определяемые пользователем типы</span><span class="sxs-lookup"><span data-stu-id="c847a-172">User-Defined Types</span></span>

<span data-ttu-id="c847a-173">Объявление определяемого пользователем типа состоит из ключевого слова `newtype` , за которым следует имя определяемого пользователем типа, тип `=` , допустимая спецификация типа и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="c847a-173">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="c847a-174">Пример:</span><span class="sxs-lookup"><span data-stu-id="c847a-174">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="c847a-175">Каждый исходный файл Q # может объявлять любое количество определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="c847a-175">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="c847a-176">Имена типов должны быть уникальными в пределах пространства имен и могут не конфликтовать с именами операций и функций.</span><span class="sxs-lookup"><span data-stu-id="c847a-176">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="c847a-177">Определяемые пользователем типы различаются, даже если базовые типы идентичны.</span><span class="sxs-lookup"><span data-stu-id="c847a-177">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="c847a-178">В частности, нет автоматического преобразования между значениями двух определяемых пользователем типов, даже если базовые типы идентичны.</span><span class="sxs-lookup"><span data-stu-id="c847a-178">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="c847a-179">Сравнение именованных и анонимных элементов</span><span class="sxs-lookup"><span data-stu-id="c847a-179">Named vs. anonymous items</span></span>

<span data-ttu-id="c847a-180">Файл Q # может определять новый именованный тип, содержащий одно значение любого допустимого типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-180">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="c847a-181">Для любого типа кортежа `T` можно объявить новый определяемый пользователем тип, который является подтипом `T` с `newtype` инструкцией.</span><span class="sxs-lookup"><span data-stu-id="c847a-181">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="c847a-182">@"microsoft.quantum.math"Например, в пространстве имен сложные числа определяются как определяемые пользователем типы:</span><span class="sxs-lookup"><span data-stu-id="c847a-182">In the @"microsoft.quantum.math" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="c847a-183">Эта инструкция создает новый тип с двумя анонимными элементами типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="c847a-183">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="c847a-184">Помимо анонимных элементов, определяемые пользователем типы также поддерживают *именованные элементы* в Q # версии 0,7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="c847a-184">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="c847a-185">Например, мы могли бы назвать элементы для `Re` типа Double, представляющего реальную часть комплексного числа и `Im` для мнимой части:</span><span class="sxs-lookup"><span data-stu-id="c847a-185">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="c847a-186">Именование одного элемента в определяемом пользователем типе не подразумевает, что все элементы должны иметь имя — любое сочетание именованных и неименованных элементов поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c847a-186">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="c847a-187">Кроме того, внутренние элементы также могут называться.</span><span class="sxs-lookup"><span data-stu-id="c847a-187">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="c847a-188">Тип `Nested` , определенный ниже в качестве примера, имеет базовый тип `(Double, (Int, String))` , в котором только элемент типа называется, `Int` а все остальные элементы являются анонимными.</span><span class="sxs-lookup"><span data-stu-id="c847a-188">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="c847a-189">Именованные элементы имеют преимущество, доступ к которому можно получить напрямую с помощью *оператора доступа* `::` .</span><span class="sxs-lookup"><span data-stu-id="c847a-189">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="c847a-190">Помимо простых псевдонимов для потенциально сложных типов кортежей, одно существенное преимущество определения таких типов заключается в том, что они могут документировать намерение определенного значения.</span><span class="sxs-lookup"><span data-stu-id="c847a-190">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="c847a-191">При возврате к примеру `Complex` , один из них мог бы также определить двумерные полярные координаты в виде определяемого пользователем типа:</span><span class="sxs-lookup"><span data-stu-id="c847a-191">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="c847a-192">Хотя оба типа `Complex` и `Polar` имеют базовый тип `(Double, Double)` , эти два типа полностью несовместимы в Q #, что сводит к минимуму риск случайного вызова сложной математической функции с полярными координатами и наоборот.</span><span class="sxs-lookup"><span data-stu-id="c847a-192">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="c847a-193">Таким образом, определяемые пользователем типы имеют аналогичную роль в качестве записей в F #, например.</span><span class="sxs-lookup"><span data-stu-id="c847a-193">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="c847a-194">Доступ к анонимным элементам с помощью оператора Unwrap</span><span class="sxs-lookup"><span data-stu-id="c847a-194">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="c847a-195">Для доступа к анонимным элементам с другой стороны, сначала необходимо извлечь заключенное в оболочку значение с помощью постфиксного оператора `!` .</span><span class="sxs-lookup"><span data-stu-id="c847a-195">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="c847a-196">Оператор "Unwrap" `!` позволяет извлечь значение, содержащееся в определяемом пользователем типе.</span><span class="sxs-lookup"><span data-stu-id="c847a-196">The "unwrap" operator, `!`, allows to extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="c847a-197">Тип такого выражения "Unwrap" является базовым типом определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-197">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="c847a-198">Оператор Unwrap разворачивает ровно один слой упаковки.</span><span class="sxs-lookup"><span data-stu-id="c847a-198">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="c847a-199">Для доступа к значению с множественной обтеканием можно использовать несколько операторов распаковки.</span><span class="sxs-lookup"><span data-stu-id="c847a-199">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="c847a-200">например</span><span class="sxs-lookup"><span data-stu-id="c847a-200">For instance:</span></span>

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

<span data-ttu-id="c847a-201">Дополнительные сведения о операторе Unwrap можно найти в [выражениях типа в Q #](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="c847a-201">More details on the unwrap operator can be found at [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="c847a-202">Создание значений определяемых пользователем типов</span><span class="sxs-lookup"><span data-stu-id="c847a-202">Creating values of user-defined types</span></span>

<span data-ttu-id="c847a-203">Значения определяемого пользователем типа можно создать, вызвав соответствующий конструктор типа:</span><span class="sxs-lookup"><span data-stu-id="c847a-203">Values of a user-defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="c847a-204">Кроме того, новые значения можно создавать из существующих с помощью [выражений копирования и обновления](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="c847a-204">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="c847a-205">Как и для массивов, такие выражения копируют все значения элементов исходного выражения, за исключением указанных именованных элементов.</span><span class="sxs-lookup"><span data-stu-id="c847a-205">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="c847a-206">Для этих значений задаются значения, определенные в правой части выражения.</span><span class="sxs-lookup"><span data-stu-id="c847a-206">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="c847a-207">Любые другие языковые конструкции, например [Операторы обновления и повторного назначения](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), доступные для элементов массива, существуют и для именованных элементов в определяемых пользователем типах.</span><span class="sxs-lookup"><span data-stu-id="c847a-207">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), that are available for array items exist for named-items in user-defined types as well.</span></span>

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

<span data-ttu-id="c847a-208">Определяемые пользователем типы могут использоваться в любом месте, где можно использовать любой другой тип.</span><span class="sxs-lookup"><span data-stu-id="c847a-208">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="c847a-209">В частности, можно определить массив определяемого пользователем типа и включить определяемый пользователем тип как элемент типа кортежа.</span><span class="sxs-lookup"><span data-stu-id="c847a-209">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="c847a-210">Примечание. невозможно создать рекурсивные структуры типов.</span><span class="sxs-lookup"><span data-stu-id="c847a-210">Note is not possible to create recursive type structures.</span></span>
<span data-ttu-id="c847a-211">То есть тип, определяющий определяемый пользователем тип, не может быть типом кортежа, включающим элемент определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-211">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="c847a-212">Как правило, определяемые пользователем типы могут не иметь циклических зависимостей друг от друга, поэтому следующий набор определений типов будет недопустимым:</span><span class="sxs-lookup"><span data-stu-id="c847a-212">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a><span data-ttu-id="c847a-213">Типы операций и функций</span><span class="sxs-lookup"><span data-stu-id="c847a-213">Operation and Function Types</span></span>

<span data-ttu-id="c847a-214">Базовый тип для любого вызываемого типа записывается как `('Tinput => 'Tresult)` или `('Tinput -> 'Tresult)` , где `'Tinput` `'Tresult` типы и являются типами.</span><span class="sxs-lookup"><span data-stu-id="c847a-214">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="c847a-215">Они называются *сигнатурой* вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="c847a-215">These are called the *signature* of the callable.</span></span>

<span data-ttu-id="c847a-216">Все вызываемые команды Q # принимают одно значение в качестве входных данных и возвращают одно значение в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c847a-216">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="c847a-217">Входные и выходные значения могут быть кортежами.</span><span class="sxs-lookup"><span data-stu-id="c847a-217">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="c847a-218">Вызываемые, не возвращающие результатов `Unit` .</span><span class="sxs-lookup"><span data-stu-id="c847a-218">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="c847a-219">Вызываемые, не имеющие входных данных, принимают пустой кортеж в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="c847a-219">Callables that have no input take the empty tuple as input.</span></span>

> [!NOTE]
> <span data-ttu-id="c847a-220">Первая форма с параметром `=>` используется для операций, а вторая форма — с `->` , для функций.</span><span class="sxs-lookup"><span data-stu-id="c847a-220">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
> <span data-ttu-id="c847a-221">Например, `((Qubit, Pauli) => Result)` представляет сигнатуру для возможной операции однозначного измерения кубит.</span><span class="sxs-lookup"><span data-stu-id="c847a-221">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>
<span data-ttu-id="c847a-222">Типы *функций* полностью определяются их сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="c847a-222">*Function* types are completely specified by their signature.</span></span>
<span data-ttu-id="c847a-223">Например, функция, вычисляющая синус угла, будет иметь тип `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="c847a-223">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="c847a-224">*Операции*---, но не функции---имеют определенные дополнительные характеристики, которые выражаются как часть типа операции.</span><span class="sxs-lookup"><span data-stu-id="c847a-224">*Operations*---but not functions---have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="c847a-225">Такие характеристики включают сведения о том, что *операторов* поддерживает операция.</span><span class="sxs-lookup"><span data-stu-id="c847a-225">Such characteristics include information about what *functors* the operation supports.</span></span>
<span data-ttu-id="c847a-226">Например, если выполнение операции может быть соблюдено в состоянии других Кубитс, оно должно поддерживать `Controlled` функтор; если операция имеет обратную, она должна поддерживать `Adjoint` функтор.</span><span class="sxs-lookup"><span data-stu-id="c847a-226">For example, if execution of the operation can be conditioned on the state of other qubits, it should support the `Controlled` functor; if the operation has an inverse, it should support the `Adjoint` functor.</span></span> <span data-ttu-id="c847a-227">Операторов и операции подробно обсуждаются в разделе [операции и функции в Q #](xref:microsoft.quantum.guide.operationsfunctions), но здесь мы просто обсудим, как это изменяет сигнатуру операции.</span><span class="sxs-lookup"><span data-stu-id="c847a-227">Functors and operations are discussed in detail at [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions), but here we simply discuss how this alters the operation signature.</span></span>

<span data-ttu-id="c847a-228">Чтобы требовать поддержку для `Controlled` и/или `Adjoint` функтор в типе операции, необходимо добавить аннотацию, указывающую соответствующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="c847a-228">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="c847a-229">Аннотация `is Ctl` (например, `(Qubit => Unit is Ctl)` ) указывает, что операция является управляемой---то есть, она выполняется в состоянии другого кубит или Кубитс.</span><span class="sxs-lookup"><span data-stu-id="c847a-229">An annotation `is Ctl` (e.g. `(Qubit => Unit is Ctl)`) indicates that the operation is controllable---that is, it's execution conditioned on the state of another qubit or qubits.</span></span> <span data-ttu-id="c847a-230">Аналогично, `is Adj` указывает, что операция имеет смежный объект; или просто может быть "инверсной", чтобы успешно применить операцию, а затем ее примыкающую к состоянию оставляет состояние без изменений.</span><span class="sxs-lookup"><span data-stu-id="c847a-230">Similarly, `is Adj` indicates that the operation has an adjoint; or simply, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="c847a-231">Если требуется, чтобы операция этого типа поддерживала `Adjoint` и `Controlled` функтор, мы можем выразить это как `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="c847a-231">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="c847a-232">Например, встроенная <xref:microsoft.quantum.intrinsic.x> Операция Паули имеет тип `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="c847a-232">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="c847a-233">Тип операции, который не поддерживает ни один операторов, задается только типом входного и выходного типа без дополнительной заметки.</span><span class="sxs-lookup"><span data-stu-id="c847a-233">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="c847a-234">Функции и операции с параметрами типа</span><span class="sxs-lookup"><span data-stu-id="c847a-234">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="c847a-235">Вызываемые типы могут содержать параметры типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-235">Callable types may contain type parameters.</span></span>
<span data-ttu-id="c847a-236">Параметры типа обозначаются символом, который предваряется одинарной кавычкой; Например, является допустимым `'A` параметром типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-236">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="c847a-237">Сведения об определении вызываемых параметрами типа приведены в статье [операции и функции на странице Q #](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) .</span><span class="sxs-lookup"><span data-stu-id="c847a-237">Details on defining type-parameterized callables are provided on the [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) page.</span></span>

<span data-ttu-id="c847a-238">Параметр типа может присутствовать в одной сигнатуре более одного раза.</span><span class="sxs-lookup"><span data-stu-id="c847a-238">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="c847a-239">Например, функция, которая применяет другую функцию к каждому элементу массива и возвращает собранные результаты, будет иметь сигнатуру `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="c847a-239">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="c847a-240">Аналогично, функция, возвращающая композицию двух операций, может иметь сигнатуру `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="c847a-240">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="c847a-241">При вызове вызываемого параметризованного типа все аргументы, имеющие один и тот же параметр типа, должны иметь один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="c847a-241">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="c847a-242">Q # не предоставляет механизм ограничения возможных типов, которые могут быть заменены для параметра типа.</span><span class="sxs-lookup"><span data-stu-id="c847a-242">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

## <a name="whats-next"></a><span data-ttu-id="c847a-243">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="c847a-243">What's Next?</span></span>
<span data-ttu-id="c847a-244">Теперь, когда вы видели все типы, составляющие язык Q #, вы можете заголовкировать [выражения в q #](xref:microsoft.quantum.guide.expressions) , чтобы узнать, как создавать и манипулировать выражениями этих различных типов.</span><span class="sxs-lookup"><span data-stu-id="c847a-244">Now that you've seen all the types which comprise the Q# language, you can head to [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to see how to create and manipulate expressions of these various types.</span></span>


