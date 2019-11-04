---
title: Структура файла | Документация Майкрософт
description: 'Q # файл структура'
author: QuantumWriter
uid: microsoft.quantum.language.file-structure
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 40b2e7ddf5def6285250dffe130b152429dce1f8
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185194"
---
# <a name="file-structure"></a><span data-ttu-id="74065-103">Структура файла</span><span class="sxs-lookup"><span data-stu-id="74065-103">File Structure</span></span>

<span data-ttu-id="74065-104">Файл Q # состоит из последовательности объявлений пространств имен.</span><span class="sxs-lookup"><span data-stu-id="74065-104">A Q# file consists of a sequence of namespace declarations.</span></span>
<span data-ttu-id="74065-105">Каждое объявление пространства имен содержит объявления для определяемых пользователем типов, операций и функций.</span><span class="sxs-lookup"><span data-stu-id="74065-105">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="74065-106">Объявление пространства имен может содержать любое количество объявлений каждого типа и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="74065-106">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="74065-107">Единственный текст, который может находиться за пределами объявления пространства имен, — это комментарии.</span><span class="sxs-lookup"><span data-stu-id="74065-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="74065-108">В частности, комментарии к документации для пространства имен предшествуют объявлению.</span><span class="sxs-lookup"><span data-stu-id="74065-108">In particular, documentation comments for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="74065-109">Объявления пространств имен</span><span class="sxs-lookup"><span data-stu-id="74065-109">Namespace Declarations</span></span>

<span data-ttu-id="74065-110">Как правило, файл Q # содержит только одно объявление пространства имен, но может содержать пустое значение (и быть пустым или содержать только комментарии) или может включать несколько пространств имен.</span><span class="sxs-lookup"><span data-stu-id="74065-110">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="74065-111">Объявления пространств имен не могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="74065-111">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="74065-112">Одно и то же пространство имен может быть объявлено в нескольких файлах Q #, компилируемых вместе, при условии, что отсутствуют объявления типов, операций или функций с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="74065-112">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="74065-113">В частности, нельзя определить один и тот же тип в одном пространстве имен в нескольких файлах, даже если объявления идентичны.</span><span class="sxs-lookup"><span data-stu-id="74065-113">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="74065-114">Объявление пространства имен состоит из ключевого слова `namespace`, за которым следует имя пространства имен, `{`открывающая скобка, объявления, содержащиеся в пространстве имен, и закрывающая фигурная скобка `}`.</span><span class="sxs-lookup"><span data-stu-id="74065-114">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="74065-115">Имена пространств имен соответствуют шаблону .NET последовательности из одного или нескольких юридических символов, разделенных точками `.`.</span><span class="sxs-lookup"><span data-stu-id="74065-115">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="74065-116">Например, `MyQuantumStuff` и `Microsoft.Quantum.Canon` являются допустимыми именами пространств имен.</span><span class="sxs-lookup"><span data-stu-id="74065-116">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Canon` are valid namespace names.</span></span>
<span data-ttu-id="74065-117">По соглашению символы в имени пространства имен записываются прописными буквами, но это не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="74065-117">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="74065-118">Объявления могут располагаться в любом порядке в объявлении пространства имен.</span><span class="sxs-lookup"><span data-stu-id="74065-118">Declarations may appear in any order in a namespace declaration.</span></span>
<span data-ttu-id="74065-119">Ссылки на типы или вызываемые объекты, объявленные ниже в файле, разрешаются правильно. нет необходимости в объявлении типа, операции или функции перед ссылкой на нее.</span><span class="sxs-lookup"><span data-stu-id="74065-119">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="74065-120">Открытые директивы</span><span class="sxs-lookup"><span data-stu-id="74065-120">Open Directives</span></span>

<span data-ttu-id="74065-121">В блоке пространства имен директива `open` может использоваться для импорта всех типов и вызываемых в определенное пространство имен, а также для обращения к ним по их неполному имени.</span><span class="sxs-lookup"><span data-stu-id="74065-121">Within a namespace block, the `open` directive may be used to import all types and callables defined in a certain namespace and refer to them by their unqualified name.</span></span> 

<span data-ttu-id="74065-122">Такая директива `open` состоит из ключевого слова `open`, за которым следует открытое пространство имен и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="74065-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

<span data-ttu-id="74065-123">Например,</span><span class="sxs-lookup"><span data-stu-id="74065-123">For instance,</span></span>

```qsharp
open Microsoft.Quantum.Canon;
```

<span data-ttu-id="74065-124">Кроме того, можно определить короткое имя для открытого пространства имен таким, чтобы все элементы из этого пространства имен могли уточняться определенным коротким именем.</span><span class="sxs-lookup"><span data-stu-id="74065-124">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="74065-125">Это короткое имя определяется путем добавления ключевого слова `as` за которым следует требуемое короткое имя перед точкой с запятой в директиве `open`:</span><span class="sxs-lookup"><span data-stu-id="74065-125">Such a short name is defined by adding the keyword `as` followed by the desired short name before the semicolon in an `open` directive:</span></span>

```qsharp
open Microsoft.Quantum.Math as Math;
```

<span data-ttu-id="74065-126">Все директивы `open` должны располагаться перед объявлениями `function`, `operation`или `newtype` в блоке пространства имен.</span><span class="sxs-lookup"><span data-stu-id="74065-126">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>
<span data-ttu-id="74065-127">Директива `open` применяется ко всему блоку пространства имен в файле.</span><span class="sxs-lookup"><span data-stu-id="74065-127">The `open` directive applies to the entire namespace block within a file.</span></span>

## <a name="user-defined-type-declarations"></a><span data-ttu-id="74065-128">Объявления определяемого пользователем типа</span><span class="sxs-lookup"><span data-stu-id="74065-128">User-Defined Type Declarations</span></span>

<span data-ttu-id="74065-129">Q # предоставляет пользователям возможность объявлять новые определяемые пользователем типы, как описано в разделе " [модель типов Q #](xref:microsoft.quantum.language.type-model) ".</span><span class="sxs-lookup"><span data-stu-id="74065-129">Q# provides a way for users to declare new user-defined types, as described in the [Q# type model](xref:microsoft.quantum.language.type-model) section.</span></span>
<span data-ttu-id="74065-130">Определяемые пользователем типы различаются, даже если базовые типы идентичны.</span><span class="sxs-lookup"><span data-stu-id="74065-130">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="74065-131">В частности, нет автоматического преобразования между значениями двух определяемых пользователем типов, даже если базовые типы идентичны.</span><span class="sxs-lookup"><span data-stu-id="74065-131">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

<span data-ttu-id="74065-132">Объявление определяемого пользователем типа состоит из ключевого слова `newtype`, за которым следует имя определяемого пользователем типа, `=`, допустимая спецификация типа и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="74065-132">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="74065-133">Пример.</span><span class="sxs-lookup"><span data-stu-id="74065-133">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="74065-134">Каждый исходный файл Q # может объявлять любое количество определяемых пользователем типов.</span><span class="sxs-lookup"><span data-stu-id="74065-134">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="74065-135">Имена типов должны быть уникальными в пределах пространства имен и могут не конфликтовать с именами операций и функций.</span><span class="sxs-lookup"><span data-stu-id="74065-135">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="74065-136">Невозможно определить циклические зависимости между определяемыми пользователем типами.</span><span class="sxs-lookup"><span data-stu-id="74065-136">It is not possible to define circular dependencies between user defined types.</span></span> <span data-ttu-id="74065-137">Поэтому рекурсивные типы невозможны в Q #.</span><span class="sxs-lookup"><span data-stu-id="74065-137">Recursive types are thus not possible within Q#.</span></span>

## <a name="operation-declarations"></a><span data-ttu-id="74065-138">Объявления операций</span><span class="sxs-lookup"><span data-stu-id="74065-138">Operation Declarations</span></span>

<span data-ttu-id="74065-139">Операции — это ядро Q #, примерно аналогичное функциям на других языках.</span><span class="sxs-lookup"><span data-stu-id="74065-139">Operations are the core of Q#, roughly analogous to functions in other languages.</span></span>
<span data-ttu-id="74065-140">Каждый исходный файл Q # может определять любое количество операций.</span><span class="sxs-lookup"><span data-stu-id="74065-140">Each Q# source file may define any number of operations.</span></span>

<span data-ttu-id="74065-141">Имена операций должны быть уникальными в пределах пространства имен и могут не конфликтовать с именами типа и функции.</span><span class="sxs-lookup"><span data-stu-id="74065-141">Operation names must be unique within a namespace and may not conflict with type and function names.</span></span>

<span data-ttu-id="74065-142">Объявления операций состоят из ключевого слова `operation`, за которым следует символ, который представляет собой имя операции, кортеж типизированного идентификатора, определяющий аргументы для операции, двоеточие `:`, аннотацию типа, описывающую тип результата операции. При необходимости заметка с характеристиками операции, открывающая фигурная скобка `{`, текст объявления операции и окончательная закрывающая фигурная скобка `}`.</span><span class="sxs-lookup"><span data-stu-id="74065-142">An operation declarations consists of the keyword `operation`, followed by the symbol that is the operation’s name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation’s result type, optionally an annotation with the operation characteristics, an open brace `{`, the body of the operation declaration, and a final closing brace `}`.</span></span>

<span data-ttu-id="74065-143">Тело объявления операции либо состоит из реализации по умолчанию, либо списка специализаций.</span><span class="sxs-lookup"><span data-stu-id="74065-143">The body of the operation declaration either consists of the default implementation or of a list of specializations.</span></span>
<span data-ttu-id="74065-144">Реализация по умолчанию может быть указана непосредственно в объявлении, если только реализация специализации тела по умолчанию должна быть явно указана.</span><span class="sxs-lookup"><span data-stu-id="74065-144">The default implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to specified explicitly.</span></span>
<span data-ttu-id="74065-145">В этом случае заметка с характеристиками операций в объявлении полезна для обеспечения автоматического создания компилятором других специализаций на основе реализации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="74065-145">In this case, an annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="74065-146">Например:</span><span class="sxs-lookup"><span data-stu-id="74065-146">For example</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

<span data-ttu-id="74065-147">Характеристики операции определяют типы операторов, которые могут быть применены к объявленной операции, и их воздействие.</span><span class="sxs-lookup"><span data-stu-id="74065-147">Operation characteristics define what kinds of functors can be applied to the declared operation, and what effect they have.</span></span> <span data-ttu-id="74065-148">Если операция реализует единое преобразование, можно определить, как работает операция при *аджоинтед* или *управлении*.</span><span class="sxs-lookup"><span data-stu-id="74065-148">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span>
<span data-ttu-id="74065-149">Существование этих специализаций можно объявить как часть сигнатуры операции.</span><span class="sxs-lookup"><span data-stu-id="74065-149">The existence of these specializations can be declared as part of the operation signature.</span></span> <span data-ttu-id="74065-150">Затем соответствующая реализация для каждой такой неявно объявленной специализации создается компилятором.</span><span class="sxs-lookup"><span data-stu-id="74065-150">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> <span data-ttu-id="74065-151">В приведенном выше примере компилятор создает смежную, управляемую и управляемую соседнюю специализацию.</span><span class="sxs-lookup"><span data-stu-id="74065-151">In the example above, an adjoint, a controlled, and a controlled adjoint specialization are generated by the compiler.</span></span> 

<span data-ttu-id="74065-152">В случае, если реализация не может быть создана компилятором, ее можно указать явно.</span><span class="sxs-lookup"><span data-stu-id="74065-152">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="74065-153">Такие явные объявления специализации могут либо состоять из подходящей директивы поколения, поясняющей, как должна быть построена определенная специализация, или пользовательской реализации.</span><span class="sxs-lookup"><span data-stu-id="74065-153">Such explicit specialization declarations can either consist of a suitable generation directive that clarify how a certain specialization is to be built, or a user defined implementation.</span></span> <span data-ttu-id="74065-154">Код в `PrepareEntangledPair` выше, например, эквивалентен приведенному ниже коду, содержащему явные объявления специализации:</span><span class="sxs-lookup"><span data-stu-id="74065-154">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="74065-155">Ключевое слово `auto` указывает, что компилятор должен определить способ создания реализации специализации.</span><span class="sxs-lookup"><span data-stu-id="74065-155">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="74065-156">Если компилятор не может создать реализацию для определенной специализации без дальнейших инструкций, например более точной директивы создания, или если можно предоставить более эффективную реализацию, то реализация может быть также определена вручную.</span><span class="sxs-lookup"><span data-stu-id="74065-156">If the compiler cannot generate the implementation for a certain specialization without further instructions - like a more precise generation directive -, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```

<span data-ttu-id="74065-157">В приведенном выше примере `adjoint invert;` указывает, что примыкающая специализация должна быть создана путем инвертирования реализации тела, а `controlled adjoint invert;` указывает, что управляемая примыкающая специализация должна быть создана путем инвертирования данной реализации элемента управления контролируемая специализация.</span><span class="sxs-lookup"><span data-stu-id="74065-157">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="74065-158">Чтобы операция поддерживала приложение `Adjoint` и (или) `Controlled` функтор, необходимо `Unit`его возвращаемый тип.</span><span class="sxs-lookup"><span data-stu-id="74065-158">For an operation to support application of the `Adjoint` and/or `Controlled` functor, its return type necessarily needs to be `Unit`.</span></span> 


### <a name="explicit-specialization-declarations"></a><span data-ttu-id="74065-159">Явные объявления специализации</span><span class="sxs-lookup"><span data-stu-id="74065-159">Explicit Specialization Declarations</span></span>

<span data-ttu-id="74065-160">Операции Q # могут содержать следующие явные объявления специализаций:</span><span class="sxs-lookup"><span data-stu-id="74065-160">Q# operations may contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="74065-161">Специализация `body` указывает реализацию операции без применения операторов.</span><span class="sxs-lookup"><span data-stu-id="74065-161">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="74065-162">`adjoint` Специализация определяет реализацию операции с применением `Adjoint` функтор.</span><span class="sxs-lookup"><span data-stu-id="74065-162">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="74065-163">`controlled` Специализация определяет реализацию операции с применением `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="74065-163">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="74065-164">`controlled adjoint`ная Специализация определяет реализацию операции с применением `Adjoint` и `Controlled` операторов.</span><span class="sxs-lookup"><span data-stu-id="74065-164">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="74065-165">Эта специализация также может называться `adjoint controlled`, так как две операторов работы.</span><span class="sxs-lookup"><span data-stu-id="74065-165">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="74065-166">Специализация операции состоит из тега специализации (например, `body`или `adjoint`и т. д.), за которым следует одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="74065-166">An operation specialization consists of the specialization tag (like e.g. `body`, or `adjoint`, etc.) followed by one of:</span></span>

- <span data-ttu-id="74065-167">Явное объявление, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="74065-167">An explicit declaration as described below.</span></span>
- <span data-ttu-id="74065-168">Директива, сообщающая компилятору, как создать специализацию, одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="74065-168">A directive that tells the compiler how to generate the specialization, one of:</span></span>
  - <span data-ttu-id="74065-169">`intrinsic`, что указывает на то, что специализация предоставляется целевым компьютером.</span><span class="sxs-lookup"><span data-stu-id="74065-169">`intrinsic`, which indicates that the specialization is provided by the target machine.</span></span>
  - <span data-ttu-id="74065-170">`distribute`, который можно использовать с специализациями `controlled` и `controlled adjoint`.</span><span class="sxs-lookup"><span data-stu-id="74065-170">`distribute`, which may be used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="74065-171">При использовании с `controlled`указывает, что компилятор должен вычислить специализацию, применяя `Controlled` ко всем операциям в `body`.</span><span class="sxs-lookup"><span data-stu-id="74065-171">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="74065-172">При использовании с `controlled adjoint`указывает, что компилятор должен вычислить специализацию, применяя `Controlled` ко всем операциям в специализации `adjoint`.</span><span class="sxs-lookup"><span data-stu-id="74065-172">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="74065-173">`invert`, которое указывает, что компилятор должен вычислять специализацию `adjoint` путем обращения `body`, т. е. Порядок операций и применение прилегающих к каждому из них.</span><span class="sxs-lookup"><span data-stu-id="74065-173">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, i.e. reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="74065-174">При использовании с `adjoint controlled`это означает, что компилятор должен вычислить специализацию, инверсию специализации `controlled`.</span><span class="sxs-lookup"><span data-stu-id="74065-174">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="74065-175">`self`, чтобы указать, что прилегающий специализации совпадает с специализацией `body`.</span><span class="sxs-lookup"><span data-stu-id="74065-175">`self`, to indicate that the adjoint specialization is the the same as the `body` specialization.</span></span>
    <span data-ttu-id="74065-176">Это допустимо для `adjoint` и `adjoint controlled`ных специализаций.</span><span class="sxs-lookup"><span data-stu-id="74065-176">This is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="74065-177">Для `adjoint controlled``self` подразумевает, что специализация `adjoint controlled` совпадает с специализацией `controlled`.</span><span class="sxs-lookup"><span data-stu-id="74065-177">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="74065-178">`auto`, чтобы указать, что компилятор должен выбрать соответствующую директиву для применения.</span><span class="sxs-lookup"><span data-stu-id="74065-178">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="74065-179">`auto` не может использоваться для специализации `body`.</span><span class="sxs-lookup"><span data-stu-id="74065-179">`auto` may not be used for the `body` specialization.</span></span>

<span data-ttu-id="74065-180">Для директив и `auto` все требуются закрывающие `;`с точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="74065-180">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="74065-181">Директива `auto` разрешается в следующую директиву поколения, если предоставлено явное объявление `body`:</span><span class="sxs-lookup"><span data-stu-id="74065-181">The `auto` directive resolves to the following generation directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="74065-182">`adjoint` специализация создается в соответствии с директивой `invert`.</span><span class="sxs-lookup"><span data-stu-id="74065-182">The `adjoint` specialization is generated according to the directive `invert`.</span></span>
- <span data-ttu-id="74065-183">`controlled` специализация создается в соответствии с директивой `distribute`.</span><span class="sxs-lookup"><span data-stu-id="74065-183">The `controlled` specialization is generated according to the directive `distribute`.</span></span>
- <span data-ttu-id="74065-184">`adjoint controlled`ная специализация создается в соответствии с директивой `invert`, если явное объявление для `controlled` задано, но не одно для `adjoint`, и `distribute` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="74065-184">The `adjoint controlled` specialization is generated according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="74065-185">Если операция является самопримыкающей, явно укажите либо примыкающую, либо управляемую соседнюю специализацию с помощью директивы поколения `self`, чтобы компилятор использовал эту информацию в целях оптимизации.</span><span class="sxs-lookup"><span data-stu-id="74065-185">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="74065-186">Объявление специализации, содержащее определенную пользователем реализацию, состоит из кортежа аргументов, за которым следует блок операторов с кодом Q #, реализующим специализацию.</span><span class="sxs-lookup"><span data-stu-id="74065-186">A specialization declaration containing a user defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="74065-187">В списке аргументов `...` используется для представления аргументов, объявленных для операции в целом.</span><span class="sxs-lookup"><span data-stu-id="74065-187">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="74065-188">Для `body` и `adjoint`список аргументов всегда должен быть `(...)`. для `controlled` и `adjoint controlled`список аргументов должен быть символом, представляющим массив элемента управления Кубитс, за которым следует `...`, заключенный в круглые скобки; Например, `(controls,...)`.</span><span class="sxs-lookup"><span data-stu-id="74065-188">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

<span data-ttu-id="74065-189">Если необходимо явно объявить одну или несколько специализаций, кроме тела по умолчанию, то реализация тела по умолчанию должна быть заключена в подходящее объявление специализации:</span><span class="sxs-lookup"><span data-stu-id="74065-189">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qs: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (q in qs) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="adjoint"></a><span data-ttu-id="74065-190">Прилегающий</span><span class="sxs-lookup"><span data-stu-id="74065-190">Adjoint</span></span>

<span data-ttu-id="74065-191">Смежная операция указывает, как реализуется комплексно сопряженное преобразование операции, т. е. как работает операция при выполнении операции "выполнить в обратную".</span><span class="sxs-lookup"><span data-stu-id="74065-191">The adjoint of an operation specifies how the complex conjugate transpose of the operation is implemented, i.e. how the operation acts when "run in reverse".</span></span>
<span data-ttu-id="74065-192">Допускается указание операции без примыкающего; Например, операции измерения не имеют примыкающих, так как они необратимы.</span><span class="sxs-lookup"><span data-stu-id="74065-192">It is legal to specify an operation with no adjoint; for instance, measurement operations have no adjoint because they are not invertible.</span></span>
<span data-ttu-id="74065-193">Операция поддерживает `Adjoint` функтор, если ее объявление содержит неявное или неявное объявление примыкающей специализации.</span><span class="sxs-lookup"><span data-stu-id="74065-193">An operation supports the `Adjoint` functor if its declaration contains an implicit or explicit declaration of an adjoint specialization.</span></span>
<span data-ttu-id="74065-194">Объявленная непосредственно управляемая примыкающая специализация подразумевает существование примыкающей специализации.</span><span class="sxs-lookup"><span data-stu-id="74065-194">An explicitly declared controlled adjoint specialization implies the existence of an adjoint specialization.</span></span> 

<span data-ttu-id="74065-195">Для операции, текст которой содержит циклы повтора, инструкции SET, измерения, операторы Return или вызовы других операций, которые не поддерживают `Adjoint` функтор, автоматическое создание примыкающей специализации после `invert` или @no__ Невозможная директива t_2_.</span><span class="sxs-lookup"><span data-stu-id="74065-195">For operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

### <a name="controlled"></a><span data-ttu-id="74065-196">Управляет</span><span class="sxs-lookup"><span data-stu-id="74065-196">Controlled</span></span>

<span data-ttu-id="74065-197">Управляемая версия операции указывает, как реализуется версия операции, управляемой тактовым генератором, т. е. как работает операция при условии применения условия в состоянии регистра такта.</span><span class="sxs-lookup"><span data-stu-id="74065-197">The controlled version of an operation specifies how a quantum-controlled version of the operation is implemented, i.e. how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="74065-198">Более полное описание приведено в разделе [Управление](xref:microsoft.quantum.language.type-model#controlled) .</span><span class="sxs-lookup"><span data-stu-id="74065-198">A more complete description is provided in the [Controlled](xref:microsoft.quantum.language.type-model#controlled) section.</span></span>

<span data-ttu-id="74065-199">Допускается указание операции без контролируемой версии; Например, операции измерения не имеют контролируемой версии, так как они не являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="74065-199">It is legal to specify an operation with no controlled version; for instance, measurement operations have no controlled version because they are not controllable.</span></span>
<span data-ttu-id="74065-200">Операция поддерживает `Controlled` функтор только в том случае, если ее объявление содержит неявное или явное объявление управляемой специализации.</span><span class="sxs-lookup"><span data-stu-id="74065-200">An operation supports the `Controlled` functor if and only if its declaration contains an implicit or explicit declaration of a controlled specialization.</span></span>
<span data-ttu-id="74065-201">Объявленная в явном виде управляемая примыкающая специализация подразумевает наличие управляемой специализации.</span><span class="sxs-lookup"><span data-stu-id="74065-201">An explicitly declared controlled adjoint specialization implies the existence of a controlled specialization.</span></span> 

<span data-ttu-id="74065-202">Для операции, текст которой содержит вызовы других операций, не поддерживающих `Controlled` функтор, автоматическое создание управляемой специализации после директивы `distribute` или `auto` невозможно.</span><span class="sxs-lookup"><span data-stu-id="74065-202">For an operation whose body contains calls to other operations that does not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

### <a name="controlled-adjoint"></a><span data-ttu-id="74065-203">Управляемый соседний</span><span class="sxs-lookup"><span data-stu-id="74065-203">Controlled Adjoint</span></span>

<span data-ttu-id="74065-204">Управляемая смежная версия операции указывает, как реализуется зависящая от такта версия смежной операции.</span><span class="sxs-lookup"><span data-stu-id="74065-204">The controlled adjoint version of an operation specifies how a quantum-controlled version of the adjoint of the operation is implemented.</span></span>
<span data-ttu-id="74065-205">Допускается указание операции без управляемой примыкающей версии; Например, операции измерения не имеют контролируемой версии, так как они не являются управляемыми и необратимыми.</span><span class="sxs-lookup"><span data-stu-id="74065-205">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="74065-206">Управляемая примыкающая специализация для операции должна существовать только в том случае, если существует и смежная, и управляемая специализация.</span><span class="sxs-lookup"><span data-stu-id="74065-206">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="74065-207">В этом случае определяется существование управляемой примыкающей специализации, и компилятор создает соответствующую специализацию, если реализация не определена явным образом.</span><span class="sxs-lookup"><span data-stu-id="74065-207">In that case, the existence of the controlled adjoint specialization is inferred and an appropriate specialization is generated by the compiler if no implementation has been defined explicitly.</span></span> 

<span data-ttu-id="74065-208">Для операции, тело которой содержит вызовы других операций, не имеющих управляемой примыкающей версии, автоматическое создание примыкающей специализации после директивы `invert`, `distribute` или `auto` невозможно.</span><span class="sxs-lookup"><span data-stu-id="74065-208">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute` or `auto` directive is not possible.</span></span>


### <a name="examples"></a><span data-ttu-id="74065-209">Примеры</span><span class="sxs-lookup"><span data-stu-id="74065-209">Examples</span></span>

<span data-ttu-id="74065-210">Объявление операции может быть простым, как показано ниже, которое определяет операцию примитива Паули X:</span><span class="sxs-lookup"><span data-stu-id="74065-210">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (q : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```

<span data-ttu-id="74065-211">Ниже определяется операция телепортируйтесь.</span><span class="sxs-lookup"><span data-stu-id="74065-211">The following defines the teleport operation.</span></span>

```qsharp
// Entangle two qubits.
// Assumes that both qubits are in the |0> state.
operation EPR (q1 : Qubit, q2 : Qubit) : Unit 
is Adj + Ctl {
    H(q2);
    CNOT(q2, q1);
}

// Teleport the quantum state of the source to the target.
// Assumes that the target is in the |0> state.
operation Teleport (source : Qubit, target : Qubit) : Unit {

    // Get a temporary for the Bell pair
    using (ancilla = Qubit())
    {
        // Create a Bell pair between the temporary and the target
        EPR(target, ancilla);

        // Do the teleportation
        Adjoint EPR (ancilla, source);

        if (MResetZ(source) == One) {
            X(target);
        }
        if (MResetZ(ancilla) == One) {
            Z(target);
        }
    }
}
```

## <a name="function-declarations"></a><span data-ttu-id="74065-212">Объявления функций</span><span class="sxs-lookup"><span data-stu-id="74065-212">Function Declarations</span></span>

<span data-ttu-id="74065-213">Функции являются исключительно классическими подпрограммами в Q #.</span><span class="sxs-lookup"><span data-stu-id="74065-213">Functions are purely classical routines in Q#.</span></span>
<span data-ttu-id="74065-214">Каждый исходный файл Q # может определять любое количество функций.</span><span class="sxs-lookup"><span data-stu-id="74065-214">Each Q# source file may define any number of functions.</span></span>

<span data-ttu-id="74065-215">Объявление функции состоит из ключевого слова `function`, за которым следует символ, который является именем функции, кортежем типизированного идентификатора, аннотацией типа, описывающей тип возвращаемого значения функции, и блок операторов, описывающий реализацию функций.</span><span class="sxs-lookup"><span data-stu-id="74065-215">A function declaration consists of the keyword `function`, followed by the symbol that is the function’s name, a typed identifier tuple, a type annotation that describes the function's return type, and a statement block that describes the implementation of the function.</span></span>

<span data-ttu-id="74065-216">Блок инструкций, определяющий функцию, должен быть заключен в `{` и `}` как любой другой блок операторов.</span><span class="sxs-lookup"><span data-stu-id="74065-216">The statement block defining a function must be enclosed in `{` and `}` like any other statement block.</span></span>

<span data-ttu-id="74065-217">Имена функций должны быть уникальными в пределах пространства имен и не могут конфликтовать с именами операций и типов.</span><span class="sxs-lookup"><span data-stu-id="74065-217">Function names must be unique within a namespace and may not conflict with operation and type names.</span></span>
<span data-ttu-id="74065-218">Функции не могут выделить или получить Кубитс или вызвать операции.</span><span class="sxs-lookup"><span data-stu-id="74065-218">Functions may not allocate or borrow qubits, or call operations.</span></span> <span data-ttu-id="74065-219">Частичное применение операций или передача типизированных значений операции прекрасно подходит.</span><span class="sxs-lookup"><span data-stu-id="74065-219">Partial application of operations or passing around operation typed values is fine.</span></span>

<span data-ttu-id="74065-220">Например,</span><span class="sxs-lookup"><span data-stu-id="74065-220">For example,</span></span>

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```