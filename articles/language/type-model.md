---
title: 'Q # тип модель | Документация Майкрософт'
description: 'Модель типа Q #'
author: QuantumWriter
uid: microsoft.quantum.language.type-model
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4e251053d1b8306bf8956314d8099e95c56bce55
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184752"
---
# <a name="the-type-model"></a><span data-ttu-id="0d891-103">Модель типа</span><span class="sxs-lookup"><span data-stu-id="0d891-103">The Type Model</span></span>

<span data-ttu-id="0d891-104">В этом разделе рассматривается модель типа Q # и описывается синтаксис указания и работы с типами.</span><span class="sxs-lookup"><span data-stu-id="0d891-104">This section lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="0d891-105">Обратите внимание, что Q # является *строго типизированным* языком, поэтому Аккуратное использование этих типов может помочь компилятору обеспечить строгую гарантию для программ Q # во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="0d891-105">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>

<span data-ttu-id="0d891-106">Чтобы обеспечить максимально возможную гарантию, преобразования между типами в Q # должны быть явными с помощью вызовов функций, которые выражают это преобразование.</span><span class="sxs-lookup"><span data-stu-id="0d891-106">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="0d891-107">Ряд таких функций предоставляется как часть пространства имен <xref:microsoft.quantum.convert>.</span><span class="sxs-lookup"><span data-stu-id="0d891-107">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="0d891-108">С другой стороны, операции приведения к совместимым типам происходят неявно.</span><span class="sxs-lookup"><span data-stu-id="0d891-108">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="0d891-109">Q # предоставляет оба типа-примитива, которые можно использовать напрямую, и различные способы создания новых типов из других типов.</span><span class="sxs-lookup"><span data-stu-id="0d891-109">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="0d891-110">В оставшейся части этого раздела мы рассмотрим каждую из них.</span><span class="sxs-lookup"><span data-stu-id="0d891-110">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="0d891-111">Примитивные типы</span><span class="sxs-lookup"><span data-stu-id="0d891-111">Primitive Types</span></span>

<span data-ttu-id="0d891-112">Язык Q # предоставляет несколько *простых типов*, из которых можно создавать другие типы:</span><span class="sxs-lookup"><span data-stu-id="0d891-112">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="0d891-113">Тип `Int` представляет собой 64-разрядное целое число со знаком, например: `2`, `107`, `-5`.</span><span class="sxs-lookup"><span data-stu-id="0d891-113">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="0d891-114">Тип `BigInt` представляет целое число со знаком произвольного размера, например `2L`, `107L`, `-5L`.</span><span class="sxs-lookup"><span data-stu-id="0d891-114">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="0d891-115">Этот тип основан на .NET <xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="0d891-115">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="0d891-116">Тип.</span><span class="sxs-lookup"><span data-stu-id="0d891-116">type.</span></span>
- <span data-ttu-id="0d891-117">Тип `Double` представляет число с плавающей запятой двойной точности, например: `0.0`, `-1.3`, `4e-7`.</span><span class="sxs-lookup"><span data-stu-id="0d891-117">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="0d891-118">Тип `Bool` представляет логическое значение, которое может быть как `true`, так и `false`.</span><span class="sxs-lookup"><span data-stu-id="0d891-118">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="0d891-119">Тип `Qubit` представляет тактовый бит или кубит.</span><span class="sxs-lookup"><span data-stu-id="0d891-119">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="0d891-120">`Qubit`ы непрозрачны для пользователя; единственной операцией с ними, кроме передачи их в другую операцию, является проверка удостоверения (равенство).</span><span class="sxs-lookup"><span data-stu-id="0d891-120">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="0d891-121">В конечном итоге действия с `Qubit`реализуются путем вызова внутренних инструкций в процессоре тактовой задержки (или модели).</span><span class="sxs-lookup"><span data-stu-id="0d891-121">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="0d891-122">Тип `Pauli` представляет один из четырех однокубитных операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="0d891-122">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="0d891-123">Этот тип используется для обозначения базовой операции для поворотов и для указания измеряемого наблюдаемого типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-123">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="0d891-124">Это перечислимый тип, имеющий четыре возможных значения: `PauliI`, `PauliX`, `PauliY`и `PauliZ`, которые являются константами типа `Pauli`.</span><span class="sxs-lookup"><span data-stu-id="0d891-124">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="0d891-125">Тип `Result` представляет результат измерения.</span><span class="sxs-lookup"><span data-stu-id="0d891-125">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="0d891-126">Это перечислимый тип с двумя возможными значениями: `One` и `Zero`, которые являются константами типа `Result`.</span><span class="sxs-lookup"><span data-stu-id="0d891-126">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="0d891-127">`Zero` указывает, что измерение + 1 еиженвалуео. `One` указывает на еиженвалуе-1.</span><span class="sxs-lookup"><span data-stu-id="0d891-127">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>
- <span data-ttu-id="0d891-128">Тип `Range` представляет последовательность целых чисел, обозначенную `start..step..stop`, где обозначаются параметры.</span><span class="sxs-lookup"><span data-stu-id="0d891-128">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is options.</span></span> 
   <span data-ttu-id="0d891-129">Это `start .. stop` соответствует `start..1..stop`, например, `1..2..7` представляет последовательность $\{1, 3, 5, 7\}$.</span><span class="sxs-lookup"><span data-stu-id="0d891-129">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="0d891-130">Тип `String` — это последовательность символов Юникода, которая непрозрачна для пользователя после создания.</span><span class="sxs-lookup"><span data-stu-id="0d891-130">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="0d891-131">Этот тип используется для передачи сообщений в классический узел в случае ошибки или диагностического события.</span><span class="sxs-lookup"><span data-stu-id="0d891-131">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="0d891-132">Тип `Unit` — это тип, который допускает только одно значение `()`.</span><span class="sxs-lookup"><span data-stu-id="0d891-132">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="0d891-133">Этот тип используется, чтобы указать, что функция Q # или операция не возвращает никаких сведений.</span><span class="sxs-lookup"><span data-stu-id="0d891-133">This type is used to indicate that Q# function or operation returns no information.</span></span> 

<span data-ttu-id="0d891-134">Константы `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`и `Zero` являются зарезервированными символами в Q #.</span><span class="sxs-lookup"><span data-stu-id="0d891-134">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="0d891-135">Типы массивов</span><span class="sxs-lookup"><span data-stu-id="0d891-135">Array Types</span></span>

<span data-ttu-id="0d891-136">Учитывая любой допустимый тип Q # `'T`, существует тип, представляющий массив значений типа `'T`.</span><span class="sxs-lookup"><span data-stu-id="0d891-136">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="0d891-137">Этот тип массива представлен как `'T[]`. Например, `Qubit[]` или `Int[][]`.</span><span class="sxs-lookup"><span data-stu-id="0d891-137">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="0d891-138">Например, коллекция целых чисел обозначается `Int[]`, а массив массивов `(Bool, Pauli)` значений обозначается `(Bool, Pauli)[][]`.</span><span class="sxs-lookup"><span data-stu-id="0d891-138">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="0d891-139">Во втором примере обратите внимание, что это может быть массив массивов массива, а не прямоугольный двумерный массив.</span><span class="sxs-lookup"><span data-stu-id="0d891-139">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="0d891-140">Q # не обеспечивает поддержку для прямоугольных многомерных массивов.</span><span class="sxs-lookup"><span data-stu-id="0d891-140">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="0d891-141">Значение массива может быть написано в исходном коде Q # с помощью квадратных скобок вокруг элементов массива, как в `[PauliI, PauliX, PauliY, PauliZ]`.</span><span class="sxs-lookup"><span data-stu-id="0d891-141">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="0d891-142">Тип литерала массива определяется общим базовым типом всех элементов массива.</span><span class="sxs-lookup"><span data-stu-id="0d891-142">The type of an array literal is determined by the common base type of all items in the array.</span></span> 

> [!WARNING]
> <span data-ttu-id="0d891-143">Элементы массива нельзя изменить после создания массива.</span><span class="sxs-lookup"><span data-stu-id="0d891-143">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="0d891-144">Для создания измененного массива можно использовать операторы обновления и повторного назначения, а также выражения копирования и обновления.</span><span class="sxs-lookup"><span data-stu-id="0d891-144">Update-and-reassign statements and/or copy-and-update expressions can be used to construct a modified array.</span></span>

<span data-ttu-id="0d891-145">Кроме того, массив можно создать из его размера с помощью ключевого слова `new`:</span><span class="sxs-lookup"><span data-stu-id="0d891-145">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="0d891-146">В любом случае, после создания массива можно использовать базовую функцию `Length`, чтобы получить количество элементов в виде `Int`.</span><span class="sxs-lookup"><span data-stu-id="0d891-146">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="0d891-147">Массивы могут быть вложенными в скрипты с помощью квадратных скобок, при этом подстрочные индексы имеют тип `Int` или Type `Range`, чтобы получить либо отдельные элементы, либо новые массивы, содержащие подмножество элементов массива.</span><span class="sxs-lookup"><span data-stu-id="0d891-147">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="0d891-148">Индексы массивов отсчитываются от нуля:</span><span class="sxs-lookup"><span data-stu-id="0d891-148">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="0d891-149">Типы кортежей</span><span class="sxs-lookup"><span data-stu-id="0d891-149">Tuple Types</span></span>

<span data-ttu-id="0d891-150">Если `T0`, `T1`,..., в соответствии с нулем или более разными типами, `Tn`, можно обозначить новый *тип кортежа* как `(T0, T1, ..., Tn)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-150">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="0d891-151">Типы, используемые для создания нового типа кортежа, могут быть кортежами, как в `(Int, (Qubit, Qubit))`.</span><span class="sxs-lookup"><span data-stu-id="0d891-151">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="0d891-152">Однако такое вложение всегда имеет конечное ограничение, так как типы кортежей не могут быть в каких-либо обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="0d891-152">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="0d891-153">Значения нового типа кортежа являются кортежами, сформированными последовательностями значений из каждого типа в кортеже.</span><span class="sxs-lookup"><span data-stu-id="0d891-153">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="0d891-154">Например, `(3, false)` является кортежем, типом которого является тип кортежа `(Int, Bool)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-154">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="0d891-155">Можно создавать массивы кортежей, кортежи массивов, кортежи подкортежей и т. д.</span><span class="sxs-lookup"><span data-stu-id="0d891-155">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="0d891-156">По отношению к Q # 0,3 `Unit` — имя *типа* пустого кортежа; `()` используется для пустого *значения*кортежа.</span><span class="sxs-lookup"><span data-stu-id="0d891-156">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="0d891-157">Экземпляры кортежей являются неизменяемыми.</span><span class="sxs-lookup"><span data-stu-id="0d891-157">Tuple instances are immutable.</span></span>
<span data-ttu-id="0d891-158">Q # не предоставляет механизм для изменения содержимого кортежа после его создания.</span><span class="sxs-lookup"><span data-stu-id="0d891-158">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="0d891-159">Кортежи — это мощная концепция, используемая в Q # для объединения значений в одно значение, что упрощает их передачу.</span><span class="sxs-lookup"><span data-stu-id="0d891-159">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="0d891-160">В частности, с помощью нотации кортежа можно выразить, что каждая операция и вызываемый метод принимают ровно один вход и возвращает ровно один результат.</span><span class="sxs-lookup"><span data-stu-id="0d891-160">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="0d891-161">Эквивалентность одноэлементного кортежа</span><span class="sxs-lookup"><span data-stu-id="0d891-161">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="0d891-162">Можно создать одноэлементный кортеж (с одним элементом), `('T1)`, например `(5)` или `([1,2,3])`.</span><span class="sxs-lookup"><span data-stu-id="0d891-162">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="0d891-163">Однако Q # обрабатывает одноэлементный кортеж как полностью эквивалентный значению заключенного в него типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-163">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="0d891-164">Это значит, что различия между `5` и `(5)`, а также между `5` и `(((5)))`или между `(5, (6))` и `(5, 6)`отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0d891-164">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>

<span data-ttu-id="0d891-165">Это эквивалентное действие применяется для всех целей, включая присваивание и выражения.</span><span class="sxs-lookup"><span data-stu-id="0d891-165">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="0d891-166">Это может быть так же, как и `(5)+3` для записи `5+3`, и оба выражения будут считаться `8`.</span><span class="sxs-lookup"><span data-stu-id="0d891-166">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>
<span data-ttu-id="0d891-167">В частности, это означает, что операция или функция, для которых Входной кортеж или тип выходного кортежа имеет одно поле, можно рассматривать как принимающий один аргумент или возвращая одно значение.</span><span class="sxs-lookup"><span data-stu-id="0d891-167">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="0d891-168">Мы будем называть это свойство _эквивалентностью одноэлементного кортежа_.</span><span class="sxs-lookup"><span data-stu-id="0d891-168">We refer to this property as _singleton tuple equivalence_.</span></span>

## <a name="user-defined-types"></a><span data-ttu-id="0d891-169">Определяемые пользователем типы</span><span class="sxs-lookup"><span data-stu-id="0d891-169">User-Defined Types</span></span>

<span data-ttu-id="0d891-170">Файл Q # может определять новый именованный тип, содержащий одно значение любого допустимого типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-170">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="0d891-171">Для любого типа кортежа `T`можно объявить новый определяемый пользователем тип, который является подтипом `T` с помощью инструкции `newtype`.</span><span class="sxs-lookup"><span data-stu-id="0d891-171">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="0d891-172">Например, в пространстве имен @"microsoft.quantum.canon" комплексные числа определяются как определяемые пользователем типы данных.</span><span class="sxs-lookup"><span data-stu-id="0d891-172">In the @"microsoft.quantum.canon" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```

<span data-ttu-id="0d891-173">Эта инструкция создает новый тип с двумя анонимными элементами типа `Double`.</span><span class="sxs-lookup"><span data-stu-id="0d891-173">This statement creates a new type with two anonymous items of type `Double`.</span></span>   
<span data-ttu-id="0d891-174">Помимо анонимных элементов, определяемые пользователем типы также поддерживают именованные элементы в Q # версии 0,7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0d891-174">Aside from anonymous items, user defined types also support named items as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="0d891-175">Например, можно назвать "to Items" `Re` для Double, представляющей реальную часть комплексного числа и `Im` для мнимой части:</span><span class="sxs-lookup"><span data-stu-id="0d891-175">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="0d891-176">Именование одного элемента в определяемом пользователем типе не подразумевает, что все элементы должны иметь имя — любое сочетание именованных и неименованных элементов поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0d891-176">Naming one item in a user defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="0d891-177">Кроме того, внутренние элементы могут называться.</span><span class="sxs-lookup"><span data-stu-id="0d891-177">Furthermore, also inner items may be named.</span></span>
<span data-ttu-id="0d891-178">Тип `Nested`, как определено ниже, имеет базовый тип `(Double, (Int, String))`, из которого называется только элемент типа `Int` и все остальные элементы являются анонимными.</span><span class="sxs-lookup"><span data-stu-id="0d891-178">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```
<span data-ttu-id="0d891-179">Именованные элементы имеют преимущество, доступ к которому можно получить напрямую с помощью оператора доступа `::`.</span><span class="sxs-lookup"><span data-stu-id="0d891-179">Named items have the advantage that they can be accessed directly via the access operator `::`.</span></span> 

```qsharp
function Addition (c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="0d891-180">Для доступа к анонимным элементам с другой стороны, сначала необходимо извлечь заключенное в оболочку значение с помощью постфиксного оператора `!`.</span><span class="sxs-lookup"><span data-stu-id="0d891-180">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="0d891-181">Оператор "Unwrap", `!`, позволяет извлекать значение, содержащееся в определяемом пользователем типе.</span><span class="sxs-lookup"><span data-stu-id="0d891-181">The "unwrap" operator, `!`, allows to extract the value contained in a user defined type.</span></span>
<span data-ttu-id="0d891-182">Тип такого выражения "Unwrap" является базовым типом определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-182">The type of such an "unwrap" expression is the underlying type of the user defined type.</span></span> 

```qsharp
function PrintMsg (value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="0d891-183">Оператор Unwrap разворачивает ровно один слой упаковки.</span><span class="sxs-lookup"><span data-stu-id="0d891-183">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="0d891-184">Для доступа к значению с множественной обтеканием можно использовать несколько операторов распаковки.</span><span class="sxs-lookup"><span data-stu-id="0d891-184">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="0d891-185">Например:</span><span class="sxs-lookup"><span data-stu-id="0d891-185">For instance:</span></span>

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

<span data-ttu-id="0d891-186">Дополнительные сведения см. в разделе о том, как [разносить выражения](xref:microsoft.quantum.language.expressions#unwrap-expressions) и [приоритеты операторов](xref:microsoft.quantum.language.expressions#operator-precedence) .</span><span class="sxs-lookup"><span data-stu-id="0d891-186">Take a look at the section on [unwrap expressions](xref:microsoft.quantum.language.expressions#unwrap-expressions) and [operators precedence](xref:microsoft.quantum.language.expressions#operator-precedence) for more details.</span></span>

<span data-ttu-id="0d891-187">Значения определяемого пользователем типа можно создать, вызвав соответствующий конструктор типа:</span><span class="sxs-lookup"><span data-stu-id="0d891-187">Values of a user defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="0d891-188">Кроме того, новые значения можно создавать из существующих с помощью [выражений копирования и обновления](xref:microsoft.quantum.language.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="0d891-188">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.language.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="0d891-189">Как и для массивов, такие выражения копируют все значения элементов исходного выражения, за исключением указанных именованных элементов.</span><span class="sxs-lookup"><span data-stu-id="0d891-189">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="0d891-190">Для этих значений задаются значения, определенные в правой части выражения.</span><span class="sxs-lookup"><span data-stu-id="0d891-190">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="0d891-191">Любые другие языковые конструкции, например [Операторы обновления и повторного назначения](xref:microsoft.quantum.language.statements#update-and-reassign-statement), доступные для элементов массива, существуют и для именованных элементов в определяемых пользователем типах.</span><span class="sxs-lookup"><span data-stu-id="0d891-191">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.language.statements#update-and-reassign-statement), that are available for array items exist for named-items in user defined types as well.</span></span>

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

<span data-ttu-id="0d891-192">Определяемые пользователем типы могут использоваться в любом месте, где можно использовать любой другой тип.</span><span class="sxs-lookup"><span data-stu-id="0d891-192">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="0d891-193">В частности, можно определить массив определяемого пользователем типа и включить определяемый пользователем тип как элемент типа кортежа.</span><span class="sxs-lookup"><span data-stu-id="0d891-193">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="0d891-194">Невозможно создать рекурсивные структуры типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-194">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="0d891-195">То есть тип, определяющий определяемый пользователем тип, не может быть типом кортежа, включающим элемент определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-195">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="0d891-196">Как правило, определяемые пользователем типы могут не иметь циклических зависимостей друг от друга, поэтому следующий набор определений типов будет недопустимым:</span><span class="sxs-lookup"><span data-stu-id="0d891-196">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```

<span data-ttu-id="0d891-197">Помимо простых псевдонимов для потенциально сложных типов кортежей, одно существенное преимущество определения таких типов заключается в том, что они могут документировать намерение определенного значения.</span><span class="sxs-lookup"><span data-stu-id="0d891-197">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="0d891-198">При возврате к примеру `Complex`один из них мог бы также определить двумерные полярные координаты как определяемый пользователем тип:</span><span class="sxs-lookup"><span data-stu-id="0d891-198">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="0d891-199">Несмотря на то, что оба `Complex` и `Polar` имеют базовый тип `(Double, Double)`, эти два типа полностью несовместимы в Q #, что сводит к минимуму риск случайного вызова сложной математической функции с полярными координатами и наоборот.</span><span class="sxs-lookup"><span data-stu-id="0d891-199">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="0d891-200">Таким образом, определяемые пользователем типы имеют аналогичную роль в качестве записей в F# , например.</span><span class="sxs-lookup"><span data-stu-id="0d891-200">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


## <a name="operation-and-function-types"></a><span data-ttu-id="0d891-201">Типы операций и функций</span><span class="sxs-lookup"><span data-stu-id="0d891-201">Operation and Function Types</span></span>

<span data-ttu-id="0d891-202">_Операция_ Q # — это подпрограмма-такт.</span><span class="sxs-lookup"><span data-stu-id="0d891-202">A Q# _operation_ is a quantum subroutine.</span></span>
<span data-ttu-id="0d891-203">То есть это вызываемая подпрограммы, которая содержит операции с тактовыми тактами.</span><span class="sxs-lookup"><span data-stu-id="0d891-203">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="0d891-204">_Функция_ Q # — это классическая подпрограмма, используемая в алгоритме такта.</span><span class="sxs-lookup"><span data-stu-id="0d891-204">A Q# _function_ is a classical subroutine used within a quantum algorithm.</span></span>
<span data-ttu-id="0d891-205">Он может содержать классический код, но не операции с тактовыми тактами.</span><span class="sxs-lookup"><span data-stu-id="0d891-205">It may contain classical code but no quantum operations.</span></span>
<span data-ttu-id="0d891-206">В частности, функции могут не выделять или позаимствовановать Кубитс, а также не могут вызывать операции.</span><span class="sxs-lookup"><span data-stu-id="0d891-206">Specifically, functions may not allocate or borrow qubits, nor may they call operations.</span></span>
<span data-ttu-id="0d891-207">Однако можно передать им операции или Кубитс для обработки.</span><span class="sxs-lookup"><span data-stu-id="0d891-207">It is possible, however, to pass them operations or qubits for processing.</span></span>
<span data-ttu-id="0d891-208">Таким образом, функции полностью детерминированы в том смысле, что их вызов с использованием одних и тех же аргументов всегда приводит к одинаковому результату.</span><span class="sxs-lookup"><span data-stu-id="0d891-208">Functions are thus entirely deterministic in the sense that calling them with the same arguments will always produce the same result.</span></span> 

<span data-ttu-id="0d891-209">Вместе операции и функции называются _вызываемыми_.</span><span class="sxs-lookup"><span data-stu-id="0d891-209">Together, operations and functions are called _callables_.</span></span>  <span data-ttu-id="0d891-210">Некоторые [примеры](#examples) приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="0d891-210">You can see some [examples](#examples) of these below.</span></span>

<span data-ttu-id="0d891-211">Все вызываемые команды Q # принимают одно значение в качестве входных данных и возвращают одно значение в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0d891-211">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="0d891-212">Входные и выходные значения могут быть кортежами.</span><span class="sxs-lookup"><span data-stu-id="0d891-212">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="0d891-213">Вызываемые, не возвращающие результатов `Unit`.</span><span class="sxs-lookup"><span data-stu-id="0d891-213">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="0d891-214">Вызываемые, не имеющие входных данных, принимают пустой кортеж в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="0d891-214">Callables that have no input take the empty tuple as input.</span></span>

<span data-ttu-id="0d891-215">Базовый тип для любого вызываемого типа записывается как `('Tinput => 'Tresult)` или `('Tinput -> 'Tresult)`, где оба `'Tinput` и `'Tresult` являются типами.</span><span class="sxs-lookup"><span data-stu-id="0d891-215">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="0d891-216">Первая форма с `=>`используется для операций. Вторая форма с `->`для функций.</span><span class="sxs-lookup"><span data-stu-id="0d891-216">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
<span data-ttu-id="0d891-217">Например, `((Qubit, Pauli) => Result)` представляет сигнатуру для возможной операции измерения с одним кубит.</span><span class="sxs-lookup"><span data-stu-id="0d891-217">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>

<span data-ttu-id="0d891-218">Типы функций полностью определяются их сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="0d891-218">Function types are completely specified by their signature.</span></span>
<span data-ttu-id="0d891-219">Например, функция, вычисляющая синус угла, будет иметь тип `(Double -> Double)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-219">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="0d891-220">Операции (но не функции) имеют определенные дополнительные _характеристики_ , которые выражаются как часть типа операции.</span><span class="sxs-lookup"><span data-stu-id="0d891-220">Operations—but not functions—have certain additional _characteristics_ that are expressed as part of the operation type.</span></span> <span data-ttu-id="0d891-221">Такие характеристики включают сведения о том, что операторов поддерживает операция.</span><span class="sxs-lookup"><span data-stu-id="0d891-221">Such characteristics include information about what functors the operation supports.</span></span>
<span data-ttu-id="0d891-222">Операторов являются мета-операциями, создающими специализацию базовой операции; см. [операторов](#functors)ниже.</span><span class="sxs-lookup"><span data-stu-id="0d891-222">Functors are meta-operations that generate a specialization of a base operation; see [Functors](#functors), below.</span></span>

<span data-ttu-id="0d891-223">Типы операций задаются типом входных данных, типом вывода и их характеристиками.</span><span class="sxs-lookup"><span data-stu-id="0d891-223">Operation types are specified by the their input type, output type, and their characteristics.</span></span>    
<span data-ttu-id="0d891-224">Чтобы обеспечить поддержку `Controlled` и (или) `Adjoint` функтор в типе операции, необходимо добавить аннотацию, указывающую соответствующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="0d891-224">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="0d891-225">Заметка `is Ctl` например, указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="0d891-225">An annotation `is Ctl` for example indicates that the operation is controllable.</span></span> <span data-ttu-id="0d891-226">Если требуется, чтобы операция этого типа поддерживала и `Adjoint`, и `Controlled` функтор, мы можем выразить это как `(Qubit => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-226">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="0d891-227">Используемые характеристики операции `Adj` и `Ctl` строго говорят — два предопределенных набора меток, где каждая метка указывает определенные характеристики операции, такие как, например, поддержка определенного функтор.</span><span class="sxs-lookup"><span data-stu-id="0d891-227">The used operation characteristics `Adj` and `Ctl` strictly speaking are two pre-defined sets of labels, where each label indicates a particular operation characteristics like e.g. support for a particular functor.</span></span>
<span data-ttu-id="0d891-228">Таким образом, `+` используется для указания объединения этих двух наборов, а `*` используется для указания пересечения, т. е. меток, общих для обоих наборов.</span><span class="sxs-lookup"><span data-stu-id="0d891-228">Hence, `+` is used to indicate the union of those two sets, and `*` is used to indicate the intersection - i.e. the labels that are common to both sets.</span></span>  

<span data-ttu-id="0d891-229">Например, операция `X` Паули имеет тип `(Qubit => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-229">For example, the Pauli `X` operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="0d891-230">Тип операции, который не поддерживает ни один операторов, задается только типом входного и выходного типа без дополнительной заметки.</span><span class="sxs-lookup"><span data-stu-id="0d891-230">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>


### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="0d891-231">Функции и операции с параметрами типа</span><span class="sxs-lookup"><span data-stu-id="0d891-231">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="0d891-232">Вызываемые типы могут содержать параметры типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-232">Callable types may contain type parameters.</span></span>
<span data-ttu-id="0d891-233">Параметры типа обозначаются символом, который предваряется одинарной кавычкой; Например, `'A` является допустимым параметром типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-233">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>

<span data-ttu-id="0d891-234">Параметр типа может присутствовать в одной сигнатуре более одного раза.</span><span class="sxs-lookup"><span data-stu-id="0d891-234">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="0d891-235">Например, функция, которая применяет другую функцию к каждому элементу массива и возвращает собранные результаты, будет иметь сигнатуру `(('A[], 'A->'A) -> 'A[])`.</span><span class="sxs-lookup"><span data-stu-id="0d891-235">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="0d891-236">Аналогично, функция, возвращающая композицию двух операций, может иметь сигнатуру `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span><span class="sxs-lookup"><span data-stu-id="0d891-236">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="0d891-237">При вызове вызываемого параметризованного типа все аргументы, имеющие один и тот же параметр типа, должны иметь один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="0d891-237">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="0d891-238">Q # не предоставляет механизм ограничения возможных типов, которые могут быть заменены для параметра типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-238">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

### <a name="type-compatibility"></a><span data-ttu-id="0d891-239">Совместимость типов</span><span class="sxs-lookup"><span data-stu-id="0d891-239">Type Compatibility</span></span>

<span data-ttu-id="0d891-240">Операция с поддержкой дополнительного операторов может использоваться в любом месте, где выполняется операция с меньшим числом операторов, но ожидается та же сигнатура.</span><span class="sxs-lookup"><span data-stu-id="0d891-240">An operation with additional functors supported may be used anywhere an operation with fewer functors but the same signature is expected.</span></span>
<span data-ttu-id="0d891-241">Например, операция типа `(Qubit => Unit is Adj)` может использоваться в любом месте, где ожидается операция типа `(Qubit => Unit)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-241">For instance, an operation of type `(Qubit => Unit is Adj)` may be used anywhere an operation of type `(Qubit => Unit)` is expected.</span></span>

<span data-ttu-id="0d891-242">Q # является ковариантным по отношению к вызываемым возвращаемым типам: вызываемый метод, возвращающий тип `'A` который совместим с вызываемым с тем же типом входных данных и типом результата, который `'A` совместим с.</span><span class="sxs-lookup"><span data-stu-id="0d891-242">Q# is covariant with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that `'A` is compatible with.</span></span>

<span data-ttu-id="0d891-243">Q # является контравариантным по отношению к входным типам: вызываемый тип, который принимает `'A` типа в качестве входных данных, совместим с вызываемым с тем же типом результата и типом входных данных, совместимым с `'A`.</span><span class="sxs-lookup"><span data-stu-id="0d891-243">Q# is contravariant with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="0d891-244">Это происходит при наличии следующих определений:</span><span class="sxs-lookup"><span data-stu-id="0d891-244">That is, given the following definitions:</span></span>

```qsharp
operation Invertible (qs : Qubit[]) : Unit 
is Adj {...} 
operation Unitary (qs : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertibleWith (
   inner: (Qubit[] => Unit is Adj),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith (
   inner: (Qubit[] => Unit is Adj + Ctl),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="0d891-245">выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="0d891-245">the following are true:</span></span>

- <span data-ttu-id="0d891-246">`ConjugateInvertibleWith` операции можно вызвать с аргументом `inner` либо `Invertible`, либо `Unitary`.</span><span class="sxs-lookup"><span data-stu-id="0d891-246">The operation `ConjugateInvertibleWith` may be invoked with an `inner` argument of either `Invertible` or `Unitary`.</span></span>
- <span data-ttu-id="0d891-247">`ConjugateUnitaryWith` операции можно вызвать с `inner` аргументом `Unitary`, но не `Invertible`.</span><span class="sxs-lookup"><span data-stu-id="0d891-247">The operation `ConjugateUnitaryWith` may be invoked with an `inner` argument of `Unitary`, but not `Invertible`.</span></span>
- <span data-ttu-id="0d891-248">Значение типа `(Qubit[] => Unit is Adj + Ctl)` может быть возвращено из `ConjugateInvertibleWith`.</span><span class="sxs-lookup"><span data-stu-id="0d891-248">A value of type `(Qubit[] => Unit is Adj + Ctl)` may be returned from `ConjugateInvertibleWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d891-249">В параметре Q # 0,3 появилась существенная разница в работе определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="0d891-249">Q# 0.3 introduces a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="0d891-250">Определяемые пользователем типы обрабатываются как упакованная версия базового типа, а не как подтип.</span><span class="sxs-lookup"><span data-stu-id="0d891-250">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="0d891-251">Это означает, что значение определяемого пользователем типа не может использоваться, если ожидается значение базового типа.</span><span class="sxs-lookup"><span data-stu-id="0d891-251">This means that a value of a user-defined type is not usable where a value of the underlying type is expected.</span></span>

### <a name="functors"></a><span data-ttu-id="0d891-252">Операторов</span><span class="sxs-lookup"><span data-stu-id="0d891-252">Functors</span></span>

<span data-ttu-id="0d891-253">Функтор в Q # — это фабрика, которая определяет новую операцию на основе другой операции.</span><span class="sxs-lookup"><span data-stu-id="0d891-253">A functor in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="0d891-254">Операторов имеет доступ к реализации базовой операции при определении реализации новой операции.</span><span class="sxs-lookup"><span data-stu-id="0d891-254">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="0d891-255">Таким же операторов может выполнять более сложные функции, чем традиционные функции более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="0d891-255">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span>

<span data-ttu-id="0d891-256">Операторов не имеют представления в системе типов Q #.</span><span class="sxs-lookup"><span data-stu-id="0d891-256">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="0d891-257">Таким образом, сейчас невозможно привязать их к переменной или передать в качестве аргументов.</span><span class="sxs-lookup"><span data-stu-id="0d891-257">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="0d891-258">Функтор используется, применяя его к операции, возвращая новую операцию.</span><span class="sxs-lookup"><span data-stu-id="0d891-258">A functor is used by applying it to an operation, returning a new operation.</span></span>
<span data-ttu-id="0d891-259">Например, операция, полученная в результате применения `Adjoint` функтор к операции `Y`, записывается как `Adjoint Y`.</span><span class="sxs-lookup"><span data-stu-id="0d891-259">For example, the operation that results from applying the `Adjoint` functor to the `Y` operation is written as `Adjoint Y`.</span></span>
<span data-ttu-id="0d891-260">Новая операция может быть затем вызвана как любая другая операция.</span><span class="sxs-lookup"><span data-stu-id="0d891-260">The new operation may then be invoked like any other operation.</span></span>
<span data-ttu-id="0d891-261">Таким же `Adjoint Y(q1)` применяет смежный функтор к операции `Y` для создания новой операции и применяет эту новую операцию к `q1`.</span><span class="sxs-lookup"><span data-stu-id="0d891-261">Thus, `Adjoint Y(q1)` applies the Adjoint functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>

<span data-ttu-id="0d891-262">Аналогичным образом `Controlled X(controls, target)` применяет контролируемый функтор к операции `X` для создания новой операции и применяет эту новую операцию к `controls` и `target`.</span><span class="sxs-lookup"><span data-stu-id="0d891-262">Similarly, `Controlled X(controls, target)` applies the Controlled functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

<span data-ttu-id="0d891-263">Два стандартных операторов в Q # `Adjoint` и `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="0d891-263">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

#### <a name="adjoint"></a><span data-ttu-id="0d891-264">Прилегающий</span><span class="sxs-lookup"><span data-stu-id="0d891-264">Adjoint</span></span>

<span data-ttu-id="0d891-265">В тактовых вычислениях смежная операция представляет собой комплексно сопряженное перестановку операции.</span><span class="sxs-lookup"><span data-stu-id="0d891-265">In quantum computing, the adjoint of an operation is the complex conjugate transpose of the operation.</span></span>
<span data-ttu-id="0d891-266">Для операций, которые реализуют единые операторы, прилегающим является обратная операция.</span><span class="sxs-lookup"><span data-stu-id="0d891-266">For operations that implement a unitary operator, the adjoint is the inverse of the operation.</span></span>
<span data-ttu-id="0d891-267">Для простой операции, которая просто вызывает последовательность других операций с набором Кубитс, можно вычислить соседнюю, применив аджоинтс подопераций к тому же Кубитс в обратный последовательности.</span><span class="sxs-lookup"><span data-stu-id="0d891-267">For a simple operation that just invokes a sequence of other unitary operations on a set of qubits, the adjoint may be computed by applying the adjoints of the sub-operations on the same qubits, in the reverse sequence.</span></span>

<span data-ttu-id="0d891-268">При наличии выражения операции новое выражение операции может быть сформировано с помощью `Adjoint` функтор.</span><span class="sxs-lookup"><span data-stu-id="0d891-268">Given an operation expression, a new operation expression may be formed using the `Adjoint` functor.</span></span>
<span data-ttu-id="0d891-269">Например, `Adjoint QFT` обозначает смежную операцию `QFT`.</span><span class="sxs-lookup"><span data-stu-id="0d891-269">For instance, `Adjoint QFT` designates the adjoint of the `QFT` operation.</span></span>
<span data-ttu-id="0d891-270">Новая операция имеет ту же сигнатуру и тип, что и базовая операция.</span><span class="sxs-lookup"><span data-stu-id="0d891-270">The new operation has the same signature and type as the base operation.</span></span>
<span data-ttu-id="0d891-271">В частности, новая операция также допускает `Adjoint`и позволяет `Controlled` только в том случае, если базовая операция была выполнена.</span><span class="sxs-lookup"><span data-stu-id="0d891-271">In particular, the new operation also allows `Adjoint`, and will allow `Controlled` if and only if the base operation did.</span></span>

<span data-ttu-id="0d891-272">Прилегающий функтор является собственным инверсией; то есть `Adjoint Adjoint Op` всегда совпадает с `Op`.</span><span class="sxs-lookup"><span data-stu-id="0d891-272">The Adjoint functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled"></a><span data-ttu-id="0d891-273">Управляет</span><span class="sxs-lookup"><span data-stu-id="0d891-273">Controlled</span></span>

<span data-ttu-id="0d891-274">Управляемая версия операции — это новая операция, которая фактически применяет базовую операцию только в том случае, если все элементы управления Кубитс находятся в указанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="0d891-274">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="0d891-275">Если элемент управления Кубитс в самом положении, то базовая операция применяется к соответствующей части детального размещения.</span><span class="sxs-lookup"><span data-stu-id="0d891-275">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="0d891-276">Поэтому управляемые операции часто используются для создания замкнутые.</span><span class="sxs-lookup"><span data-stu-id="0d891-276">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="0d891-277">В Q # управляемые версии всегда принимают массив элементов управления Кубитс, а заданное состояние всегда используется для всех Кубитс элементов управления, которые должны находиться в вычислительном (`PauliZ`) `One`ном состоянии, $ \кет{1}$.</span><span class="sxs-lookup"><span data-stu-id="0d891-277">In Q#, controlled versions always take an array of control qubits, and the specified state is always for all of the control qubits to be in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
<span data-ttu-id="0d891-278">Управление, основанное на других состояниях, можно получить, применив соответствующую единую операцию к элементу управления, Кубитс до управляемой операции, а затем применяя обратную операцию единой операции после управляемой операции.</span><span class="sxs-lookup"><span data-stu-id="0d891-278">Controlling based on other states may be achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
<span data-ttu-id="0d891-279">Например, применение операции `X` к элементу управления, кубит до и после управляемой операции, приведет к тому, что операция будет управлять состоянием `Zero` ($ \кет{0}$) для этого кубит; применение операции `H` до и после будет контролировать состояние `PauliX` `One`, то есть-1 еиженвалуе Паули X, $ \кет{-} \масрел{: =} (\кет{0}-\кет{1})/\скрт{2}$, а не `PauliZ` `One`.</span><span class="sxs-lookup"><span data-stu-id="0d891-279">For example, applying an `X` operation to a control qubit before and after a controlled operation will cause the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after will control on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="0d891-280">При наличии выражения операции новое выражение операции может быть сформировано с помощью `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="0d891-280">Given an operation expression, a new operation expression may be formed using the `Controlled` functor.</span></span>
<span data-ttu-id="0d891-281">Сигнатура новой операции основана на сигнатуре исходной операции.</span><span class="sxs-lookup"><span data-stu-id="0d891-281">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="0d891-282">Тип результата такой же, но тип входных данных — это кортеж с массивом кубит, содержащий элемент управления кубит в качестве первого элемента и аргументы исходной операции в качестве второго элемента.</span><span class="sxs-lookup"><span data-stu-id="0d891-282">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="0d891-283">Новая операция поддерживает `Controlled`и будет поддерживать `Adjoint` только в том случае, если была выполнена исходная операция.</span><span class="sxs-lookup"><span data-stu-id="0d891-283">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="0d891-284">Если исходная операция заняла только один аргумент, здесь будет прилагаться эквивалентность одноэлементного кортежа.</span><span class="sxs-lookup"><span data-stu-id="0d891-284">If the original operation took only a single argument, then singleton tuple equivalence will come into play here.</span></span>
<span data-ttu-id="0d891-285">Например, `Controlled X` является управляемой версией операции `X`.</span><span class="sxs-lookup"><span data-stu-id="0d891-285">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span>
<span data-ttu-id="0d891-286">`X` имеет тип `(Qubit => Unit is Adj + Ctl)`, поэтому `Controlled X` имеет тип `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; из-за равенства одноэлементных кортежей это то же самое, что `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-286">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="0d891-287">Если базовая операция заняла несколько аргументов, не забудьте заключить соответствующие аргументы управляемой версии операции в круглые скобки, чтобы преобразовать их в кортеж.</span><span class="sxs-lookup"><span data-stu-id="0d891-287">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="0d891-288">Например, `Controlled Rz` является управляемой версией операции `Rz`.</span><span class="sxs-lookup"><span data-stu-id="0d891-288">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span>
<span data-ttu-id="0d891-289">`Rz` имеет тип `((Double, Qubit) => Unit is Adj + Ctl)`, поэтому `Controlled Rz` имеет тип `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-289">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="0d891-290">Таким образом, `Controlled Rz(controls, (0.1, target))` будет действительным вызовом `Controlled Rz` (Обратите внимание на круглые скобки вокруг `0.1, target`).</span><span class="sxs-lookup"><span data-stu-id="0d891-290">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="0d891-291">Другой пример: `CNOT(control, target)` можно реализовать как `Controlled X([control], target)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-291">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="0d891-292">Если целевой объект должен управляться 2 Control Кубитс (ККНОТ), можно использовать оператор `Controlled X([control1, control2], target)`.</span><span class="sxs-lookup"><span data-stu-id="0d891-292">If a target should be controlled by 2 control qubits (CCNOT), we can use `Controlled X([control1, control2], target)` statement.</span></span>

### <a name="examples"></a><span data-ttu-id="0d891-293">Примеры</span><span class="sxs-lookup"><span data-stu-id="0d891-293">Examples</span></span>

<span data-ttu-id="0d891-294">Этот пример операции Q # взят из примера [измерения](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) .</span><span class="sxs-lookup"><span data-stu-id="0d891-294">This example of a Q# operation comes from the [Measurement](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) sample.</span></span> <span data-ttu-id="0d891-295">В рамках операций мы можем выделить Кубитс и использовать операции над такими Кубитс, как `H` и `X`:</span><span class="sxs-lookup"><span data-stu-id="0d891-295">Within operations, we can allocate qubits and use quantum operations on those qubits such as `H` and `X`:</span></span>

```qsharp
/// # Summary
/// Prepares a state and measures it in the Pauli-Z basis.
operation MeasureOneQubit () : Result {
        mutable result = Zero;

        using (qubit = Qubit()) { // Allocate a qubit
            H(qubit);               // Use a quantum operation on that qubit

            set result = M(qubit);      // Measure the qubit

            if (result == One) {    // Reset the qubit so that it can be released
                X(qubit);
            }

            return result;
        }
 }
```

<span data-ttu-id="0d891-296">Этот пример функции взят из примера [фасистиматион](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="0d891-296">This example of a function comes from the [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) sample.</span></span> <span data-ttu-id="0d891-297">Он содержит чисто классический код.</span><span class="sxs-lookup"><span data-stu-id="0d891-297">It contains purely classical code.</span></span> <span data-ttu-id="0d891-298">Вы видите, что, в отличие от приведенного выше примера, Кубитс не выделяется, а операции с тактами не используются.</span><span class="sxs-lookup"><span data-stu-id="0d891-298">You can see that, unlike the example above, no qubits are allocated, and no quantum operations are used.</span></span>


```qsharp
/// # Summary
/// Given two arrays, returns a new array that is the pointwise product
/// of each of the given arrays.
function MultiplyPointwise (left : Double[], right : Double[]) : Double[] {
    mutable product = new Double[Length(left)];

    for (idxElement in IndexRange(left)) {
        set product w/= idxElement <- left[idxElement] * right[idxElement];
    }
    return product;
}
```

<span data-ttu-id="0d891-299">Также возможно, что функция передается Кубитс для обработки, как в этом примере из примера [реверсиблелогиксинсесис](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) .</span><span class="sxs-lookup"><span data-stu-id="0d891-299">It is also possible for a function to be passed qubits for processing, as in this example from the [ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) sample.</span></span> <span data-ttu-id="0d891-300">Кубитс передаются функции и используются для обработки, хотя ни одна из них не изменила кубит состояния.</span><span class="sxs-lookup"><span data-stu-id="0d891-300">Qubits are passed to the function and used for processing, although at no point are the qubit states themselves modified.</span></span>

```qsharp
/// # Summary
/// Translate MCT masks into multiple-controlled Toffoli gates (with single
/// targets).
function GateMasksToToffoliGates (qubits : Qubit[], masks : MCMTMask[]) : MCTGate[] {

    mutable result = new MCTGate[0];
    let n = Length(qubits);

    for (i in 0 .. Length(masks) - 1) {
        let (controls, targets) = (masks[i])!;
        let controlBits = IntegerBits(controls, n);
        let targetBits = IntegerBits(targets, n);
        let cQubits = Subarray(controlBits, qubits);
        let tQubits = Subarray(targetBits, qubits);

        for (target in tQubits) {
            set result += [MCTGate(cQubits, target)];
        }
    }

    return result;
}
```
