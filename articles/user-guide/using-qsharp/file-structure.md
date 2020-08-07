---
title: Q#Структура файла
description: Описывает структуру и синтаксис Q# файла.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
no-loc:
- Q#
- $$v
ms.openlocfilehash: ac73962b1a718cd04aa87ee3476c66781fe3ac2b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867936"
---
# <a name="no-locq-file-structure"></a><span data-ttu-id="c9e3c-103">Q#Структура файла</span><span class="sxs-lookup"><span data-stu-id="c9e3c-103">Q# File Structure</span></span>

<span data-ttu-id="c9e3c-104">Q#Файл состоит из последовательности *объявлений пространств имен*.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-104">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="c9e3c-105">Каждое объявление пространства имен содержит объявления для определяемых пользователем типов, операций и функций, а также может содержать любое количество объявлений каждого типа и в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-105">Each namespace declaration contains declarations for user-defined types, operations, and functions, and can contain any number of each type of declaration and in any order.</span></span>
<span data-ttu-id="c9e3c-106">Дополнительные сведения об объявлениях в пространстве имен см. в разделе [определяемые пользователем типы](xref:microsoft.quantum.guide.types#user-defined-types), [операции](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)и [функции](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).</span><span class="sxs-lookup"><span data-stu-id="c9e3c-106">For more information on declarations within a namespace, see [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).</span></span>

<span data-ttu-id="c9e3c-107">Единственный текст, который может находиться за пределами объявления пространства имен, — это комментарии.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="c9e3c-108">В частности, комментарии к документации для пространства имен предшествуют объявлению.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-108">In particular, documentation comments for a namespace precede the declaration.</span></span> <span data-ttu-id="c9e3c-109">Дополнительные сведения см. в [комментариях к документации](#documentation-comments) в этой статье.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-109">For more information, see [Documentation comments](#documentation-comments) in this article.</span></span> 

## <a name="namespace-declarations"></a><span data-ttu-id="c9e3c-110">Объявление пространств имен</span><span class="sxs-lookup"><span data-stu-id="c9e3c-110">Namespace Declarations</span></span>

<span data-ttu-id="c9e3c-111">Q#Как правило, файл содержит только одно объявление пространства имен, но может иметь значение None (и быть пустым или содержать только комментарии) или содержать несколько пространств имен.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-111">A Q# file typically has just one namespace declaration, but could have none (and be empty or just contain comments) or could contain multiple namespaces.</span></span>
<span data-ttu-id="c9e3c-112">Объявления пространств имен не могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-112">Namespace declarations can not be nested.</span></span>

<span data-ttu-id="c9e3c-113">Одно и то же пространство имен можно объявить в нескольких Q# файлах, компилируемых вместе, если нет объявлений типа, операции или функции с одним и тем же именем.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-113">You can declare the same namespace in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="c9e3c-114">В частности, нельзя определить один и тот же тип в одном пространстве имен в нескольких файлах, даже если объявления идентичны.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-114">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="c9e3c-115">Объявление пространства имен состоит из ключевого слова `namespace` , за которым следует имя пространства имен и объявления, содержащиеся в пространстве имен, заключенном в фигурные скобки `{ }` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-115">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, and the declarations contained in the namespace enclosed in braces `{ }`.</span></span>
<span data-ttu-id="c9e3c-116">Имена пространств имен соответствуют шаблону .NET последовательности из одного или нескольких юридических символов, разделенных точками `.` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-116">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="c9e3c-117">Например, `MyQuantumStuff` и `Microsoft.Quantum.Intrinsic` являются допустимыми именами пространств имен.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-117">For example, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="c9e3c-118">По соглашению символы в имени пространства имен можно заменять на прописные, однако это не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-118">By convention, capitalize the symbols in a namespace name, however, this is not required.</span></span>

<span data-ttu-id="c9e3c-119">Ссылки на типы или вызываемые объекты, объявленные ниже в файле, разрешаются надлежащим образом. нет необходимости в объявлении типа, операции или функции перед ссылкой на нее.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-119">References to types or callables declared further down in a file resolve properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="c9e3c-120">Открытые директивы</span><span class="sxs-lookup"><span data-stu-id="c9e3c-120">Open Directives</span></span>

<span data-ttu-id="c9e3c-121">В блоке пространства имен используйте `open` директиву, чтобы импортировать все типы и вызываемые, объявленные в определенном пространстве имен, и ссылаться на них по их неполному имени.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-121">Within a namespace block, use the `open` directive to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="c9e3c-122">Такая `open` директива состоит из `open` ключевого слова, за которым следует открытое пространство имен и завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="c9e3c-123">Все `open` директивы должны находиться перед `function` `operation` объявлениями, или `newtype` в блоке пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-123">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="c9e3c-124">При необходимости можно определить короткое имя для открытого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-124">Optionally, you can define a short name for the opened namespace.</span></span> <span data-ttu-id="c9e3c-125">Если задано короткое имя, необходимо уточнить все элементы из этого пространства имен на определенное короткое имя.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-125">If a short name is defined, you must qualify all elements from that namespace by the defined short name.</span></span> <span data-ttu-id="c9e3c-126">Например, учитывая следующее объявление пространства имен и открытые директивы,</span><span class="sxs-lookup"><span data-stu-id="c9e3c-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="c9e3c-127">Если в объявленной операции используется операция `Op` из `Microsoft.Quantum.Intrinsic` , ее можно вызвать, просто используя `Op` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-127">if a declared operation uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, you call it by simply using `Op`.</span></span>
<span data-ttu-id="c9e3c-128">Однако для вызова определенной функции из необходимо `Fn` `Microsoft.Quantum.Math` вызвать ее с помощью `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-128">However, to call a certain function `Fn` from `Microsoft.Quantum.Math`, you must call it using `Math.Fn`.</span></span>

<span data-ttu-id="c9e3c-129">`open`Директива применяется ко всему блоку пространства имен в файле.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="c9e3c-130">Следовательно, если определить дополнительное пространство имен в том же Q# файле, что и `NS` ранее, то любые операции, функции и типы, определенные во втором пространстве имен, не будут иметь доступа ни к чему, ни к `Microsoft.Quantum.Intrinsic` `Microsoft.Quantum.Math` тому или только если вы повторно выпустили директивы Open.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-130">Hence, if you define an additional namespace in the same Q# file as `NS` earlier, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless you repeated the open directives therein.</span></span> 

<span data-ttu-id="c9e3c-131">Чтобы сослаться на тип или вызываемый, определенный в другом пространстве имен, который *не* открыт в текущем пространстве имен, необходимо создать ссылку на него по полному имени.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-131">To reference a type or callable defined in another namespace that is *not* opened in the current namespace, you must reference it by its fully-qualified name.</span></span>
<span data-ttu-id="c9e3c-132">Например, для операции с именем `Op` из `X.Y` пространства имен:</span><span class="sxs-lookup"><span data-stu-id="c9e3c-132">For example, given an operation named `Op` from the `X.Y` namespace:</span></span>

* <span data-ttu-id="c9e3c-133">Необходимо создать ссылку на него по полному имени `X.Y.Op` , если только `X.Y` пространство имен не было открыто ранее в текущем блоке.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-133">You must reference it by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> 
* <span data-ttu-id="c9e3c-134">Даже если `X` пространство имен открыто, нельзя ссылаться на операцию как `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-134">Even if the `X` namespace is opened, it is not possible to reference the operation as `Y.Op`.</span></span>
* <span data-ttu-id="c9e3c-135">Если вы определили короткое имя `Z` для `X.Y` в этом пространстве имен и файле, необходимо указать ссылку `Op` как `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-135">If you defined the short name `Z` for `X.Y` in that namespace and file, you must reference `Op` as `Z.Op`.</span></span> 

<span data-ttu-id="c9e3c-136">Обычно лучше включать пространство имен с помощью `open` директивы.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-136">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="c9e3c-137">Использование полного имени требуется, если два пространства имен определяют конструкции с одинаковым именем, а текущий источник использует конструкции из обоих.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-137">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="c9e3c-138">Q#следует тем же правилам для именования, что и для других языков .NET.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-138">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="c9e3c-139">Однако не Q# поддерживает относительные ссылки на пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-139">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="c9e3c-140">Например, если пространство имен `a.b` открыто, ссылка на операцию с именем не `c.d` разрешается *not* в операцию с полным именем `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-140">For example, if the namespace `a.b` is open, a reference to an operation named `c.d` does *not* resolve to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="c9e3c-141">Форматирование</span><span class="sxs-lookup"><span data-stu-id="c9e3c-141">Formatting</span></span>

<span data-ttu-id="c9e3c-142">Большинство Q# инструкций и директив заканчиваются завершающей точкой с запятой, `;` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-142">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="c9e3c-143">Инструкции и объявления, такие как `for` и `operation` , заканчивающиеся блоком операторов (см. следующий раздел), не нуждаются в завершающей точке с запятой.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-143">Statements and declarations such as `for` and `operation` that end with a statement block (see the following section) do not require a terminating semicolon.</span></span>
<span data-ttu-id="c9e3c-144">Каждое описание инструкции отмечает, требуется ли завершающая точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-144">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="c9e3c-145">Инструкции, такие как выражения, объявления и директивы, можно разделить на несколько строк.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-145">Statements, like expressions, declarations, and directives, can be broken out across multiple lines.</span></span>
<span data-ttu-id="c9e3c-146">Старайтесь не размещать несколько инструкций в одной строке.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-146">Avoid putting multiple statements on a single line.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="c9e3c-147">Блоки инструкций</span><span class="sxs-lookup"><span data-stu-id="c9e3c-147">Statement Blocks</span></span>

<span data-ttu-id="c9e3c-148">Q#Операторы группируются в блоки инструкций, которые содержатся в фигурных скобках `{ }` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-148">Q# statements are grouped into statement blocks, which are contained with braces `{ }`.</span></span> <span data-ttu-id="c9e3c-149">Блок операторов начинается с открытия `{` и заканчивается закрывающим `}` .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-149">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="c9e3c-150">Блок операторов, который лексической заключен в другой блок, считается вложенным блоком содержащего блока. содержащие и вложенные блоки также называются внешними и внутренними блоками.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-150">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="c9e3c-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9e3c-151">Comments</span></span>

<span data-ttu-id="c9e3c-152">Комментарии начинаются с двух косых черт, `//` и продолжаются до конца строки.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-152">Comments begin with two forward slashes, `//`, and continue until the end of the line.</span></span>
<span data-ttu-id="c9e3c-153">Комментарий может находиться в любом месте Q# исходного файла.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-153">A comment can appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="c9e3c-154">Комментарии для документации</span><span class="sxs-lookup"><span data-stu-id="c9e3c-154">Documentation Comments</span></span>

<span data-ttu-id="c9e3c-155">Комментарии, начинающиеся с трех косых черт, `///` , обрабатываются компилятором специально, когда они появляются непосредственно перед определением пространства имен, операции, специализации, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-155">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="c9e3c-156">В этом случае компилятор обрабатывает их как документацию для определенного вызываемого или определяемого пользователем типа, аналогично другим языкам .NET.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-156">In that case, the compiler treats them as documentation for the defined callable or user-defined type, the same as other .NET languages.</span></span>

<span data-ttu-id="c9e3c-157">Внутри `///` комментариев текст, который будет отображаться как часть документации по API, форматируется как [Markdown](https://daringfireball.net/projects/markdown/syntax), а различные части документации — с помощью специально именованных заголовков.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-157">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation indicated by specially-named headers.</span></span>
<span data-ttu-id="c9e3c-158">В Markdown используйте `@"<ref target>"` расширение для операций с перекрестными ссылками, функций и определяемых пользователем типов в Q# .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-158">In Markdown, use the `@"<ref target>"` extension to cross-reference operations, functions, and user-defined types in Q#.</span></span> <span data-ttu-id="c9e3c-159">Замените на полное `<ref target>` имя упоминаемого объекта кода.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-159">Replace `<ref target>` with the fully qualified name of the referenced code object.</span></span>
<span data-ttu-id="c9e3c-160">Различные обработчики документации также могут поддерживать дополнительные расширения Markdown.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-160">Different documentation engines may also support additional Markdown extensions.</span></span>

<span data-ttu-id="c9e3c-161">Пример:</span><span class="sxs-lookup"><span data-stu-id="c9e3c-161">For example:</span></span>

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

<span data-ttu-id="c9e3c-162">Следующие имена являются допустимыми в качестве заголовков комментариев документации.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-162">The following names are valid as documentation comment headers.</span></span>

- <span data-ttu-id="c9e3c-163">**Сводка**: краткое описание поведения функции или операции или назначение типа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-163">**Summary**: A short summary of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="c9e3c-164">Первый абзац сводки используется для сведений о наведении.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-164">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="c9e3c-165">Он должен быть обычным текстом.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-165">It should be plain text.</span></span>
- <span data-ttu-id="c9e3c-166">**Описание**: описание поведения функции или операции или назначение типа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-166">**Description**: A description of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="c9e3c-167">Вместе сводка и описание формируют созданный файл документации для функции, операции или типа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-167">Together, the summary and description form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="c9e3c-168">Описание поддерживает встроенные в LaTeX символы и уравнения.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-168">The description supports in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="c9e3c-169">**Входные данные**: описание входного кортежа для операции или функции.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-169">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="c9e3c-170">Может содержать дополнительные подразделы Markdown, указывающие каждый элемент входного кортежа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-170">Can contain additional Markdown subsections indicating each element of the input tuple.</span></span>
- <span data-ttu-id="c9e3c-171">**Output**: описание кортежа, возвращаемого операцией или функцией.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-171">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="c9e3c-172">**Параметры типа**: пустой раздел, содержащий один дополнительный подраздел для каждого параметра универсального типа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-172">**Type Parameters**: An empty section that contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="c9e3c-173">**Пример**. Краткий пример использования операции, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-173">**Example**: A short example of the operation, function, or type in use.</span></span>
- <span data-ttu-id="c9e3c-174">**Примечания**. различные prose, описывающие некоторые аспекты операции, функции или типа.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-174">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="c9e3c-175">**См. также**: список полных имен, указывающих связанные функции, операции или определяемые пользователем типы.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-175">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="c9e3c-176">**Ссылки**: список ссылок и ссылки на задокументированный элемент.</span><span class="sxs-lookup"><span data-stu-id="c9e3c-176">**References**: A list of references and citations for the documented item.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c9e3c-177">Дальнейшие шаги</span><span class="sxs-lookup"><span data-stu-id="c9e3c-177">Next steps</span></span>

<span data-ttu-id="c9e3c-178">Сведения об [операциях и функциях](xref:microsoft.quantum.guide.operationsfunctions) в Q# .</span><span class="sxs-lookup"><span data-stu-id="c9e3c-178">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>