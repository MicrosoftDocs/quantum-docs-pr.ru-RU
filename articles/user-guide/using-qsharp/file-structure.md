---
title: 'Q # файл структура'
description: 'Описывает структуру и синтаксис файла Q #.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: cbee92c6d7e765237a7a42532dd7012b51421708
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430974"
---
# <a name="q-file-structure"></a><span data-ttu-id="8f77a-103">Q # файл структура</span><span class="sxs-lookup"><span data-stu-id="8f77a-103">Q# File Structure</span></span>

<span data-ttu-id="8f77a-104">Каждая операция Q #, функция и определяемый пользователем тип определяется в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8f77a-104">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>

<span data-ttu-id="8f77a-105">Файл Q # состоит из последовательности *объявлений пространств имен*.</span><span class="sxs-lookup"><span data-stu-id="8f77a-105">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="8f77a-106">Каждое объявление пространства имен содержит объявления для определяемых пользователем типов, операций и функций.</span><span class="sxs-lookup"><span data-stu-id="8f77a-106">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="8f77a-107">Объявление пространства имен может содержать любое количество объявлений каждого типа и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="8f77a-107">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="8f77a-108">Используйте эти ссылки для получения дополнительных сведений об объявлении [определяемых пользователем типов](xref:microsoft.quantum.guide.types#user-defined-types), [операций](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)и [функций](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8f77a-108">Follow these links for more details on declaring [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) within a namespace.</span></span>

<span data-ttu-id="8f77a-109">Единственный текст, который может находиться за пределами объявления пространства имен, — это комментарии.</span><span class="sxs-lookup"><span data-stu-id="8f77a-109">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="8f77a-110">В частности, комментарии к документации (Дополнительные сведения см. ниже) для пространства имен перед объявлением.</span><span class="sxs-lookup"><span data-stu-id="8f77a-110">In particular, documentation comments (more details below) for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="8f77a-111">Объявление пространств имен</span><span class="sxs-lookup"><span data-stu-id="8f77a-111">Namespace Declarations</span></span>

<span data-ttu-id="8f77a-112">Как правило, файл Q # содержит только одно объявление пространства имен, но может содержать пустое значение (и быть пустым или содержать только комментарии) или может включать несколько пространств имен.</span><span class="sxs-lookup"><span data-stu-id="8f77a-112">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="8f77a-113">Объявления пространств имен не могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="8f77a-113">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="8f77a-114">Одно и то же пространство имен может быть объявлено в нескольких файлах Q #, компилируемых вместе, при условии, что отсутствуют объявления типов, операций или функций с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="8f77a-114">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="8f77a-115">В частности, нельзя определить один и тот же тип в одном пространстве имен в нескольких файлах, даже если объявления идентичны.</span><span class="sxs-lookup"><span data-stu-id="8f77a-115">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="8f77a-116">Объявление пространства имен состоит из ключевого слова `namespace` , за которым следует имя пространства имен, открывающую фигурную скобку `{` , объявления, содержащиеся в пространстве имен, и закрывающую фигурную скобку `}` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-116">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="8f77a-117">Имена пространств имен соответствуют шаблону .NET последовательности из одного или нескольких юридических символов, разделенных точками `.` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-117">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="8f77a-118">Например, `MyQuantumStuff` и `Microsoft.Quantum.Intrinsic` являются допустимыми именами пространств имен.</span><span class="sxs-lookup"><span data-stu-id="8f77a-118">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="8f77a-119">По соглашению символы в имени пространства имен записываются прописными буквами, но это не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8f77a-119">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="8f77a-120">Ссылки на типы или вызываемые объекты, объявленные ниже в файле, разрешаются правильно. нет необходимости в объявлении типа, операции или функции перед ссылкой на нее.</span><span class="sxs-lookup"><span data-stu-id="8f77a-120">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="8f77a-121">Открытые директивы</span><span class="sxs-lookup"><span data-stu-id="8f77a-121">Open Directives</span></span>

<span data-ttu-id="8f77a-122">В блоке пространства имен `open` директива может использоваться для импорта всех типов и вызовов, объявленных в определенном пространстве имен, и ссылаться на них по их неполному имени.</span><span class="sxs-lookup"><span data-stu-id="8f77a-122">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="8f77a-123">Такая `open` директива состоит из `open` ключевого слова, за которым следует открытое пространство имен и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="8f77a-123">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="8f77a-124">Все `open` директивы должны находиться перед `function` `operation` объявлениями, или `newtype` в блоке пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8f77a-124">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="8f77a-125">Кроме того, можно определить короткое имя для открытого пространства имен таким, чтобы все элементы из этого пространства имен могли уточняться определенным коротким именем.</span><span class="sxs-lookup"><span data-stu-id="8f77a-125">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="8f77a-126">Например, учитывая следующее объявление пространства имен и открытые директивы,</span><span class="sxs-lookup"><span data-stu-id="8f77a-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="8f77a-127">Если операция, которую мы объявляем, использует операцию `Op` из `Microsoft.Quantum.Intrinsic` , мы вызываем ее, просто используя `Op` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-127">if an operation we declare uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, we would call it by simply using `Op`.</span></span>
<span data-ttu-id="8f77a-128">Однако если бы нам требовалось вызвать определенную функцию `Fn` из `Microsoft.Quantum.Math` , необходимо вызвать ее с помощью `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-128">However, if we wanted a call a certain function `Fn` from `Microsoft.Quantum.Math`, we would need to call it using `Math.Fn`.</span></span>

<span data-ttu-id="8f77a-129">`open`Директива применяется ко всему блоку пространства имен в файле.</span><span class="sxs-lookup"><span data-stu-id="8f77a-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="8f77a-130">Таким образом, если бы было определено дополнительное пространство имен в том же файле Q # `NS` , что и ранее, то любые операции, функции и типы, определенные во втором пространстве имен, не будут иметь доступа ни к чему, ни к `Microsoft.Quantum.Intrinsic` тому или только мы не повторяли `Microsoft.Quantum.Math` директивы Open.</span><span class="sxs-lookup"><span data-stu-id="8f77a-130">Hence, if we were to define an additional namespace in the same Q# file as `NS` above, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless we repeated the open directives therein.</span></span> 

<span data-ttu-id="8f77a-131">На тип или вызываемый объект, определенный в другом пространстве имен, который *не* открыт в текущем пространстве имен, должен ссылаться полное имя.</span><span class="sxs-lookup"><span data-stu-id="8f77a-131">A type or callable defined in another namespace that is *not* opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="8f77a-132">Например, на операцию с именем `Op` из `X.Y` пространства имен должно ссылаться полное имя `X.Y.Op` , если только `X.Y` пространство имен не было открыто ранее в текущем блоке.</span><span class="sxs-lookup"><span data-stu-id="8f77a-132">For example, an operation named `Op` from the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="8f77a-133">Как упоминалось выше, даже если `X` пространство имен было открыто, ссылаться на эту операцию как невозможно `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-133">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="8f77a-134">Если `Z` `X.Y` в этом пространстве имен и файле было определено короткое имя, необходимо `Op` называть его `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-134">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

<span data-ttu-id="8f77a-135">Обычно лучше включать пространство имен с помощью `open` директивы.</span><span class="sxs-lookup"><span data-stu-id="8f77a-135">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="8f77a-136">Использование полного имени требуется, если два пространства имен определяют конструкции с одинаковым именем, а текущий источник использует конструкции из обоих.</span><span class="sxs-lookup"><span data-stu-id="8f77a-136">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="8f77a-137">В параметре Q # применяются те же правила именования, что и для других языков .NET.</span><span class="sxs-lookup"><span data-stu-id="8f77a-137">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="8f77a-138">Однако Q # не поддерживает относительные ссылки на пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8f77a-138">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="8f77a-139">То есть, если пространство имен `a.b` было открыто, ссылка на операцию с именем `c.d` *не* будет разрешаться в операцию с полным именем `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-139">That is, if the namespace `a.b` has been opened, a reference to an operation named `c.d` will *not* be resolved to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="8f77a-140">Форматирование</span><span class="sxs-lookup"><span data-stu-id="8f77a-140">Formatting</span></span>

<span data-ttu-id="8f77a-141">Большинство инструкций и директив Q # заканчиваются завершающей точкой с запятой, `;` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-141">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="8f77a-142">Инструкции и объявления, такие как `for` и `operation` , заканчивающиеся блоком операторов (см. ниже), не нуждаются в завершающей точке с запятой.</span><span class="sxs-lookup"><span data-stu-id="8f77a-142">Statements and declarations such as `for` and `operation` that end with a statement block (see below) do not require a terminating semicolon.</span></span>
<span data-ttu-id="8f77a-143">Каждое описание инструкции отмечает, требуется ли завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="8f77a-143">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="8f77a-144">Инструкции, такие как выражения, объявления и директивы, могут быть разбиты на несколько строк.</span><span class="sxs-lookup"><span data-stu-id="8f77a-144">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="8f77a-145">Следует избегать нескольких инструкций в одной строке.</span><span class="sxs-lookup"><span data-stu-id="8f77a-145">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="8f77a-146">Блоки инструкций</span><span class="sxs-lookup"><span data-stu-id="8f77a-146">Statement Blocks</span></span>

<span data-ttu-id="8f77a-147">Инструкции Q # группируются в блоки инструкций.</span><span class="sxs-lookup"><span data-stu-id="8f77a-147">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="8f77a-148">Блок операторов начинается с открытия `{` и заканчивается закрывающим `}` .</span><span class="sxs-lookup"><span data-stu-id="8f77a-148">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="8f77a-149">Блок операторов, который лексической заключен в другой блок, считается вложенным блоком содержащего блока. содержащие и вложенные блоки также называются внешними и внутренними блоками.</span><span class="sxs-lookup"><span data-stu-id="8f77a-149">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="8f77a-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f77a-150">Comments</span></span>

<span data-ttu-id="8f77a-151">Комментарии начинаются с двух косых черт, `//` и продолжаются до конца строки.</span><span class="sxs-lookup"><span data-stu-id="8f77a-151">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="8f77a-152">Комментарий может находиться в любом месте исходного файла Q #.</span><span class="sxs-lookup"><span data-stu-id="8f77a-152">A comment may appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="8f77a-153">Комментарии для документации</span><span class="sxs-lookup"><span data-stu-id="8f77a-153">Documentation Comments</span></span>

<span data-ttu-id="8f77a-154">Комментарии, начинающиеся с трех косых черт, `///` , обрабатываются компилятором специально, когда они появляются непосредственно перед определением пространства имен, операции, специализации, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-154">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="8f77a-155">В этом случае их содержимое берется в виде документации по определенному вызываемому или определяемому пользователем типу, как и для других языков .NET.</span><span class="sxs-lookup"><span data-stu-id="8f77a-155">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="8f77a-156">В `///` комментариях текст, который будет отображаться как часть документации по API, форматируется как [Markdown](https://daringfireball.net/projects/markdown/syntax), а различные части документации указываются с помощью специально именованных заголовков.</span><span class="sxs-lookup"><span data-stu-id="8f77a-156">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="8f77a-157">Как расширение Markdown, перекрестные ссылки на операции, функции и определяемые пользователем типы в Q # могут включаться с помощью `@"<ref target>"` , где `<ref target>` заменяется полным именем объекта кода, на который указывает ссылка.</span><span class="sxs-lookup"><span data-stu-id="8f77a-157">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="8f77a-158">Кроме того, обработчик документации может также поддерживать дополнительные расширения Markdown.</span><span class="sxs-lookup"><span data-stu-id="8f77a-158">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="8f77a-159">Пример:</span><span class="sxs-lookup"><span data-stu-id="8f77a-159">For example:</span></span>

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
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="8f77a-160">Следующие имена распознаются как заголовки комментариев документации.</span><span class="sxs-lookup"><span data-stu-id="8f77a-160">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="8f77a-161">**Сводка**: краткое описание поведения функции или операции или назначения типа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-161">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="8f77a-162">Первый абзац сводки используется для сведений о наведении.</span><span class="sxs-lookup"><span data-stu-id="8f77a-162">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="8f77a-163">Он должен быть обычным текстом.</span><span class="sxs-lookup"><span data-stu-id="8f77a-163">It should be plain text.</span></span>
- <span data-ttu-id="8f77a-164">**Описание**: описание поведения функции или операции, либо назначение типа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-164">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="8f77a-165">Сводные данные и описание объединяются, образуя созданный файл документации для функции, операции или типа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-165">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="8f77a-166">Описание может содержать встроенные LaTeX символы и уравнения.</span><span class="sxs-lookup"><span data-stu-id="8f77a-166">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="8f77a-167">**Входные данные**: описание входного кортежа для операции или функции.</span><span class="sxs-lookup"><span data-stu-id="8f77a-167">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="8f77a-168">Может содержать дополнительные подразделы Markdown, указывающие каждый отдельный элемент входного кортежа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-168">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="8f77a-169">**Output**: описание кортежа, возвращаемого операцией или функцией.</span><span class="sxs-lookup"><span data-stu-id="8f77a-169">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="8f77a-170">**Параметры типа**: пустой раздел, содержащий один дополнительный подраздел для каждого параметра универсального типа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-170">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="8f77a-171">**Пример**. короткий пример используемой операции, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-171">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="8f77a-172">**Примечания**. различные prose, описывающие некоторые аспекты операции, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="8f77a-172">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="8f77a-173">**См. также**: список полных имен, указывающих связанные функции, операции или определяемые пользователем типы.</span><span class="sxs-lookup"><span data-stu-id="8f77a-173">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="8f77a-174">**Ссылки**: список ссылок и ссылок для задокументированного элемента.</span><span class="sxs-lookup"><span data-stu-id="8f77a-174">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="whats-next"></a><span data-ttu-id="8f77a-175">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="8f77a-175">What's Next?</span></span>
<span data-ttu-id="8f77a-176">Сведения об [операциях и функциях](xref:microsoft.quantum.guide.operationsfunctions) в Q #.</span><span class="sxs-lookup"><span data-stu-id="8f77a-176">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>