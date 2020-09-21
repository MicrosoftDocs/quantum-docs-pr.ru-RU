---
title: Типы в Q#
description: Сведения о различных типах, используемых в Q# языке программирования.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- Q#
- $$v
ms.openlocfilehash: c4a3e6563b8cabee87d1db6b9cb1c1f1c1a7131b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835831"
---
# <a name="types-in-no-locq"></a><span data-ttu-id="adcbb-103">Типы в Q#</span><span class="sxs-lookup"><span data-stu-id="adcbb-103">Types in Q#</span></span>

<span data-ttu-id="adcbb-104">В этой статье описывается Q# модель типов и синтаксис для указания типов и работы с ними.</span><span class="sxs-lookup"><span data-stu-id="adcbb-104">This article describes the Q# type model and the syntax for specifying and working with types.</span></span> <span data-ttu-id="adcbb-105">Дополнительные сведения о создании выражений этих типов и работе с ними см. в разделе [выражения типов](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="adcbb-105">For details on how to create and operate on expressions of these types, see [Type Expressions](xref:microsoft.quantum.guide.expressions).</span></span>

<span data-ttu-id="adcbb-106">Обратите внимание, что Q# является *строго типизированным* языком, так что Аккуратное использование этих типов может помочь компилятору обеспечить строгую гарантию для Q# программ во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="adcbb-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="adcbb-107">Чтобы обеспечить максимально возможную гарантию, преобразования между типами в Q# должны быть явными с помощью вызовов функций, которые выражают это преобразование.</span><span class="sxs-lookup"><span data-stu-id="adcbb-107">To provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> 
<span data-ttu-id="adcbb-108">Q# предоставляет множество таких функций, как часть <xref:microsoft.quantum.convert> пространства имен.</span><span class="sxs-lookup"><span data-stu-id="adcbb-108">Q# provides a variety of such functions as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="adcbb-109">С другой стороны, операции приведения к совместимым типам происходят неявно.</span><span class="sxs-lookup"><span data-stu-id="adcbb-109">Upcasts to compatible types, on the other hand, happen implicitly.</span></span> 

<span data-ttu-id="adcbb-110">Q# предоставляет оба типа-примитива, которые используются напрямую, и различные способы создания новых типов из других типов.</span><span class="sxs-lookup"><span data-stu-id="adcbb-110">Q# provides both primitive types, which are used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="adcbb-111">В оставшейся части этой статьи мы рассмотрим каждую из них.</span><span class="sxs-lookup"><span data-stu-id="adcbb-111">We describe each in the rest of this article.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="adcbb-112">Примитивные типы</span><span class="sxs-lookup"><span data-stu-id="adcbb-112">Primitive Types</span></span>

<span data-ttu-id="adcbb-113">Q#Язык предоставляет следующие типы- *примитивы*, которые можно использовать непосредственно в Q# программах.</span><span class="sxs-lookup"><span data-stu-id="adcbb-113">The Q# language provides the following *primitive types*, all of which you can use directly in Q# programs.</span></span> <span data-ttu-id="adcbb-114">Эти примитивные типы также можно использовать для создания новых типов.</span><span class="sxs-lookup"><span data-stu-id="adcbb-114">You can also use these primitive types to construct new types.</span></span>

- <span data-ttu-id="adcbb-115">`Int`Тип представляет 64-разрядное целое число со знаком, например,, `2` `107` `-5` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-115">The `Int` type represents a 64-bit signed integer, for example, `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="adcbb-116">`BigInt`Тип представляет целое число со знаком произвольного размера, например, `2L` , `107L` , `-5L` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-116">The `BigInt` type represents a signed integer of arbitrary size, for example, `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="adcbb-117">Этот тип основан на .NET <xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="adcbb-117">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="adcbb-118">Java.</span><span class="sxs-lookup"><span data-stu-id="adcbb-118">type.</span></span>

- <span data-ttu-id="adcbb-119">`Double`Тип представляет число с плавающей запятой двойной точности, например,, `0.0` `-1.3` `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-119">The `Double` type represents a double-precision floating-point number, for example, `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="adcbb-120">`Bool`Тип представляет логическое значение либо `true` `false` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-120">The `Bool` type represents a Boolean value of either `true` or `false`.</span></span>
- <span data-ttu-id="adcbb-121">`Range`Тип представляет последовательность целых чисел, обозначенную параметром `start..step..stop` , где указание шага является необязательным.</span><span class="sxs-lookup"><span data-stu-id="adcbb-121">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="adcbb-122">Например, `start .. stop` соответствует `start..1..stop` , и `1..2..7` представляет последовательность $ \{ 1, 3, 5, 7 \} $.</span><span class="sxs-lookup"><span data-stu-id="adcbb-122">For example, `start .. stop` corresponds to `start..1..stop`, and `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="adcbb-123">`String`Тип — это последовательность символов Юникода, которая непрозрачна для пользователя после создания.</span><span class="sxs-lookup"><span data-stu-id="adcbb-123">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="adcbb-124">Используйте `string` тип для передачи сообщений на классический узел в случае ошибки или диагностического события.</span><span class="sxs-lookup"><span data-stu-id="adcbb-124">Use the `string` type to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="adcbb-125">`Unit`Тип может иметь только одно значение, `()` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-125">The `Unit` type can have only one value, `()`.</span></span> 
  <span data-ttu-id="adcbb-126">Используйте этот тип, чтобы указать, что Q# функция или операция не возвращает никакой информации.</span><span class="sxs-lookup"><span data-stu-id="adcbb-126">Use this type to indicate that a Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="adcbb-127">`Qubit`Тип представляет тактовый бит или кубит.</span><span class="sxs-lookup"><span data-stu-id="adcbb-127">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="adcbb-128">`Qubit`непрозрачны для пользователя.</span><span class="sxs-lookup"><span data-stu-id="adcbb-128">`Qubit`s are opaque to the user.</span></span> <span data-ttu-id="adcbb-129">Единственной операцией с ними, кроме передачи их в другую операцию, является проверка удостоверения (равенство).</span><span class="sxs-lookup"><span data-stu-id="adcbb-129">The only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="adcbb-130">В конечном итоге, вы реализуете действия в с `Qubit` помощью вызова внутренних инструкций для процессора тактовой задержки (или имитатора такта).</span><span class="sxs-lookup"><span data-stu-id="adcbb-130">Ultimately, you implement actions on `Qubit`s by calling intrinsic instructions on a quantum processor (or a quantum simulator).</span></span>
- <span data-ttu-id="adcbb-131">`Pauli`Тип представляет один из четырех однокубитых операторов Паули.</span><span class="sxs-lookup"><span data-stu-id="adcbb-131">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="adcbb-132">Используйте этот тип, чтобы обозначить базовую операцию для поворотов и указать измеряемый наблюдаемый объект.</span><span class="sxs-lookup"><span data-stu-id="adcbb-132">Use this type to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="adcbb-133">Это перечислимый тип, имеющий четыре возможных значения: `PauliI` , `PauliX` , `PauliY` и, которые `PauliZ` являются константами типа `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-133">It is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="adcbb-134">`Result`Тип представляет результат измерения.</span><span class="sxs-lookup"><span data-stu-id="adcbb-134">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="adcbb-135">Это перечислимый тип с двумя возможными значениями: `One` и `Zero` , которые являются константами типа `Result` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-135">It is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="adcbb-136">`Zero` Указывает, что был измерен + 1 еиженвалуе; `One` указывает, что еиженвалуе-1 был измерен.</span><span class="sxs-lookup"><span data-stu-id="adcbb-136">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue was measured.</span></span>

<span data-ttu-id="adcbb-137">Константы,,,,,, `true` `false` `PauliI` `PauliX` `PauliY` `PauliZ` `One` и `Zero` являются зарезервированными символами в Q# .</span><span class="sxs-lookup"><span data-stu-id="adcbb-137">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="adcbb-138">Типы массивов</span><span class="sxs-lookup"><span data-stu-id="adcbb-138">Array Types</span></span>

* <span data-ttu-id="adcbb-139">Для любого допустимого Q# типа существует тип, представляющий массив значений этого типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-139">For any valid Q# type, there is a type that represents an array of values of that type.</span></span>
    <span data-ttu-id="adcbb-140">Например, `Qubit[]` и `(Bool, Pauli)[]` представляют массивы `Qubit` значений и `(Bool, Pauli)` значений кортежей.</span><span class="sxs-lookup"><span data-stu-id="adcbb-140">For example, `Qubit[]` and `(Bool, Pauli)[]` represent arrays of `Qubit` values and `(Bool, Pauli)` tuple values.</span></span>

* <span data-ttu-id="adcbb-141">Массив массивов также является допустимым.</span><span class="sxs-lookup"><span data-stu-id="adcbb-141">An array of arrays is also valid.</span></span> <span data-ttu-id="adcbb-142">Развернув предыдущий пример, вы `(Bool, Pauli)` обозначаете массив массивов `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-142">Expanding on the previous example, an array of `(Bool, Pauli)` arrays is denoted `(Bool, Pauli)[][]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="adcbb-143">Этот пример, `(Bool, Pauli)[][]` представляет потенциально неровный массив массивов, а не прямоугольный двумерный массив.</span><span class="sxs-lookup"><span data-stu-id="adcbb-143">This example, `(Bool, Pauli)[][]`, represents a potentially jagged array of arrays and not a rectangular two-dimensional array.</span></span> <span data-ttu-id="adcbb-144">Q# не поддерживает прямоугольные многомерные массивы.</span><span class="sxs-lookup"><span data-stu-id="adcbb-144">Q# does not support rectangular multi-dimensional arrays.</span></span>

* <span data-ttu-id="adcbb-145">Значение массива может быть записано в Q# исходном коде с помощью квадратных скобок вокруг элементов массива, как в `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-145">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="adcbb-146">Общий базовый тип всех элементов массива определяет тип литерала массива.</span><span class="sxs-lookup"><span data-stu-id="adcbb-146">The common base type of all items in the array determines the type of an array literal.</span></span> <span data-ttu-id="adcbb-147">Таким образом, создание массива с элементами, не имеющими общего базового типа, вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="adcbb-147">Hence, constructing an array with elements that have no common base type raises an error.</span></span>  
<span data-ttu-id="adcbb-148">Пример см. в разделе [массивы вызываемых элементов](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span><span class="sxs-lookup"><span data-stu-id="adcbb-148">For an example, see [arrays of callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span></span>

    > [!WARNING]
    > <span data-ttu-id="adcbb-149">После создания элементы массива не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="adcbb-149">Once created, the elements of an array cannot be changed.</span></span>
    > <span data-ttu-id="adcbb-150">Для создания измененного массива используйте [инструкции UPDATE-и-reassignя](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) или [выражения копирования и обновления](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="adcbb-150">To construct a modified array, use [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span>

* <span data-ttu-id="adcbb-151">Кроме того, массив можно создать из его размера с помощью `new` ключевого слова:</span><span class="sxs-lookup"><span data-stu-id="adcbb-151">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* <span data-ttu-id="adcbb-152">Используйте функцию Core, `Length` чтобы получить количество элементов массива в виде `Int` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-152">Use the core function `Length` to obtain the number of elements from an array as an `Int`.</span></span>
* <span data-ttu-id="adcbb-153">Массивы могут быть вложенными в скрипт, чтобы получить либо отдельные элементы, либо новые массивы, содержащие подмножество элементов массива.</span><span class="sxs-lookup"><span data-stu-id="adcbb-153">Arrays can be subscripted to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="adcbb-154">Индексы массивов отсчитываются от нуля и должны иметь тип `Int` или тип `Range` :</span><span class="sxs-lookup"><span data-stu-id="adcbb-154">The subscripts of arrays are zero-based and must be type `Int` or type `Range`:</span></span>

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a><span data-ttu-id="adcbb-155">Типы кортежей</span><span class="sxs-lookup"><span data-stu-id="adcbb-155">Tuple Types</span></span>

<span data-ttu-id="adcbb-156">Кортежи — это мощная концепция, используемая в процессе объединения Q# значений в одно значение, что упрощает их передачу.</span><span class="sxs-lookup"><span data-stu-id="adcbb-156">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="adcbb-157">В частности, с помощью нотации кортежа можно выразить, что каждая операция и вызываемый метод принимают ровно один вход и возвращает ровно один результат.</span><span class="sxs-lookup"><span data-stu-id="adcbb-157">In particular, using tuple notation, you can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

* <span data-ttu-id="adcbb-158">Если указано ноль или более различных типов, `T0` `T1` ,..., `Tn` можно обозначить новый  *тип кортежа* как `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-158">Given zero or more different types `T0`, `T1`, ..., `Tn`, you can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="adcbb-159">Типы, используемые для создания нового типа кортежа, могут быть кортежами, как в `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-159">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="adcbb-160">Однако такое вложение всегда имеет конечное ограничение, так как типы кортежей не могут быть в каких-либо обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="adcbb-160">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

* <span data-ttu-id="adcbb-161">Значения нового типа кортежа являются кортежами, сформированными последовательностями значений из каждого типа в кортеже.</span><span class="sxs-lookup"><span data-stu-id="adcbb-161">The values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="adcbb-162">Например, `(3, false)` — это кортеж, тип которого является типом кортежа `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-162">For example, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="adcbb-163">Можно создавать массивы кортежей, кортежи массивов, кортежи подкортежей и т. д.</span><span class="sxs-lookup"><span data-stu-id="adcbb-163">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, and so on.</span></span>

* <span data-ttu-id="adcbb-164">Начиная с Q# 0,3 `Unit` — это имя *типа* пустого кортежа; `()` используется для *значения* пустого кортежа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-164">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the *value* of the empty tuple.</span></span>

* <span data-ttu-id="adcbb-165">Экземпляры кортежей являются неизменяемыми.</span><span class="sxs-lookup"><span data-stu-id="adcbb-165">Tuple instances are immutable.</span></span>
<span data-ttu-id="adcbb-166">Q# не предоставляет механизм для изменения содержимого кортежа после его создания.</span><span class="sxs-lookup"><span data-stu-id="adcbb-166">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>



### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="adcbb-167">Эквивалентность одноэлементного кортежа</span><span class="sxs-lookup"><span data-stu-id="adcbb-167">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="adcbb-168">Можно создать одноэлементный кортеж (с одним элементом) `('T1)` , например `(5)` или `([1,2,3])` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-168">It is possible to create a singleton (single-element) tuple `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="adcbb-169">Однако Q# обрабатывает одноэлементный кортеж как эквивалентный значению заключенного в него типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-169">However, Q# treats a singleton tuple as equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="adcbb-170">Это значит, что различия между and и OR между and и `5` `(5)` `5` `(((5)))` `(5, (6))` `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-170">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="adcbb-171">Его можно написать так же, `(5)+3` как и для записи `5+3` ; оба выражения имеют значение `8` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-171">It is just as valid to write `(5)+3` as it is to write `5+3`; both expressions evaluate to `8`.</span></span>

<span data-ttu-id="adcbb-172">Это эквивалентное действие применяется для всех целей, включая присваивание и выражения.</span><span class="sxs-lookup"><span data-stu-id="adcbb-172">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="adcbb-173">При наличии любого выражения такое же выражение, заключенное в круглые скобки, является выражением того же типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-173">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="adcbb-174">Например, `(7)` выражение типа `Int` , `([1,2,3])` является выражением типа `Int[]` , а `((1,2))` является выражением типа `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-174">For example, `(7)` is an expression of type `Int`, `([1,2,3])` is an expression of type `Int[]`, and `((1,2))` is an expression of type `(Int, Int)`.</span></span>

<span data-ttu-id="adcbb-175">В частности, это означает, что вы можете просмотреть операцию или функцию, у которых Входной кортеж или тип выходного кортежа имеет одно поле, которое принимает один аргумент или возвращает одно значение.</span><span class="sxs-lookup"><span data-stu-id="adcbb-175">In particular, this means that you can view an operation or function whose input tuple or output tuple type has one field as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="adcbb-176">Мы будем называть это свойство _эквивалентностью одноэлементного кортежа_.</span><span class="sxs-lookup"><span data-stu-id="adcbb-176">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="adcbb-177">Определяемые пользователем типы</span><span class="sxs-lookup"><span data-stu-id="adcbb-177">User-Defined Types</span></span>

<span data-ttu-id="adcbb-178">Объявление определяемого пользователем типа состоит из ключевого слова `newtype` , за которым следует имя определяемого пользователем типа, тип `=` , допустимая спецификация типа и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="adcbb-178">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="adcbb-179">Пример:</span><span class="sxs-lookup"><span data-stu-id="adcbb-179">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* <span data-ttu-id="adcbb-180">Каждый Q# исходный файл может объявлять любое количество определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="adcbb-180">Each Q# source file may declare any number of user-defined types.</span></span>
* <span data-ttu-id="adcbb-181">Имена типов должны быть уникальными в пределах пространства имен и могут не конфликтовать с именами операций и функций.</span><span class="sxs-lookup"><span data-stu-id="adcbb-181">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>
* <span data-ttu-id="adcbb-182">Определяемые пользователем типы различаются, даже если базовые типы идентичны.</span><span class="sxs-lookup"><span data-stu-id="adcbb-182">User-defined types are distinct, even if the base types are identical.</span></span>
<span data-ttu-id="adcbb-183">В частности, не существует автоматического преобразования между значениями двух определяемых пользователем типов, даже если базовые типы идентичны.</span><span class="sxs-lookup"><span data-stu-id="adcbb-183">In particular, there is no automatic conversion between the values of two user-defined types, even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="adcbb-184">Сравнение именованных и анонимных элементов</span><span class="sxs-lookup"><span data-stu-id="adcbb-184">Named vs. anonymous items</span></span>

<span data-ttu-id="adcbb-185">Q#Файл может определять новый именованный тип, содержащий одно значение любого допустимого типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-185">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="adcbb-186">Для любого типа кортежа `T` можно объявить новый определяемый пользователем тип, который является подтипом `T` с `newtype` инструкцией.</span><span class="sxs-lookup"><span data-stu-id="adcbb-186">For any tuple type `T`, you can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="adcbb-187">@"microsoft.quantum.math"Например, в пространстве имен в качестве определяемого пользователем типа определены комплексные числа:</span><span class="sxs-lookup"><span data-stu-id="adcbb-187">In the @"microsoft.quantum.math" namespace, for example, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="adcbb-188">Эта инструкция создает новый тип с двумя анонимными элементами типа `Double` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-188">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="adcbb-189">Помимо анонимных элементов, определяемые пользователем типы также поддерживают *именованные элементы* Q# версии 0,7 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="adcbb-189">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="adcbb-190">Например, можно присвоить элементам имя `Real` Double, представляющей реальную часть комплексного числа и `Imag` для мнимой части:</span><span class="sxs-lookup"><span data-stu-id="adcbb-190">For example, you could name the items to `Real` for the double representing the real part of a complex number and `Imag` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Real : Double, Imag : Double);
```
<span data-ttu-id="adcbb-191">Именование одного элемента в определяемом пользователем типе не подразумевает, что все элементы должны иметь имя — любое сочетание именованных и неименованных элементов поддерживается.</span><span class="sxs-lookup"><span data-stu-id="adcbb-191">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="adcbb-192">Кроме того, внутренние элементы также могут называться.</span><span class="sxs-lookup"><span data-stu-id="adcbb-192">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="adcbb-193">Тип `Nested` , как определено ниже, имеет базовый тип `(Double, (Int, String))` , для которого только элемент типа `Int` имеет имя, а все остальные элементы являются анонимными.</span><span class="sxs-lookup"><span data-stu-id="adcbb-193">The type `Nested`, as defined below for example, has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named, and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="adcbb-194">Именованные элементы имеют преимущество, доступ к которому можно получить напрямую с помощью *оператора доступа* `::` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-194">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Real + c2::Real, c1::Imag + c2::Imag);
}
```

<span data-ttu-id="adcbb-195">Помимо простых псевдонимов для потенциально сложных типов кортежей, значительное преимущество определения таких типов заключается в том, что они могут документировать намерение определенного значения.</span><span class="sxs-lookup"><span data-stu-id="adcbb-195">In addition to providing short aliases for potentially complicated tuple types, a significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="adcbb-196">При возврате к примеру `Complex` , один из них мог бы также определить полярную координату репресенатион в качестве определяемого пользователем типа:</span><span class="sxs-lookup"><span data-stu-id="adcbb-196">Returning to the example of `Complex`, one could have also defined a polar coordinate represenation as a user-defined type:</span></span>

```qsharp
newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```

<span data-ttu-id="adcbb-197">Хотя оба типа `Complex` и `ComplexPolar` оба имеют базовый тип `(Double, Double)` , эти два типа полностью несовместимы в, что Q# минимизирует риск случайного вызова сложной математической функции с полярными координатами и наоборот.</span><span class="sxs-lookup"><span data-stu-id="adcbb-197">Even though both `Complex` and `ComplexPolar` both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="adcbb-198">Доступ к анонимным элементам с помощью оператора Unwrap</span><span class="sxs-lookup"><span data-stu-id="adcbb-198">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="adcbb-199">Чтобы получить доступ к анонимным элементам, сначала извлеките упакованное значение с помощью постфиксного оператора `!` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-199">To access anonymous items, first extract the wrapped value using the postfix operator `!`.</span></span>
<span data-ttu-id="adcbb-200">С помощью оператора "Unwrap" `!` можно извлечь значение, содержащееся в определяемом пользователем типе.</span><span class="sxs-lookup"><span data-stu-id="adcbb-200">With the "unwrap" operator, `!`, you can extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="adcbb-201">Тип такого выражения "Unwrap" является базовым типом определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-201">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="adcbb-202">Один неупакованный Оператор разворачивает один слой упаковки.</span><span class="sxs-lookup"><span data-stu-id="adcbb-202">A single unwrap operator unwraps one layer of wrapping.</span></span> <span data-ttu-id="adcbb-203">Для доступа к значению с множественной обтеканием используйте несколько операторов Unwrap.</span><span class="sxs-lookup"><span data-stu-id="adcbb-203">Use multiple unwrap operators to access a multiply-wrapped value.</span></span>

<span data-ttu-id="adcbb-204">Пример:</span><span class="sxs-lookup"><span data-stu-id="adcbb-204">For example:</span></span>

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

<span data-ttu-id="adcbb-205">Дополнительные сведения о операторе Unwrap см. [в разделе выражения типа Q# в ](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="adcbb-205">For more details on the unwrap operator, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="adcbb-206">Создание значений определяемых пользователем типов</span><span class="sxs-lookup"><span data-stu-id="adcbb-206">Creating values of user-defined types</span></span>

<span data-ttu-id="adcbb-207">Создайте значения определяемого пользователем типа, вызвав соответствующий конструктор типа:</span><span class="sxs-lookup"><span data-stu-id="adcbb-207">Create values of a user-defined type by calling the corresponding type constructor:</span></span>

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="adcbb-208">Кроме того, можно создавать новые значения из существующих с помощью [выражений копирования и обновления](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="adcbb-208">Alternatively, you can create new values from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="adcbb-209">Точно так же, как и с массивами, выражения копирования и обновления копируют все значения элементов исходного выражения, за исключением указанных именованных элементов.</span><span class="sxs-lookup"><span data-stu-id="adcbb-209">Just as they do with arrays, copy-and-update expressions copy all item values of the original expression, except for the specified named items.</span></span> <span data-ttu-id="adcbb-210">Для этих исключений значения этих элементов являются значениями, определенными в правой части выражения.</span><span class="sxs-lookup"><span data-stu-id="adcbb-210">For these exceptions, the values of these items are the values defined on the right-hand side of the expression.</span></span> <span data-ttu-id="adcbb-211">Любые другие языковые конструкции, доступные для элементов массива, например [Операторы обновления и повторного назначения](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), существуют и для именованных элементов в определяемых пользователем типах.</span><span class="sxs-lookup"><span data-stu-id="adcbb-211">Any other language constructs that are available for array items, for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), exist for named-items in user-defined types as well.</span></span>

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

* <span data-ttu-id="adcbb-212">Определяемые пользователем типы можно использовать в любом месте, где используются любые другие типы.</span><span class="sxs-lookup"><span data-stu-id="adcbb-212">You can use user-defined types anywhere you use any other types.</span></span>
<span data-ttu-id="adcbb-213">В частности, можно определить массив определяемого пользователем типа и включить определяемый пользователем тип как элемент типа кортежа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-213">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

* <span data-ttu-id="adcbb-214">Невозможно создать рекурсивные структуры типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-214">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="adcbb-215">То есть тип, определяющий определяемый пользователем тип, не может быть кортежным типом, включающим элемент определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-215">That is, the type that defines a user-defined type cannot be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="adcbb-216">В общем, определяемые пользователем типы могут не иметь циклических зависимостей друг от друга, поэтому следующий набор определений типов является недопустимым:</span><span class="sxs-lookup"><span data-stu-id="adcbb-216">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions are invalid:</span></span>

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a><span data-ttu-id="adcbb-217">Типы операций и функций</span><span class="sxs-lookup"><span data-stu-id="adcbb-217">Operation and Function Types</span></span>

<span data-ttu-id="adcbb-218">С учетом типов `'Tinput` и `'Tresult` :</span><span class="sxs-lookup"><span data-stu-id="adcbb-218">Given the types `'Tinput` and `'Tresult`:</span></span>

* <span data-ttu-id="adcbb-219">`('Tinput => 'Tresult)` — Это базовый тип для любой *операции*, например `((Qubit, Pauli) => Result)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-219">`('Tinput => 'Tresult)` is the basic type for any *operation*, for example `((Qubit, Pauli) => Result)`.</span></span>
* <span data-ttu-id="adcbb-220">`('Tinput -> 'Tresult)` — Это базовый тип для любой *функции*, например `(Int -> Int)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-220">`('Tinput -> 'Tresult)` is the basic type for any *function*, for example `(Int -> Int)`.</span></span> 

<span data-ttu-id="adcbb-221">Они называются *сигнатурой* вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="adcbb-221">These are called the *signature* of the callable.</span></span>

* <span data-ttu-id="adcbb-222">Все Q# вызываемые команды принимают одно значение в качестве входных данных и возвращают одно значение в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="adcbb-222">All Q# callables take a single value as input and return a single value as output.</span></span>
* <span data-ttu-id="adcbb-223">Кортежи можно использовать как для входных, так и для выходных значений.</span><span class="sxs-lookup"><span data-stu-id="adcbb-223">You can use tuples for both the input and output values.</span></span>
* <span data-ttu-id="adcbb-224">Вызываемые, которые не имеют результата, возвращают `Unit` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-224">Callables that have no result, return `Unit`.</span></span>
* <span data-ttu-id="adcbb-225">Вызываемые, не имеющие входных данных, принимают пустой кортеж в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="adcbb-225">Callables that have no input take the empty tuple as input.</span></span>

### <a name="functors"></a><span data-ttu-id="adcbb-226">Операторов</span><span class="sxs-lookup"><span data-stu-id="adcbb-226">Functors</span></span>

<span data-ttu-id="adcbb-227">Типы *функций* полностью определяются их сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="adcbb-227">*Function* types are completely specified by their signature.</span></span> <span data-ttu-id="adcbb-228">Например, функция, вычисляющая синус угла, будет иметь тип `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-228">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span> 

<span data-ttu-id="adcbb-229">*Операции* имеют определенные дополнительные характеристики, которые выражаются как часть типа операции.</span><span class="sxs-lookup"><span data-stu-id="adcbb-229">*Operations* have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="adcbb-230">Такие характеристики включают сведения о том, какие *операторов* поддерживаются операцией.</span><span class="sxs-lookup"><span data-stu-id="adcbb-230">Such characteristics include information about which *functors* the operation supports.</span></span>
<span data-ttu-id="adcbb-231">Например, если выполнение операции зависит от состояния других Кубитс, то оно должно поддерживать `Controlled` функтор; если операция имеет обратный, она должна поддерживать `Adjoint` функтор.</span><span class="sxs-lookup"><span data-stu-id="adcbb-231">For example, if the running of the operation relies on the state of other qubits, then it should support the `Controlled` functor; if the operation has an inverse, then it should support the `Adjoint` functor.</span></span>

> [!NOTE]
> <span data-ttu-id="adcbb-232">В этой статье обсуждается только, как операторов изменяет подпись операции.</span><span class="sxs-lookup"><span data-stu-id="adcbb-232">This article only discuss how functors alter the operation signature.</span></span> <span data-ttu-id="adcbb-233">Дополнительные сведения о операторов и операциях см. [в разделе операции и Q# функции в ](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="adcbb-233">For more details about functors and operations, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span> 

<span data-ttu-id="adcbb-234">Чтобы требовать поддержку для `Controlled` и/или `Adjoint` функтор в типе операции, необходимо добавить заметку, указывающую соответствующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="adcbb-234">To require support for the `Controlled` and/or `Adjoint` functor in an operation type, you need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="adcbb-235">Аннотация `is Ctl` (например, `(Qubit => Unit is Ctl)` ) указывает, что операция является управляемой.</span><span class="sxs-lookup"><span data-stu-id="adcbb-235">The annotation `is Ctl` (for example, `(Qubit => Unit is Ctl)`) indicates that the operation is controllable.</span></span> <span data-ttu-id="adcbb-236">Это значит, что его выполнение зависит от состояния другого кубит или Кубитс.</span><span class="sxs-lookup"><span data-stu-id="adcbb-236">That is, its run relies on the state of another qubit or qubits.</span></span> <span data-ttu-id="adcbb-237">Аналогичным образом, заметка `is Adj` указывает, что операция имеет смежное значение, то есть может быть "инвертированным", чтобы успешно применить операцию, а затем ее примыкающую к состоянию оставляет состояние без изменений.</span><span class="sxs-lookup"><span data-stu-id="adcbb-237">Similarly, the annotation `is Adj` indicates that the operation has an adjoint, that is, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="adcbb-238">Если требуется, чтобы операция этого типа поддерживала `Adjoint` и `Controlled` функтор, можно выразить это как `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-238">If you want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor you can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="adcbb-239">Например, встроенная <xref:microsoft.quantum.intrinsic.x> Операция Паули имеет тип `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-239">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="adcbb-240">Тип операции, который не поддерживает ни один операторов, задается только типом входного и выходного типа без дополнительной заметки.</span><span class="sxs-lookup"><span data-stu-id="adcbb-240">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="adcbb-241">Функции и операции с параметрами типа</span><span class="sxs-lookup"><span data-stu-id="adcbb-241">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="adcbb-242">Вызываемые типы могут содержать *Параметры типа*.</span><span class="sxs-lookup"><span data-stu-id="adcbb-242">Callable types may contain *type parameters*.</span></span>
<span data-ttu-id="adcbb-243">Используйте символ, обозначенный префиксом одинарной кавычки, для обозначения параметра типа; Например, является допустимым `'A` параметром типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-243">Use a symbol prefixed by a single quote to indicated a type parameter; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="adcbb-244">Дополнительные сведения и сведения о том, как определять вызываемые параметрами типа, см. [в разделе операции и Q# функции в ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span><span class="sxs-lookup"><span data-stu-id="adcbb-244">For more information and details on how to define type-parameterized callables, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span></span>

<span data-ttu-id="adcbb-245">Параметр типа может присутствовать в одной сигнатуре более одного раза.</span><span class="sxs-lookup"><span data-stu-id="adcbb-245">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="adcbb-246">Например, функция, которая применяет другую функцию к каждому элементу массива и возвращает собранные результаты, имеет сигнатуру `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-246">For example, a function that applies another function to each element of an array and returns the collected results has the signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="adcbb-247">Аналогично, функция, возвращающая композицию двух операций, имеет сигнатуру `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="adcbb-247">Similarly, a function that returns the composition of two operations has the signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="adcbb-248">При вызове вызываемого параметризованного типа все аргументы, имеющие один и тот же параметр типа, должны иметь один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="adcbb-248">When you invoke a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="adcbb-249">Q# не предоставляет механизм ограничения возможных типов, которые пользователь может заменить параметром типа.</span><span class="sxs-lookup"><span data-stu-id="adcbb-249">Q# does not provide a mechanism for constraining the possible types that a user might substitute for a type parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="adcbb-250">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="adcbb-250">Next steps</span></span>

<span data-ttu-id="adcbb-251">Теперь, когда вы видели все типы Q# , составляющие язык, см. раздел [Expression types в Q# ](xref:microsoft.quantum.guide.expressions) , чтобы научиться создавать и манипулировать выражениями этих различных типов.</span><span class="sxs-lookup"><span data-stu-id="adcbb-251">Now that you've seen all the types which comprise the Q# language, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to learn how to create and manipulate expressions of these various types.</span></span>
