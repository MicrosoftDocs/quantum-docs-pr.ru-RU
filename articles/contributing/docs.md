---
title: Дополнение к документации по Microsoft КДК
description: Узнайте, как вносить концептуальные материалы или содержимое API в набор документации по Microsoft тактов.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.docs
ms.openlocfilehash: ed5ab5df9de5d71ccd922cd430cf15779806dd6a
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022632"
---
# <a name="improving-documentation"></a><span data-ttu-id="ab0b4-103">Улучшение документации</span><span class="sxs-lookup"><span data-stu-id="ab0b4-103">Improving Documentation</span></span>

<span data-ttu-id="ab0b4-104">Документация по пакету разработки тактовой задержки принимает несколько различных форм, что позволяет разработчикам тактов получить доступ к информации.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-104">The documentation for the Quantum Development Kit takes on several different forms, such that information is readily available to quantum developers.</span></span>

<span data-ttu-id="ab0b4-105">Следуя принципам работы с [документами в качестве кода](https://www.writethedocs.org/guide/docs-as-code/), вся документация по пакету разработки такта форматируется как код и управляется с помощью Git так же, как и исходный код, используемый для создания пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-105">Following the principles of [Docs as Code](https://www.writethedocs.org/guide/docs-as-code/), all Quantum Development Kit documentation is formatted as code and is managed using Git in the same way as the source code that is used to build the Quantum Development Kit.</span></span>
<span data-ttu-id="ab0b4-106">В большинстве случаев резервная документация по коду состоит из различных форм [Markdown](https://daringfireball.net/projects/markdown/), языка для написания форматированного текста в виде обычного текста, который легко использовать в командной строке, в IDE и в системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-106">For the most part, the code backing documentation consists of various forms of [Markdown](https://daringfireball.net/projects/markdown/), a language for writing out richly formatted text in a plain text format that's easy to use at the command line, in IDEs, and with source control.</span></span>
<span data-ttu-id="ab0b4-107">Мы также используем библиотеку [масжакс](https://www.mathjax.org/) , чтобы обеспечить форматирование математики в документации с помощью языка LaTeX, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-107">We similarly adopt the [MathJax](https://www.mathjax.org/) library to allow for formatting mathematics in documentation using the LaTeX language, as detailed further below.</span></span>


<span data-ttu-id="ab0b4-108">С другой стороны, каждая форма документации немного различается в деталях:</span><span class="sxs-lookup"><span data-stu-id="ab0b4-108">That said, each form of documentation does vary somewhat in the details:</span></span>

- <span data-ttu-id="ab0b4-109">**Концептуальная документация** состоит из набора статей, опубликованных в https://docs.microsoft.com/quantumи описывающих все, от основ тактовых вычислений до технических спецификаций для форматов обмена.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-109">The **conceptual documentation** consists of a set of articles that are published to https://docs.microsoft.com/quantum, and that describe everything from the basics of quantum computing to the technical specifications for interchange formats.</span></span> <span data-ttu-id="ab0b4-110">Эти статьи написаны на [DocFX Markdown (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html), Markdown вариант, используемый для создания обширных наборов документации.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-110">These articles are written in [DocFX-Flavored Markdown (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html), a Markdown variant used for creating rich documentation sets.</span></span>
- <span data-ttu-id="ab0b4-111">**Справочник по API** — это набор страниц для каждой функции Q #, операции и определяемого пользователем типа, опубликованный в https://docs.microsoft.com/qsharp/api/.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-111">The **API reference** is a set of pages for each Q# function, operation, and user-defined type, published to https://docs.microsoft.com/qsharp/api/.</span></span> <span data-ttu-id="ab0b4-112">Эти страницы задокументированы входы и операции для каждого вызова, а также примеры и ссылки на дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-112">These pages document the inputs and operations to each callable, along with examples and links to more information.</span></span> <span data-ttu-id="ab0b4-113">Справочник по API автоматически извлекается из небольших документов DFM в исходном коде Q # в составе каждого выпуска.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-113">The API reference is automatically extracted from small DFM documents in Q# source code as a part of each release.</span></span>
- <span data-ttu-id="ab0b4-114">Файлы **сведений<!---->. md** , включенные в каждый пример и Ката, описывают, как использовать этот пример или Ката, что он охватывает и как он связан с остальной частью пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-114">The **README<!---->.md** files included with each sample and kata describe how to use that sample or kata is used, what it covers, and how it relates to the rest of the Quantum Development Kit.</span></span> <span data-ttu-id="ab0b4-115">Эти файлы пишутся с помощью [GitHub Markdown (GFM)](https://github.github.com/gfm/), более простой альтернативы DFM, который часто используется для присоединения документации непосредственно к репозиториям кода.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-115">These files are written using [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/), a more lightweight alternative to DFM that's popular for attaching documentation directly to code repositories.</span></span>

## <a name="contributing-to-the-conceptual-documentation"></a><span data-ttu-id="ab0b4-116">Вклад в концептуальную документацию</span><span class="sxs-lookup"><span data-stu-id="ab0b4-116">Contributing to the Conceptual Documentation</span></span>

<span data-ttu-id="ab0b4-117">Чтобы внести улучшения в общую документацию или документация с файлами сведений, следует начать с запроса на вытягивание в [**MicrosoftDocs/такт-куантумкатас-PR**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**Microsoft/такт**](https://github.com/Microsoft/Quantum)или [**Microsoft/** ](https://github.com/Microsoft/QuantumKatas).</span><span class="sxs-lookup"><span data-stu-id="ab0b4-117">To contribute an improvement to the conceptual or README documentation, then, starts with a pull request onto either [**MicrosoftDocs/quantum-docs-pr**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**Microsoft/Quantum**](https://github.com/Microsoft/Quantum), or [**Microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas), as is appropriate.</span></span>
<span data-ttu-id="ab0b4-118">Мы подробно расскажем о запросах на вытягивание, но для этого у нас есть несколько вещей, которые следует учитывать при улучшении документации:</span><span class="sxs-lookup"><span data-stu-id="ab0b4-118">We'll describe more about pull requests below, but for now there's a few things that are good to keep in mind as you improve documentation:</span></span>

- <span data-ttu-id="ab0b4-119">Читатели поставляются в документацию по пакету разработки тактов из самых широкого спектра фоновых рисунков.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-119">Readers come to the Quantum Development Kit documentation from a very wide range of backgrounds.</span></span> <span data-ttu-id="ab0b4-120">Все пользователи из старших учебных заведений, которые узнают о новых возможностях просмотрим факультета, выполняющего исследование тактовых вычислений, должны иметь возможность избавиться от необходимости читать документацию.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-120">Everyone from high school students looking to learn something new and exciting through to tenured faculty performing quantum computing research should be able to get something out of reading the documentation.</span></span> <span data-ttu-id="ab0b4-121">В то же время вы можете не получать обширных знаний о части читателей, так как они могут быть просто запущены. Это наиболее полезно, если вы можете предоставить четкие и доступные описания или предоставить ссылки на другие ресурсы для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-121">To the extent that's possible, please don't assume extensive knowledge on the part of your readers, as they may just be starting out. It's most helpful if you can provide clear and accessible descriptions, or can provide links to other resources for more information.</span></span>
- <span data-ttu-id="ab0b4-122">Наборы документации не размещаются в виде книг или документов, в том, что читатели будут поступать на то, что может показаться «средней».</span><span class="sxs-lookup"><span data-stu-id="ab0b4-122">Documentation sets aren't laid out like books or papers, in that readers will arrive in what might seem like the "middle."</span></span> <span data-ttu-id="ab0b4-123">Например, поисковые системы могут не предлагать индекс, или же они могли бы отправить ссылку друг на друга. Постарайтесь помочь вашему читателю, всегда предоставляя понятный контекст и ссылки там, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-123">For example, search engines might not suggest the index, or they might have been sent a link by a friend trying to help them out. Try to help your reader by always providing a clear context, along with links where appropriate.</span></span>
- <span data-ttu-id="ab0b4-124">Некоторые читатели найдут наиболее полезные абстрактные операторы и определения, а другие читатели лучше всего работают путем экстраполяции из конкретных примеров.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-124">Some readers will find abstract statements and definitions most helpful, while other readers work best by extrapolating from concrete examples.</span></span> <span data-ttu-id="ab0b4-125">Как общий случай, так и конкретные примеры могут помочь читателям максимально эффективно программировать такты.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-125">Providing both the general case and specific examples can help both readers get the most out of quantum programming.</span></span>
- <span data-ttu-id="ab0b4-126">В особенности, если вы также написали задокументированный код, некоторые из них могут быть очевидны, что не все очевидны для читателя.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-126">Especially if you also wrote the code being documented, things may be obvious to you that are not at all obvious to your reader.</span></span> <span data-ttu-id="ab0b4-127">Нет ни одного уникального способа программирования, так что независимо от того, насколько разумны или опытные читатели не могут быть, они не могут предположить, какие шаблоны проектирования вы нашли наиболее полезными для выражения идей в коде.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-127">There's no one unique best way to program, so no matter how clever or experienced a reader might be, they can't guess at what design patterns you found the most helpful to express your ideas in code.</span></span> <span data-ttu-id="ab0b4-128">Ясно, как читатель может использовать ваш код, чтобы предоставить этот контекст.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-128">Being clear about how a reader can expect to make use of your code can help provide that context.</span></span>
- <span data-ttu-id="ab0b4-129">Многие члены сообщества по программированию тактов — это научные судебные работы, которые распознаются главным образом посредством ссылок для их вклада в сообщество.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-129">Many members of the quantum programming community are academic researchers, and are recognized mainly through citations for their contributions to the community.</span></span> <span data-ttu-id="ab0b4-130">Помимо того, чтобы помочь читателям найти дополнительные материалы, убедитесь, что они должным образом заключить такие выводы, как документы, обсуждения, записи в блоге и программные средства, которые помогут участникам, чтобы помочь пользователям улучшить сообщество.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-130">In addition to helping readers find additional materials, making sure to properly cite academic outputs such as papers, talks, blog posts, and software tools can help academic contributors to keep doing their best work to improve the community.</span></span>
- <span data-ttu-id="ab0b4-131">Сообщество по программированию тактов — это широкое и замечательное сообщество.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-131">The quantum programming community is a broad and wonderfully diverse community.</span></span> <span data-ttu-id="ab0b4-132">Использование Пол-существительных в примерах третьих лиц (например, «если пользователь...») может привести к исключению, а не к включению.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-132">The use of gendered pronouns in third-person examples (e.g.: "if a user ..., he will ...") can work to exclude rather than include.</span></span> <span data-ttu-id="ab0b4-133">Компания cognizant имена людей в ссылках и ссылки, а правильное включение символов, отличных от ASCII, может привести к разнообразию сообщества, показывая о его членах.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-133">Being cognizant of people's names in citations and links, and of the correct inclusion of non-ASCII characters can serve the diversity of the community by showing respect to its members.</span></span> <span data-ttu-id="ab0b4-134">Аналогичным образом, многие слова на английском языке часто используются хатефул способом, поэтому их использование в технической документации может привести к тому, что они будут нести вред отдельным читателям и сообществу в целом.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-134">Similarly, many words in the English language are often used in a hateful manner, such that their use in technical documentation can cause harm both to individual readers and to the community at large.</span></span>

### <a name="referencing-sample-code-from-conceptual-articles"></a><span data-ttu-id="ab0b4-135">Создание ссылок на примеры кода из концептуальных статей</span><span class="sxs-lookup"><span data-stu-id="ab0b4-135">Referencing Sample Code from Conceptual Articles</span></span>

<span data-ttu-id="ab0b4-136">Если вы хотите включить код из [репозитория Samples](https://github.com/Microsoft/Quantum), это можно сделать с помощью специальной команды Markdown DocFX:</span><span class="sxs-lookup"><span data-stu-id="ab0b4-136">If you want to include code from the [samples repository](https://github.com/Microsoft/Quantum), you can do so using a special DocFX-Flavored Markdown command:</span></span>

```markdown
:::code language="qsharp" source="~/quantum/samples/algorithms/chsh-game/Game.qs" range="4-8":::
```

<span data-ttu-id="ab0b4-137">Эта команда импортирует строки 4 – 8 из [файла`Game.qs` из примера `chsh-game`](https://github.com/microsoft/Quantum/blob/master/samples/algorithms/chsh-game/Game.qs), помечая их как код Q # для выделения синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-137">This command will import lines 4 to 8 of the [`Game.qs` file from the `chsh-game` sample](https://github.com/microsoft/Quantum/blob/master/samples/algorithms/chsh-game/Game.qs), marking them as Q# code for the purpose of syntax highlighting.</span></span>
<span data-ttu-id="ab0b4-138">С помощью этой команды можно избежать дублирования кода между концептуальными статьями и репозиторием примеров, чтобы образец кода в документации всегда был как можно более актуальным.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-138">Using this command, you can avoid duplicating code between conceptual articles and the samples repository, so that sample code in documentation is always as up to date as possible.</span></span>

## <a name="contributing-to-the-api-references"></a><span data-ttu-id="ab0b4-139">Дополнение к ссылкам на API</span><span class="sxs-lookup"><span data-stu-id="ab0b4-139">Contributing to the API References</span></span>

<span data-ttu-id="ab0b4-140">Чтобы внести улучшения в ссылки API, очень полезно открыть запрос на вытягивание непосредственно в задокументированном коде.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-140">To contribute an improvement to the API references, it's most helpful to open a pull request directly on the code being documented.</span></span>
<span data-ttu-id="ab0b4-141">Каждая функция, операция или определяемый пользователем тип поддерживает комментарий к документации (обозначенный `///` вместо `//`).</span><span class="sxs-lookup"><span data-stu-id="ab0b4-141">Each function, operation, or user-defined type supports a documentation comment (denoted with `///` instead of `//`).</span></span>
<span data-ttu-id="ab0b4-142">При компиляции каждого выпуска пакета средств разработки тактов эти комментарии используются для создания справочника по API на https://docs.microsoft.com/qsharp/api/, включая сведения о входах и выходных данных каждого из вызываемых функций, предположения о каждом вызываемом методе и примеры их использования.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-142">When we compile each release of the Quantum Development Kit, these comments are used to generate the API reference at https://docs.microsoft.com/qsharp/api/, including details about the inputs to and outputs from each callable, the assumptions each callable makes, and examples of how to use them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab0b4-143">Не изменяйте созданную документацию по API вручную, так как эти файлы перезаписываются с каждым новым выпуском.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-143">Please make sure to not manually edit the generated API documentation, as these files are overwritten with each new release.</span></span>
> <span data-ttu-id="ab0b4-144">Мы предлагаем вам вклад в сообщество и хотим убедиться, что изменения продолжают помочь пользователям выпустить после выпуска.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-144">We value your contribution to the community, and want to make sure that your changes continue to help users release after release.</span></span>

<span data-ttu-id="ab0b4-145">Например, рассмотрим функцию `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-145">For example, consider the function `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="ab0b4-146">Комментарий к документации должен помочь пользователю узнать, как интерпретировать `bits` и `oracle` и функции.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-146">A documentation comment should help a user learn how to interpret `bits` and `oracle` and what the function is for.</span></span>
<span data-ttu-id="ab0b4-147">Каждый из этих частей информации может предоставляться компилятору Q # с помощью специально названного раздела Markdown в комментарии к документации.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-147">Each of these different pieces of information can be provided to the Q# compiler by a specially named Markdown section in the documentation comment.</span></span>
<span data-ttu-id="ab0b4-148">В качестве примера `ControlledOnBitString`можно написать нечто вроде следующего:</span><span class="sxs-lookup"><span data-stu-id="ab0b4-148">For the example of `ControlledOnBitString`, we might write something like the following:</span></span>

```qsharp
 /// # Summary
 /// Returns a unitary operation that applies an oracle on the target register if the 
 /// control register state corresponds to a specified bit mask.
 ///
 /// # Description
 /// The output of this function is an operation that can be represented by a
 /// unitary transformation $U$ such that
 /// \begin{align}
 ///     U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes
 ///     \begin{cases}
 ///         V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\
 ///         \ket{\psi} & \textrm{otherwise}
 ///     \end{cases},
 /// \end{align}
 /// where $V$ is a unitary transformation that represents the action of the
 /// `oracle` operation.
 ///
 /// # Input
 /// ## bits
 /// The bit string to control the given unitary operation on.
 /// ## oracle
 /// The unitary operation to be applied on the target register.
 ///
 /// # Output
 /// A unitary operation that applies `oracle` on the target register if the control 
 /// register state corresponds to the bit mask `bits`.
 ///
 /// # Remarks
 /// The length of `bits` and `controlRegister` must be equal.
 ///
 /// Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function
 /// is an operation that performs the following steps:
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits`;
 /// * apply `Controlled oracle` to the control and target registers;
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits` again to return the control register to the original state.
 ///
 /// The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.
 ///
 /// # Example
 /// The following code snippets are equivalent:
 /// ```qsharp
 /// (ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
 /// ```
 /// and
 /// ```qsharp
 /// within {
 ///     ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
 /// } apply {
 ///     Controlled oracle(controlRegister, targetRegister);
 /// }
 /// ```
 ///
 /// The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:
 /// ```qsharp
 /// using (register = Qubit[2]) {
 ///     ApplyToEach(H, register);
 ///     (ControlledOnBitString([false], Z))(register[0..0], register[1]);
 /// }
 /// ```
 function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
 {
     return ControlledOnBitStringImpl(bits, oracle, _, _);
 }
```

<span data-ttu-id="ab0b4-149">Отображаемую версию кода, приведенную выше, можно увидеть в [документации по API для функции `ControlledOnBitString`](xref:microsoft.quantum.canon.controlledonbitstring).</span><span class="sxs-lookup"><span data-stu-id="ab0b4-149">You can see the rendered version of the code above in the [API documentation for the `ControlledOnBitString` function](xref:microsoft.quantum.canon.controlledonbitstring).</span></span>

<span data-ttu-id="ab0b4-150">В дополнение к общей практике написания документации по написанию комментариев к документации по API он помогает в уме некоторые моменты.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-150">In addition to the general practice of documentation writing, in writing API documentation comments it helps to keep a few things in mind:</span></span>

- <span data-ttu-id="ab0b4-151">Формат каждого комментария документации должен совпадать с тем, что компилятор Q # ожидает, чтобы ваша документация отображалась правильно.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-151">The format of each documentation comment has to match what the Q# compiler expects for your documentation to appear correctly.</span></span> <span data-ttu-id="ab0b4-152">Некоторые разделы, например `/// # Remarks` позволяют использовать произвольное содержимое, в то время как разделы, такие как `/// # See Also` разделе, являются более узкими.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-152">Some sections, such as `/// # Remarks` allow for freeform content, while sections such as `/// # See Also` section are more restrictive.</span></span>
- <span data-ttu-id="ab0b4-153">Читатель может прочитать документацию по API на основном эталонном сайте API, сводку по каждому пространству имен или даже в интегрированной среде разработки, используя сведения о наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-153">A reader may read your API documentation on the main API reference site, on the summary for each namespace, or even from within their IDE through the use of hover information.</span></span> <span data-ttu-id="ab0b4-154">Убедитесь, что `/// # Summary` не длиннее, чем предложение, поможет читателям быстро отсортировать информацию о том, нужно ли читать их дальше или искать в других местах, а также быстро просканировать сводки пространств имен.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-154">Making sure that `/// # Summary` isn't longer than about a sentence helps your reader quickly sort out whether they need to read further or look elsewhere, and can help in quickly scanning through namespace summaries.</span></span>
- <span data-ttu-id="ab0b4-155">Ваша документация может быть хорошо занимать намного больше времени, чем сам код, но это нормально!</span><span class="sxs-lookup"><span data-stu-id="ab0b4-155">Your documentation may well wind up being much longer than the code itself, but that's OK!</span></span> <span data-ttu-id="ab0b4-156">Даже небольшой фрагмент кода может иметь неожиданные последствия для пользователей, которые не узнают контекст, в котором существует код.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-156">Even a small piece of code can have unexpected effects to users that don't know the context in which that code exists.</span></span> <span data-ttu-id="ab0b4-157">Предоставляя конкретные примеры и четкие объяснения, пользователи могут помочь пользователям лучше использовать код, доступный для них.</span><span class="sxs-lookup"><span data-stu-id="ab0b4-157">By providing concrete examples and clear explanations, you can help users make the best use of the code that's available to them.</span></span>

<!-- ## LaTeX Formatting ##

**TODO** -->
