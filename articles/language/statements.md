---
title: 'Q # операторы | Документация Майкрософт'
description: 'Инструкции Q #'
author: QuantumWriter
uid: microsoft.quantum.language.statements
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 5bcbee868c76aaf53d0b7969e6e634da62689aaa
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184871"
---
# <a name="statements-and-other-constructs"></a><span data-ttu-id="1ee2d-103">Операторы и другие конструкции</span><span class="sxs-lookup"><span data-stu-id="1ee2d-103">Statements and Other Constructs</span></span>

## <a name="comments"></a><span data-ttu-id="1ee2d-104">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ee2d-104">Comments</span></span>

<span data-ttu-id="1ee2d-105">Комментарии начинаются с двух косых черт, `//`и продолжаются до конца строки.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-105">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="1ee2d-106">Комментарий может находиться в любом месте исходного файла Q #.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-106">A comment may appear anywhere in a Q# source file.</span></span>

### <a name="documentation-comments"></a><span data-ttu-id="1ee2d-107">Комментарии к документации</span><span class="sxs-lookup"><span data-stu-id="1ee2d-107">Documentation Comments</span></span>

<span data-ttu-id="1ee2d-108">Комментарии, начинающиеся с трех косых черт, `///`, обрабатываются компилятором специально, когда они появляются непосредственно перед определением пространства имен, операции, специализации, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-108">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="1ee2d-109">В этом случае их содержимое берется в виде документации по определенному вызываемому или определяемому пользователем типу, как и для других языков .NET.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-109">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="1ee2d-110">В `///` комментариях текст, отображаемый в составе документации по API, форматируется как [Markdown](https://daringfireball.net/projects/markdown/syntax), а различные части документации указываются с помощью специально именованных заголовков.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-110">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="1ee2d-111">Как расширение Markdown, перекрестные ссылки на операции, функции и определяемые пользователем типы в Q # можно включать с помощью `@"<ref target>"`, где `<ref target>` заменяется полным именем объекта кода, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-111">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="1ee2d-112">Кроме того, обработчик документации может также поддерживать дополнительные расширения Markdown.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-112">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="1ee2d-113">Пример.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-113">For example:</span></span>

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit
{
    op(target);
    op(target);
}
```

<span data-ttu-id="1ee2d-114">Следующие имена распознаются как заголовки комментариев документации.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-114">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="1ee2d-115">**Сводка**: краткое описание поведения функции или операции или назначения типа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-115">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="1ee2d-116">Первый абзац сводки используется для сведений о наведении.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-116">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="1ee2d-117">Он должен быть обычным текстом.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-117">It should be plain text.</span></span>
- <span data-ttu-id="1ee2d-118">**Описание**: описание поведения функции или операции, либо назначение типа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-118">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="1ee2d-119">Сводные данные и описание объединяются, образуя созданный файл документации для функции, операции или типа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-119">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="1ee2d-120">Описание может содержать встроенные LaTeX символы и уравнения.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-120">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="1ee2d-121">**Входные данные**: описание входного кортежа для операции или функции.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-121">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="1ee2d-122">Может содержать дополнительные подразделы Markdown, указывающие каждый отдельный элемент входного кортежа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-122">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="1ee2d-123">**Output**: описание кортежа, возвращаемого операцией или функцией.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-123">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="1ee2d-124">**Параметры типа**: пустой раздел, содержащий один дополнительный подраздел для каждого параметра универсального типа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-124">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="1ee2d-125">**Пример**. короткий пример используемой операции, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-125">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="1ee2d-126">**Примечания**. различные prose, описывающие некоторые аспекты операции, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-126">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="1ee2d-127">**См. также**: список полных имен, указывающих связанные функции, операции или определяемые пользователем типы.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-127">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="1ee2d-128">**Ссылки**: список ссылок и ссылок для задокументированного элемента.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-128">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="namespaces"></a><span data-ttu-id="1ee2d-129">Пространства имен</span><span class="sxs-lookup"><span data-stu-id="1ee2d-129">Namespaces</span></span>

<span data-ttu-id="1ee2d-130">Каждая операция Q #, функция и определяемый пользователем тип определяется в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-130">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>
<span data-ttu-id="1ee2d-131">В параметре Q # применяются те же правила именования, что и для других языков .NET.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-131">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="1ee2d-132">Однако Q # не поддерживает относительные ссылки на пространства имен.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-132">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="1ee2d-133">То есть если было открыто `a.b` пространства имен, ссылка на имена операций `c.d` не будет разрешена в операцию с полным именем `a.b.c.d`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-133">That is, if the namespace `a.b` has been opened, a reference to an operation names `c.d` will not be resolved to an operation with full name `a.b.c.d`.</span></span>

<span data-ttu-id="1ee2d-134">В блоке пространства имен директива `open` может использоваться для импорта всех типов и вызываемых, объявленных в определенном пространстве имен, и ссылаться на них по их неполному имени.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-134">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span> <span data-ttu-id="1ee2d-135">Кроме того, можно определить короткое имя для открытого пространства имен таким, чтобы все элементы из этого пространства имен могли уточняться определенным коротким именем.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-135">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="1ee2d-136">Директива `open` применяется ко всему блоку пространства имен в файле.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-136">The `open` directive applies to the entire namespace block within a file.</span></span>

<span data-ttu-id="1ee2d-137">На тип или вызываемый объект, определенный в другом пространстве имен, который не открыт в текущем пространстве имен, должен ссылаться полное имя.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-137">A type or callable defined in another namespace that is not opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="1ee2d-138">Например, на операцию с именем `Op` в пространстве имен `X.Y` должно ссылаться полное имя `X.Y.Op`, если только пространство имен `X.Y` не было открыто ранее в текущем блоке.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-138">For example, an operation named `Op` in the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="1ee2d-139">Как упоминалось выше, даже при открытии пространства имен `X` нельзя ссылаться на операцию как на `Y.Op`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-139">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="1ee2d-140">Если в этом пространстве имен и файле определено короткое имя `Z` для `X.Y`, то `Op` необходимо называть `Z.Op`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-140">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

```qsharp
namespace NS {

    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace
}
```

<span data-ttu-id="1ee2d-141">Обычно лучше включать пространство имен с помощью директивы `open`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-141">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="1ee2d-142">Использование полного имени требуется, если два пространства имен определяют конструкции с одинаковым именем, а текущий источник использует конструкции из обоих.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-142">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

## <a name="formatting"></a><span data-ttu-id="1ee2d-143">Форматирование</span><span class="sxs-lookup"><span data-stu-id="1ee2d-143">Formatting</span></span>

<span data-ttu-id="1ee2d-144">Большинство инструкций и директив Q # заканчиваются завершающей точкой с запятой, `;`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-144">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="1ee2d-145">Инструкции и объявления, такие как `for` и `operation`, заканчивающиеся блоком операторов, не нуждаются в завершающей точке с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-145">Statements and declarations such as `for` and `operation` that end with a statement block do not require a terminating semicolon.</span></span>
<span data-ttu-id="1ee2d-146">Каждое описание инструкции отмечает, требуется ли завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-146">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="1ee2d-147">Инструкции, такие как выражения, объявления и директивы, могут быть разбиты на несколько строк.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-147">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="1ee2d-148">Следует избегать нескольких инструкций в одной строке.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-148">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="1ee2d-149">Блоки инструкций</span><span class="sxs-lookup"><span data-stu-id="1ee2d-149">Statement Blocks</span></span>

<span data-ttu-id="1ee2d-150">Инструкции Q # группируются в блоки инструкций.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-150">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="1ee2d-151">Блок операторов начинается с открывающего `{` и заканчивается закрывающим `}`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-151">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="1ee2d-152">Блок операторов, который лексической заключен в другой блок, считается вложенным блоком содержащего блока. содержащие и вложенные блоки также называются внешними и внутренними блоками.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-152">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="symbol-binding-and-assignment"></a><span data-ttu-id="1ee2d-153">Привязка и назначение символов</span><span class="sxs-lookup"><span data-stu-id="1ee2d-153">Symbol Binding and Assignment</span></span>

<span data-ttu-id="1ee2d-154">Q # различает изменяемые и неизменяемые символы.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-154">Q# distinguishes between mutable and immutable symbols.</span></span>
<span data-ttu-id="1ee2d-155">Как правило, использование неизменяемых символов рекомендуется, поскольку оно позволяет компилятору выполнять более оптимизацию.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-155">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="1ee2d-156">Левая часть привязки состоит из кортежа символов, а также с правой стороны выражения.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-156">The left-hand-side of the binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

<span data-ttu-id="1ee2d-157">Так как все типы Q # являются типами значений — с Кубитс, принимающей более специальную роль, формально создается «Copy», когда значение привязывается к символу, или при повторной привязке символа.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-157">Since all Q# types are value types - with the qubits taking a somewhat special role - formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="1ee2d-158">То есть, поведение Q # аналогично тому, как если бы копия была создана при назначении.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-158">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span> <span data-ttu-id="1ee2d-159">В частности, это также касается массивов.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-159">This in particular also includes arrays.</span></span> <span data-ttu-id="1ee2d-160">Разумеется, на практике при необходимости воссоздаются только соответствующие части.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-160">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

### <a name="tuple-deconstruction"></a><span data-ttu-id="1ee2d-161">Деконструкция кортежа</span><span class="sxs-lookup"><span data-stu-id="1ee2d-161">Tuple Deconstruction</span></span>

<span data-ttu-id="1ee2d-162">Если правая часть привязки является кортежем, то этот кортеж можно деконструировать после назначения.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-162">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="1ee2d-163">Такие деконструкции могут содержать вложенные кортежи, а любая полная или частичная деконструкция является допустимой, если форма кортежа в правой части совместима с формой кортежа символов.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-163">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>
<span data-ttu-id="1ee2d-164">Деконструкцию кортежей можно также использовать, если правая часть `=` является кортежным выражением.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-164">Tuple deconstruction can in particular also be used when the right-hand side of the `=` is a tuple-valued expression.</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

### <a name="immutable-symbols"></a><span data-ttu-id="1ee2d-165">Неизменяемые символы</span><span class="sxs-lookup"><span data-stu-id="1ee2d-165">Immutable Symbols</span></span>

<span data-ttu-id="1ee2d-166">Неизменяемые символы привязываются с помощью оператора `let`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-166">Immutable symbols are bound using the `let` statement.</span></span>
<span data-ttu-id="1ee2d-167">Это примерно эквивалентно объявлению и инициализации переменных на таких языках, C#как, за исключением того, что символ Q # после привязки не может быть изменен. привязки `let` являются неизменяемыми.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-167">This is roughly equivalent to variable declaration and initialization in languages such as C#, except that Q# symbols, once bound, may not be changed; `let` bindings are immutable.</span></span>

<span data-ttu-id="1ee2d-168">Неизменяемая Привязка состоит из ключевого слова `let`, за которым следует символ или кортеж символов, знак равенства `=`, выражение для привязки символов к и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-168">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="1ee2d-169">Тип привязанных символов определяется на основе выражения с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-169">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span>

### <a name="mutable-symbols"></a><span data-ttu-id="1ee2d-170">Изменяемые символы</span><span class="sxs-lookup"><span data-stu-id="1ee2d-170">Mutable Symbols</span></span>

<span data-ttu-id="1ee2d-171">Изменяемые символы определяются и инициализируются с помощью инструкции `mutable`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-171">Mutable symbols are defined and initialized using the `mutable` statement.</span></span>
<span data-ttu-id="1ee2d-172">Символы, объявленные и привязанные как часть оператора `mutable`, можно повторно привязать к другому значению позже в коде.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-172">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> 

<span data-ttu-id="1ee2d-173">Изменяемый оператор привязки состоит из ключевого слова `mutable`, за которым следует символ или кортеж символов, знак равенства `=`, выражение для привязки символов к и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-173">A mutable binding statement consists of the keyword `mutable`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="1ee2d-174">Тип привязанных символов определяется на основе выражения с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-174">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span> <span data-ttu-id="1ee2d-175">Если символ повторно привязан позже в коде, его тип не изменится, а связанное значение должно быть совместимо с этим типом.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-175">If a symbol is rebound later in the code, its type does not change, and the bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="1ee2d-176">Повторная привязка изменяемых символов</span><span class="sxs-lookup"><span data-stu-id="1ee2d-176">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="1ee2d-177">Изменяемую переменную можно повторно привязать с помощью инструкции `set`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-177">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="1ee2d-178">Такая повторная привязка состоит из ключевого слова `set`, за которым следует символ или кортеж символов, знак равенства `=`, выражение для повторной привязки символов к и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-178">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="1ee2d-179">Значение должно быть совместимо с типами символов, к которым он привязан.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-179">The value must be compatible with the type(s) of the symbol(s) it is bound to.</span></span>

#### <a name="apply-and-reassign-statement"></a><span data-ttu-id="1ee2d-180">Инструкция Apply и REASSIGN</span><span class="sxs-lookup"><span data-stu-id="1ee2d-180">Apply-and-Reassign Statement</span></span>

<span data-ttu-id="1ee2d-181">Определенный тип оператора Set, который называется оператором применения и повторного присваивания, предоставляет удобный способ объединения, если правая часть состоит из приложения бинарного оператора, а результат повторно привязан к оператору слева.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-181">A particular kind of set-statement we refer to as an apply-and-reassign statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="1ee2d-182">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-182">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="1ee2d-183">увеличивает значение счетчика `counter` в каждой итерации цикла `for`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-183">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="1ee2d-184">Приведенный выше код эквивалентен</span><span class="sxs-lookup"><span data-stu-id="1ee2d-184">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```
<span data-ttu-id="1ee2d-185">Аналогичные операторы доступны для всех бинарных операторов, в которых тип левой стороны соответствует типу выражения.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-185">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="1ee2d-186">Это предоставляет пример удобного способа накопления значений:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-186">This provides for example a convenient way to accumulate values:</span></span>
```qsharp
mutable results = new Result[0];
for (q in qubits) {
    set results += [M(q)];
    // ...
}
```
#### <a name="update-and-reassign-statement"></a><span data-ttu-id="1ee2d-187">Инструкция UPDATE и REASSIGN</span><span class="sxs-lookup"><span data-stu-id="1ee2d-187">Update-and-Reassign Statement</span></span>

<span data-ttu-id="1ee2d-188">Аналогичное объединение существует для выражений копирования и обновления с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-188">A similar concatenation exists for copy-and-update expressions on the right hand side.</span></span> <span data-ttu-id="1ee2d-189">Соответственно, операторы Update и reassignя существуют для именованных элементов в определяемых пользователем типах, а также для элементов массива.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-189">Correspondingly, update-and-reassign statements exist for named items in user-defined types as well as for array items.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function AddAll (reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="1ee2d-190">В случае массивов наши стандартные библиотеки содержат необходимые средства для многих общих задач инициализации и манипуляции массивов, что позволяет избежать необходимости обновлять элементы массива в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-190">In the case of arrays, our standard libraries contain the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> <span data-ttu-id="1ee2d-191">Инструкции обновления и повторного назначения предоставляют альтернативный вариант при необходимости:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-191">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {

    mutable samples = new Double[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}

operation SampleUniformDistr(nrSamples : Int, prec : Int) : Double[] {

    let normalization = 1. / IntAsDouble(prec);
    mutable samples = RandomInts(prec, nrSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

> [!TIP]   
> <span data-ttu-id="1ee2d-192">Избегайте ненужного использования инструкций обновления и повторного назначения, используя средства, предоставляемые в <xref:microsoft.quantum.arrays>.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-192">Avoid unnecessary use of update-and-reassign statements by leveraging the tools provided in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="1ee2d-193">Функция</span><span class="sxs-lookup"><span data-stu-id="1ee2d-193">The function</span></span>
```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
{
    mutable pauliArray = new Pauli[n];
    for (index in 0 .. n - 1) {
        set pauliArray w/= index <- 
            index == location ? pauli | PauliI;
    }    
    return pauliArray;
}
```
<span data-ttu-id="1ee2d-194">Например, можно просто упростить использование функции `ConstantArray` в `Microsoft.Quantum.Arrays`и возвратить выражение копирования и обновления:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-194">for example can simply be simplified using the function `ConstantArray` in `Microsoft.Quantum.Arrays`, and returning a copy-and-update expression:</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    return ConstantArray(n, PauliI) w/ i <- pauli;
}
```

### <a name="binding-scopes"></a><span data-ttu-id="1ee2d-195">Области привязки</span><span class="sxs-lookup"><span data-stu-id="1ee2d-195">Binding Scopes</span></span>

<span data-ttu-id="1ee2d-196">Как правило, привязки к символам выходят за пределы области действия и становятся неработоспособными в конце блока операторов, в котором они встречаются.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-196">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="1ee2d-197">Существует два исключения из этого правила:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-197">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="1ee2d-198">Привязка переменной цикла `for` цикла находится в области видимости тела цикла for, но не после конца цикла.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-198">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="1ee2d-199">Все три части `repeat`/цикл `until` (текст, тест и адресная привязка) обрабатываются как одна область, поэтому символы, привязанные к тексту, доступны в тесте и в адресной привязке.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-199">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="1ee2d-200">Для обоих типов циклов каждый проход по циклу выполняется в своей собственной области, поэтому привязки из предыдущего прохода не будут доступны на более позднем этапе.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-200">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>

<span data-ttu-id="1ee2d-201">Привязки символов из внешних блоков наследуются внутренними блоками.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-201">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="1ee2d-202">Символ может быть привязан только один раз для каждого блока; нельзя определить символ с тем же именем, что и у другого символа, находящихся в пределах области (без "тени").</span><span class="sxs-lookup"><span data-stu-id="1ee2d-202">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="1ee2d-203">Следующие последовательности будут допустимыми:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-203">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="1ee2d-204">Azure и</span><span class="sxs-lookup"><span data-stu-id="1ee2d-204">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
```

<span data-ttu-id="1ee2d-205">Но это недопустимо:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-205">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="1ee2d-206">как:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-206">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="control-flow"></a><span data-ttu-id="1ee2d-207">Поток управления</span><span class="sxs-lookup"><span data-stu-id="1ee2d-207">Control Flow</span></span>

### <a name="for-loop"></a><span data-ttu-id="1ee2d-208">Цикл for</span><span class="sxs-lookup"><span data-stu-id="1ee2d-208">For Loop</span></span>

<span data-ttu-id="1ee2d-209">Оператор `for` поддерживает итерацию по диапазону целых чисел или к массиву.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-209">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="1ee2d-210">Оператор состоит из ключевого слова `for`, открывающей скобки `(`, за которой следует символ или кортеж символов, ключевое слово `in`, выражение типа `Range` или Array, закрывающая круглая скобка `)`и блок операторов.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-210">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="1ee2d-211">Блок операторов (тело цикла) выполняется повторно с определенными символами (переменными цикла), привязанными к каждому значению в диапазоне или массиве.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-211">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="1ee2d-212">Обратите внимание, что если выражение диапазона принимает пустой диапазон или массив, тело не будет выполняться вообще.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-212">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="1ee2d-213">Выражение полностью вычисляется перед входом в цикл и не будет изменяться во время выполнения цикла.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-213">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="1ee2d-214">Привязка объявленных символов является неизменяемой и соответствует тем же правилам, что и другие привязки переменных.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-214">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> <span data-ttu-id="1ee2d-215">В частности, можно уничтожения, например, элементы массива для итерации по массиву после присваивания переменным цикла.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-215">In particular, it is possible to destruct e.g. array items for an iteration over an array upon assignment to the loop variable(s).</span></span>

<span data-ttu-id="1ee2d-216">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-216">For example,</span></span>

```qsharp
// ...
for (qb in qubits) { // qubits contains a Qubit[]
    H(qb);
}

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {
    set results w/= index <- (index, M(qubits[index]));
}

mutable accumulated = 0;
for ((index, measured) in results) {
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

<span data-ttu-id="1ee2d-217">Переменная цикла привязывается к каждому входу в тело цикла и не привязана к концу тела.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-217">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="1ee2d-218">В частности, переменная цикла не привязана после завершения цикла for.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-218">In particular, the loop variable is not bound after the for loop is completed.</span></span>

### <a name="repeat-until-success-loop"></a><span data-ttu-id="1ee2d-219">Цикл "повторить" до "успешно"</span><span class="sxs-lookup"><span data-stu-id="1ee2d-219">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="1ee2d-220">Инструкция `repeat` поддерживает шаблон такта "повторять до успешного завершения".</span><span class="sxs-lookup"><span data-stu-id="1ee2d-220">The `repeat` statement supports the quantum “repeat until success” pattern.</span></span>
<span data-ttu-id="1ee2d-221">Он состоит из ключевого слова `repeat`, за которым следует блок операторов (тело _цикла_ ), ключевое слово `until`, логическое выражение и либо завершающая точка с запятой, либо ключевое слово `fixup`, за которым следует другой блок операторов ( _адресная привязка_).</span><span class="sxs-lookup"><span data-stu-id="1ee2d-221">It consists of the keyword `repeat`, followed by a statement block (the _loop_ body), the keyword `until`, a Boolean expression, and either a terminating semicolon or the keyword `fixup` followed by another statement block (the _fixup_).</span></span>
<span data-ttu-id="1ee2d-222">Тело цикла, условие и исправление считаются одной областью, поэтому символы, привязанные к тексту, доступны в условии и адресной привязке.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-222">The loop body, condition, and fixup are all considered to be a single scope, so symbols bound in the body are available in the condition and fixup.</span></span>

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qs);
    let success = ComputeSuccessIndicator(qs);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qs);
}
```

<span data-ttu-id="1ee2d-223">Выполняется тело цикла, а затем вычисляется условие.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-223">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="1ee2d-224">Если условие истинно, инструкция завершается; в противном случае выполняется адресная привязка и выполняется повторная инструкция, начиная с тела цикла.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-224">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>
<span data-ttu-id="1ee2d-225">Обратите внимание, что завершение выполнения адресной привязки завершает область действия инструкции, чтобы привязки символов, сделанные во время тела или исправления, были недоступны при последующих повторах.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-225">Note that completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="1ee2d-226">Например, следующий код представляет собой цепь вероятностная, которая реализует важный шлюз ротации $V _3 = (\болдоне + 2 i Z)/\скрт{5}$ с использованием Хадамард и T Gates.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-226">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the Hadamard and T gates.</span></span>
<span data-ttu-id="1ee2d-227">Цикл завершается через 8/5 повторений в среднем.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-227">The loop terminates in 8/5 repetitions on average.</span></span>
<span data-ttu-id="1ee2d-228">Дополнительные сведения см. в разделе [*Повтор-Until-Success: недетерминированная декомпозиция одного кубит унитариес*](https://arxiv.org/abs/1311.1074) (Паетзникк и своре, 2014).</span><span class="sxs-lookup"><span data-stu-id="1ee2d-228">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for details.</span></span>

```qsharp
using (anc = Qubit()) {
    repeat {
        H(anc);
        T(anc);
        CNOT(target,anc);
        H(anc);
        Adjoint T(anc);
        H(anc);
        T(anc);
        H(anc);
        CNOT(target,anc);
        T(anc);
        Z(target);
        H(anc);
        let result = M(anc);
    } until (result == Zero);
}
```

> [!TIP]   
> <span data-ttu-id="1ee2d-229">Избегайте использования циклов повторения до успешного выполнения в функциях.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-229">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="1ee2d-230">Соответствующие функциональные возможности обеспечиваются циклами while в функциях.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-230">The corresponding functionality is provided by while loops in functions.</span></span> 

### <a name="while-loop"></a><span data-ttu-id="1ee2d-231">Цикл while</span><span class="sxs-lookup"><span data-stu-id="1ee2d-231">While Loop</span></span>

<span data-ttu-id="1ee2d-232">Шаблоны Repeat-Until-Success имеют очень много времени.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-232">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="1ee2d-233">Они широко используются в определенных классах тактовых алгоритмов, поэтому выделенная конструкция языка в Q #.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-233">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="1ee2d-234">Однако циклы, которые нарушаются в зависимости от условия и длина выполнения которого во время компиляции неизвестны, должны обрабатываться с определенной осторожностью в среде выполнения такта.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-234">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="1ee2d-235">Их использование в функциях с другой стороны не является проблемой, поскольку в них содержится только код, который будет выполняться на обычном (не такте) оборудовании.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-235">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="1ee2d-236">Таким образом, Q # поддерживает использование циклов while только внутри функций.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-236">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="1ee2d-237">Оператор `while` состоит из ключевого слова `while`, открывающей скобки `(`, условия (т. е. логического выражения), закрывающей скобки `)`и блока операторов.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-237">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="1ee2d-238">Блок операторов (тело цикла) выполняется при условии, что условие принимает значение `true`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-238">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

### <a name="conditional-statement"></a><span data-ttu-id="1ee2d-239">Условный оператор</span><span class="sxs-lookup"><span data-stu-id="1ee2d-239">Conditional Statement</span></span>

<span data-ttu-id="1ee2d-240">Оператор `if` поддерживает условное выполнение.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-240">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="1ee2d-241">Он состоит из ключевого слова `if`, открывающей скобки `(`, логического выражения, закрывающей скобки `)`и блока операторов (блок _then_ ).</span><span class="sxs-lookup"><span data-stu-id="1ee2d-241">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="1ee2d-242">За этим может следовать любое число предложений else-if, каждое из которых состоит из ключевого слова `elif`, открывающей скобки `(`, логического выражения, закрывающей скобки `)`и блока операторов ( _Else-If_ ).</span><span class="sxs-lookup"><span data-stu-id="1ee2d-242">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="1ee2d-243">Наконец, оператор может при необходимости завершиться предложением else, которое состоит из ключевого слова `else` за которым следует другой блок операторов (блок _else_ ).</span><span class="sxs-lookup"><span data-stu-id="1ee2d-243">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>
<span data-ttu-id="1ee2d-244">Условие вычисляется, и, если оно равно true, выполняется блок then.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-244">The condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="1ee2d-245">Если условие имеет значение false, то проверяется первое условие else-if; Если значение равно true, выполняется блок Else-If.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-245">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="1ee2d-246">В противном случае проверяется второй блок-If, а затем третий и т. д., пока не будет обнаружено предложение с истинным условием или отсутствуют другие предложения Else-If.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-246">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="1ee2d-247">Если исходное условие If и все предложения Else-If имеют значение false, то блок Else выполняется, если он был предоставлен.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-247">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="1ee2d-248">Обратите внимание, что любой блок выполняется в своей собственной области.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-248">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="1ee2d-249">Привязки, сделанные внутри блока then, else-if или else, не видны после окончания оператора if.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-249">Bindings made inside of a then, else-if, or else block are not visible after the end of the if statement.</span></span>

<span data-ttu-id="1ee2d-250">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-250">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
} 
```

<span data-ttu-id="1ee2d-251">или</span><span class="sxs-lookup"><span data-stu-id="1ee2d-251">or</span></span>

```qsharp
if (i == 1) {
    X(target);
} elif (i == 2) {
    Y(target);
} else {
    Z(target);
}
```

### <a name="return"></a><span data-ttu-id="1ee2d-252">Return</span><span class="sxs-lookup"><span data-stu-id="1ee2d-252">Return</span></span>

<span data-ttu-id="1ee2d-253">Оператор Return завершает выполнение операции или функции и возвращает значение вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-253">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="1ee2d-254">Он состоит из ключевого слова `return`, за которым следует выражение соответствующего типа и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-254">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="1ee2d-255">Вызываемый метод, возвращающий пустой кортеж, `()`, не требует оператора return.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-255">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="1ee2d-256">Если требуется выполнить раннее завершение работы, в этом случае может использоваться `return ()`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-256">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="1ee2d-257">Для вызова, возвращающего любой другой тип, требуется завершающий оператор return.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-257">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="1ee2d-258">В операции отсутствует максимальное число инструкций Return.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-258">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="1ee2d-259">Компилятор может выдать предупреждение, если операторы следуют за оператором Return в блоке.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-259">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="1ee2d-260">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-260">For example,</span></span>

```qsharp
return 1;
```

<span data-ttu-id="1ee2d-261">или</span><span class="sxs-lookup"><span data-stu-id="1ee2d-261">or</span></span>

```qsharp
return ();
```

<span data-ttu-id="1ee2d-262">или</span><span class="sxs-lookup"><span data-stu-id="1ee2d-262">or</span></span>

```qsharp
return (results, qubits);
```

### <a name="fail"></a><span data-ttu-id="1ee2d-263">Fail;</span><span class="sxs-lookup"><span data-stu-id="1ee2d-263">Fail</span></span>

<span data-ttu-id="1ee2d-264">Инструкция Fail завершает выполнение операции и возвращает вызывающему объекту значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-264">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="1ee2d-265">Он состоит из ключевого слова `fail`, за которым следует строка и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-265">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="1ee2d-266">Строка возвращается в классический драйвер в качестве сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-266">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="1ee2d-267">Количество инструкций Fail в операции не ограничено.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-267">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="1ee2d-268">Компилятор может выдать предупреждение, если операторы следуют за оператором Fail в блоке.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-268">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="1ee2d-269">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-269">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```

<span data-ttu-id="1ee2d-270">или</span><span class="sxs-lookup"><span data-stu-id="1ee2d-270">or</span></span>

```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="qubit-management"></a><span data-ttu-id="1ee2d-271">Управление кубит</span><span class="sxs-lookup"><span data-stu-id="1ee2d-271">Qubit Management</span></span>

<span data-ttu-id="1ee2d-272">Обратите внимание, что ни одна из этих инструкций не разрешена в теле функции.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-272">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="1ee2d-273">Они действительны только в пределах операций.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-273">They are only valid within operations.</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="1ee2d-274">Очистить Кубитс</span><span class="sxs-lookup"><span data-stu-id="1ee2d-274">Clean Qubits</span></span>

<span data-ttu-id="1ee2d-275">Оператор `using` используется для получения новых Кубитс для использования во время блока инструкций.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-275">The `using` statement is used to acquire new qubits for use during a statement block.</span></span>
<span data-ttu-id="1ee2d-276">Кубитс гарантированно инициализируются в вычислительное состояние `Zero`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-276">The qubits are guaranteed to be initialized to the computational `Zero` state.</span></span>
<span data-ttu-id="1ee2d-277">Кубитс должен находиться в состоянии вычислительного `Zero` в конце блока инструкции; для этого рекомендуется применять симуляторы.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-277">The qubits should be in the computational `Zero` state at the end of the statement block; simulators are encouraged to enforce this.</span></span>

<span data-ttu-id="1ee2d-278">Оператор состоит из ключевого слова `using`, за которым следует открывающая круглая скобка `(`, привязка, закрывающая круглая скобка `)`и блок операторов, в рамках которого будет доступна Кубитс.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-278">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="1ee2d-279">Привязка соответствует тому же шаблону, что и `let`ные операторы: один символ или кортеж символов, за которым следует знак равенства `=`и одно значение или соответствующий кортеж инициализаторов.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-279">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of initializers.</span></span>
<span data-ttu-id="1ee2d-280">Инициализаторы доступны для одного кубит, обозначенного как `Qubit()`, или массива Кубитс, обозначенного `Qubit[`, `Int`ным выражением и `]`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-280">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, indicated by `Qubit[`, an `Int` expression, and `]`.</span></span>

<span data-ttu-id="1ee2d-281">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-281">For example,</span></span>

```qsharp
using (q = Qubit()) {
    // ...
}
using ((ancilla, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

### <a name="dirty-qubits"></a><span data-ttu-id="1ee2d-282">Грязный Кубитс</span><span class="sxs-lookup"><span data-stu-id="1ee2d-282">Dirty Qubits</span></span>

<span data-ttu-id="1ee2d-283">Оператор `borrowing` используется для получения Кубитс для временного использования.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-283">The `borrowing` statement is used to obtain qubits for temporary use.</span></span> <span data-ttu-id="1ee2d-284">Оператор состоит из ключевого слова `borrowing`, за которым следует открывающая круглая скобка `(`, привязка, закрывающая круглая скобка `)`и блок операторов, в рамках которого будет доступна Кубитс.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-284">The statement consists of the keyword `borrowing`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="1ee2d-285">Привязка соответствует тому же шаблону и правилам, что и в операторе `using`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-285">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>

<span data-ttu-id="1ee2d-286">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-286">For example,</span></span>

```qsharp
borrowing (q = Qubit()) {
    // ...
}
borrowing ((ancilla, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

<span data-ttu-id="1ee2d-287">Заимствованные Кубитс находятся в неизвестном состоянии и выходят за пределы области действия в конце блока инструкций.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-287">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="1ee2d-288">Он фиксируется, чтобы покинуть Кубитс в том состоянии, в котором они находились в момент заимствования, т. е. состояние в начале и в конце блока инструкции должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-288">The borrower commits to leaving the qubits in the same state they were in when they were borrowed, i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="1ee2d-289">Это состояние в частности не всегда является классическим состоянием, поэтому в большинстве случаев области действия не должны содержать измерений.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-289">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="1ee2d-290">Такие Кубитс часто называются «грязными анЦиллаами».</span><span class="sxs-lookup"><span data-stu-id="1ee2d-290">Such qubits are often known as “dirty ancilla”.</span></span>
<span data-ttu-id="1ee2d-291">Пример использования "грязных" 2N см. в разделе [*факторинг с использованием функции "Тоффоли" + 2 Кубитс с модульным умножением на*](https://arxiv.org/abs/1611.07995) единицу (Ханер, Роеттелер и своре 2017).</span><span class="sxs-lookup"><span data-stu-id="1ee2d-291">See [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an example of dirty ancilla use.</span></span>

<span data-ttu-id="1ee2d-292">При заимствовании Кубитс система сначала пытается заполнить запрос от Кубитс, который используется, но к нему не обращаются в теле инструкции `borrowing`.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-292">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="1ee2d-293">Если такой Кубитс не хватает, он выделит новый Кубитс для выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-293">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>

## <a name="conjugations"></a><span data-ttu-id="1ee2d-294">Лиц</span><span class="sxs-lookup"><span data-stu-id="1ee2d-294">Conjugations</span></span>

<span data-ttu-id="1ee2d-295">В отличие от классических битов освобождение памяти такта немного сложнее, так как в результате нежелательного сброса Кубитс может иметь нежелательные последствия для оставшихся вычислений, если Кубитс все еще запутанными.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-295">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="1ee2d-296">Это можно избежать, правильно выполнив вычисления перед освобождением памяти.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-296">This can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="1ee2d-297">Общий шаблон в тактовых вычислениях, следовательно, является следующим:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-297">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="1ee2d-298">: New: начиная с нашего выпуска 0,9 мы поддерживаем инструкцию конжугатион, которая реализует преобразование выше.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-298">:new: Starting with our 0.9 release, we support a conjugation statement that implements the transformation above.</span></span> <span data-ttu-id="1ee2d-299">С помощью этой инструкции операция `ApplyWith` может быть реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1ee2d-299">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="1ee2d-300">Очевидно, что такой оператор конжугатион гораздо полезнее, если внешнее и внутреннее преобразование недоступно в качестве операций, но вместо этого более удобно описывать блоком, состоящим из нескольких инструкций.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-300">Such a conjugation statement obviously becomes far more useful if the outer and inner transformation are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="1ee2d-301">Обратное преобразование для инструкций, определенных в блоке внутри блока, автоматически создается компилятором и выполняется после завершения блока Apply.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-301">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and executed after the apply-block completes.</span></span> <span data-ttu-id="1ee2d-302">Поскольку любые изменяемые переменные, используемые в качестве части блока in, не могут быть повторно привязаны в блоке применения, созданное преобразование гарантируется как прилегающие вычисления в блоке внутри блока.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-302">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 

## <a name="expression-evaluation-statements"></a><span data-ttu-id="1ee2d-303">Операторы вычисления выражений</span><span class="sxs-lookup"><span data-stu-id="1ee2d-303">Expression Evaluation Statements</span></span>

<span data-ttu-id="1ee2d-304">Любое выражение вызова типа `Unit` может использоваться в качестве инструкции.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-304">Any call expression of type `Unit` may be used as a statement.</span></span>
<span data-ttu-id="1ee2d-305">Это в первую очередь используется при вызове операций с Кубитс, возвращающих `Unit`, так как целью инструкции является изменение неявного состояния такта.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-305">This is primarily of use when calling operations on qubits that return `Unit` because the purpose of the statement is to modify the implicit quantum state.</span></span>
<span data-ttu-id="1ee2d-306">Для операторов вычисления выражения требуется завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="1ee2d-306">Expression evaluation statements require a terminating semicolon.</span></span>

<span data-ttu-id="1ee2d-307">Например,</span><span class="sxs-lookup"><span data-stu-id="1ee2d-307">For example,</span></span>

```qsharp
X(q);
CNOT(control, target);
Adjoint T(q);
```
