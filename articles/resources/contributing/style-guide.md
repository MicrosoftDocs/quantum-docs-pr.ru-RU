---
title: :::no-loc(Q#):::Руководству по стилю Майкрософт
description: 'Сведения об именовании, вводе, документации и соглашениях о форматировании для :::no-loc(Q#)::: программ и библиотек.'
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 7666974e255d537c8d611d0077b7f9b37a61f918
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691730"
---
# <a name="no-locq-style-guide"></a><span data-ttu-id="22bb0-103">:::no-loc(Q#)::: Рекомендации по стилю</span><span class="sxs-lookup"><span data-stu-id="22bb0-103">:::no-loc(Q#)::: Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="22bb0-104">Общие соглашения</span><span class="sxs-lookup"><span data-stu-id="22bb0-104">General Conventions</span></span> ##

<span data-ttu-id="22bb0-105">Соглашения, предлагаемые в этом разделе, призваны помочь сделать программы и библиотеки более удобочитаемыми :::no-loc(Q#)::: и понятными.</span><span class="sxs-lookup"><span data-stu-id="22bb0-105">The conventions suggested in this guide are intended to help make programs and libraries written in :::no-loc(Q#)::: easier to read and understand.</span></span>

## <a name="guidance"></a><span data-ttu-id="22bb0-106">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-106">Guidance</span></span>

<span data-ttu-id="22bb0-107">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-107">We suggest:</span></span>

- <span data-ttu-id="22bb0-108">Не следует игнорировать соглашение, если это не сделано намеренно, чтобы предоставить пользователям более понятный и понятный код.</span><span class="sxs-lookup"><span data-stu-id="22bb0-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="22bb0-109">Соглашения об именах</span><span class="sxs-lookup"><span data-stu-id="22bb0-109">Naming Conventions</span></span> ##

<span data-ttu-id="22bb0-110">В составе пакета средств разработки тактов мы стремимся использовать имена функций и операций, которые помогают разработчикам создавать программы, которые просты в чтении, и сокращают их сюрприз.</span><span class="sxs-lookup"><span data-stu-id="22bb0-110">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="22bb0-111">Важной частью является то, что при выборе имен для функций, операций и типов мы создаем *словарь* , используемый программистами для выражения тактовых концепций. с нашими вариантами мы можем либо отнестись к их усилиям, чтобы четко взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="22bb0-111">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="22bb0-112">Это полагает ответственность за то, чтобы имена, которые мы предложит, были понятны, а не скрыты.</span><span class="sxs-lookup"><span data-stu-id="22bb0-112">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="22bb0-113">В этом разделе мы подробно расскажу о том, как мы удовлетворены этим обязательством с точки зрения явных руководств, которые помогут нам лучше всего сделать это в :::no-loc(Q#)::: сообществе разработчиков.</span><span class="sxs-lookup"><span data-stu-id="22bb0-113">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the :::no-loc(Q#)::: development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="22bb0-114">Операции и функции</span><span class="sxs-lookup"><span data-stu-id="22bb0-114">Operations and Functions</span></span> ###

<span data-ttu-id="22bb0-115">Одно из первых действий, которое должно установить имя, — это то, представляет ли заданный символ функцию или операцию.</span><span class="sxs-lookup"><span data-stu-id="22bb0-115">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="22bb0-116">Разница между функциями и операциями крайне важна для понимания того, как работает блок кода.</span><span class="sxs-lookup"><span data-stu-id="22bb0-116">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="22bb0-117">Чтобы обеспечить различие между функциями и операциями для пользователей, мы будем полагаться на то, что модели зависят от :::no-loc(Q#)::: использования побочных эффектов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-117">To communicate the distinction between functions and operations to users, we rely on that :::no-loc(Q#)::: models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="22bb0-118">Это значит, что операция *делает* что-то.</span><span class="sxs-lookup"><span data-stu-id="22bb0-118">That is, an operation *does* something.</span></span>

<span data-ttu-id="22bb0-119">Функции, напротив, описывают математические связи между данными.</span><span class="sxs-lookup"><span data-stu-id="22bb0-119">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="22bb0-120">Выражение `Sin(PI() / 2.0)` *имеет* значение `1.0` и не подразумевает ничего о состоянии программы или ее Кубитс.</span><span class="sxs-lookup"><span data-stu-id="22bb0-120">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="22bb0-121">Формирование сводных данных, операции выполняются, когда функции являются объектами.</span><span class="sxs-lookup"><span data-stu-id="22bb0-121">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="22bb0-122">Это различие подразумевает, что операции именования являются глаголами и функциями в качестве существительных.</span><span class="sxs-lookup"><span data-stu-id="22bb0-122">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="22bb0-123">При объявлении определяемого пользователем типа Новая функция, которая конструирует экземпляры этого типа, неявно определяется в то же время.</span><span class="sxs-lookup"><span data-stu-id="22bb0-123">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="22bb0-124">С этой точки зрения определяемые пользователем типы должны называться существительными, чтобы оба типа и функции конструктора имели одинаковые имена.</span><span class="sxs-lookup"><span data-stu-id="22bb0-124">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="22bb0-125">В разумных случаях убедитесь, что имена операций начинаются с глаголов, которые четко указывают на результат операции.</span><span class="sxs-lookup"><span data-stu-id="22bb0-125">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="22bb0-126">Пример:</span><span class="sxs-lookup"><span data-stu-id="22bb0-126">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="22bb0-127">Одним из случаев, которым заслуживает особое упоминание, является то, что операция принимает в качестве входных данных другую операцию и вызывает ее.</span><span class="sxs-lookup"><span data-stu-id="22bb0-127">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="22bb0-128">В таких случаях действие, выполняемое входной операцией, не ясно при определении внешней операции, что означает, что правая команда не будет немедленно очищена.</span><span class="sxs-lookup"><span data-stu-id="22bb0-128">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="22bb0-129">Рекомендуется использовать команду `Apply` , как в `ApplyIf` , `ApplyToEach` и `ApplyToFirst` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-129">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="22bb0-130">Другие глаголы также могут быть полезны в этом случае, как в `IterateThroughCartesianPower` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-130">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="22bb0-131">Команда</span><span class="sxs-lookup"><span data-stu-id="22bb0-131">Verb</span></span> | <span data-ttu-id="22bb0-132">Ожидаемый результат</span><span class="sxs-lookup"><span data-stu-id="22bb0-132">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="22bb0-133">Применить</span><span class="sxs-lookup"><span data-stu-id="22bb0-133">Apply</span></span> | <span data-ttu-id="22bb0-134">Операция, предоставленная в качестве входных данных, называется</span><span class="sxs-lookup"><span data-stu-id="22bb0-134">An operation provided as input is called</span></span> |
| <span data-ttu-id="22bb0-135">Assert</span><span class="sxs-lookup"><span data-stu-id="22bb0-135">Assert</span></span> | <span data-ttu-id="22bb0-136">Гипотеза о результате возможного измерения такта проверяется симулятором.</span><span class="sxs-lookup"><span data-stu-id="22bb0-136">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="22bb0-137">Оценка</span><span class="sxs-lookup"><span data-stu-id="22bb0-137">Estimate</span></span> | <span data-ttu-id="22bb0-138">Возвращается классический параметр, представляющий оценку, полученную от одного или нескольких измерений.</span><span class="sxs-lookup"><span data-stu-id="22bb0-138">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="22bb0-139">Measure</span><span class="sxs-lookup"><span data-stu-id="22bb0-139">Measure</span></span> | <span data-ttu-id="22bb0-140">Выполняется измерение такта, и результат возвращается пользователю.</span><span class="sxs-lookup"><span data-stu-id="22bb0-140">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="22bb0-141">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="22bb0-141">Prepare</span></span> | <span data-ttu-id="22bb0-142">Заданный регистр Кубитс инициализируется в определенном состоянии</span><span class="sxs-lookup"><span data-stu-id="22bb0-142">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="22bb0-143">Образец</span><span class="sxs-lookup"><span data-stu-id="22bb0-143">Sample</span></span> | <span data-ttu-id="22bb0-144">Классическое значение возвращается случайным образом из некоторого распределения</span><span class="sxs-lookup"><span data-stu-id="22bb0-144">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="22bb0-145">Для функций мы рекомендуем избегать использования глаголов в пользу общих существительных (см. Руководство по правильным существительным ниже) или прилагательные:</span><span class="sxs-lookup"><span data-stu-id="22bb0-145">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="22bb0-146">В частности, в большинстве случаев мы рекомендуем использовать последние партиЦиплес, где нужно указать, что имя функции строго соединено с действием или побочным эффектов в другом месте в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="22bb0-146">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="22bb0-147">Например,  `ControlledOnInt` использует форму части причастий команды "Control", чтобы указать, что функция выступает в качестве прилагательного для изменения своего аргумента.</span><span class="sxs-lookup"><span data-stu-id="22bb0-147">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="22bb0-148">Это имя имеет дополнительное преимущество в соответствии с семантикой встроенных `Controlled` функтор, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="22bb0-148">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="22bb0-149">Аналогичным образом можно использовать _существительные агентов_ для создания имен функций и определяемых пользователем типов из имен операций, как в случае имени `Encoder` определяемого пользователем типа, который строго связан с `Encode` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-149">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-150">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-150">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-151">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-151">We suggest:</span></span>

- <span data-ttu-id="22bb0-152">Используйте глаголы для имен операций.</span><span class="sxs-lookup"><span data-stu-id="22bb0-152">Use verbs for operation names.</span></span>
- <span data-ttu-id="22bb0-153">Для имен функций используйте существительные или прилагательные.</span><span class="sxs-lookup"><span data-stu-id="22bb0-153">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="22bb0-154">Используйте существительные для определяемых пользователем типов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-154">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="22bb0-155">Для всех вызываемых имен используйте `CamelCase` строгое предпочтение для `pascalCase` , `snake_case` или `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-155">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="22bb0-156">В частности, убедитесь, что вызываемые имена начинаются с прописных букв.</span><span class="sxs-lookup"><span data-stu-id="22bb0-156">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="22bb0-157">Для всех локальных переменных используйте `pascalCase` строгое предпочтение в `CamelCase` , `snake_case` или `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-157">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="22bb0-158">В частности, убедитесь, что локальные переменные начинаются с строчных букв.</span><span class="sxs-lookup"><span data-stu-id="22bb0-158">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="22bb0-159">Избегайте использования знаков подчеркивания `_` в именах функций и операций, где требуются дополнительные уровни иерархии, используйте пространства имен и псевдонимы пространств имен.</span><span class="sxs-lookup"><span data-stu-id="22bb0-159">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-160">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="22bb0-161">Имя</span><span class="sxs-lookup"><span data-stu-id="22bb0-161">Name</span></span> | <span data-ttu-id="22bb0-162">Описание</span><span class="sxs-lookup"><span data-stu-id="22bb0-162">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="22bb0-163">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-163">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="22bb0-164">Снимите флажок использовать глагол ("отражать"), чтобы указать результат операции.</span><span class="sxs-lookup"><span data-stu-id="22bb0-164">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="22bb0-165">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-165">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="22bb0-166">Использование фразы существительное предлагает функцию, а не операцию.</span><span class="sxs-lookup"><span data-stu-id="22bb0-166">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="22bb0-167">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-167">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="22bb0-168">Использование `snake_case` :::no-loc(Q#)::: нотации контравенес.</span><span class="sxs-lookup"><span data-stu-id="22bb0-168">Use of `snake_case` contravenes :::no-loc(Q#)::: notation.</span></span> |
| <span data-ttu-id="22bb0-169">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-169">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="22bb0-170">Использование символов подчеркивания Internal для обозначения операции контравенес :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="22bb0-170">Use of underscores internal to operation name contravenes :::no-loc(Q#)::: notation.</span></span> |
| <span data-ttu-id="22bb0-171">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-171">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="22bb0-172">Использование фразы с существительным предполагает, что функция возвращает операцию.</span><span class="sxs-lookup"><span data-stu-id="22bb0-172">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="22bb0-173">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-173">☑</span></span> | `function EqualityFact` | <span data-ttu-id="22bb0-174">Снимите флажок использовать существительное (факт), чтобы указать, что это функция, в то время как прилагательное.</span><span class="sxs-lookup"><span data-stu-id="22bb0-174">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="22bb0-175">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-175">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="22bb0-176">Использование глагола ("Get") предполагает, что это операция.</span><span class="sxs-lookup"><span data-stu-id="22bb0-176">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="22bb0-177">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-177">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="22bb0-178">Явное использование фразы с существительным означает результат вызова конструктора определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="22bb0-178">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="22bb0-179">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-179">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="22bb0-180">Использование глагола-фразы предполагает, что конструктор определяемого пользователем типа является операцией.</span><span class="sxs-lookup"><span data-stu-id="22bb0-180">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="22bb0-181">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-181">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="22bb0-182">Использование фразы существительное сообщает об использовании атрибута.</span><span class="sxs-lookup"><span data-stu-id="22bb0-182">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="entry-points"></a><span data-ttu-id="22bb0-183">Точки входа</span><span class="sxs-lookup"><span data-stu-id="22bb0-183">Entry Points</span></span>

<span data-ttu-id="22bb0-184">При определении точки входа в :::no-loc(Q#)::: программу :::no-loc(Q#)::: компилятор распознает [ `@EntryPoint()` атрибут](xref:Microsoft.Quantum.Core.EntryPoint) , а не требует, чтобы точки входа имели определенное имя (например `main` ,, `Main` или `__main__` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-184">When defining an entry point into a :::no-loc(Q#)::: program, the :::no-loc(Q#)::: compiler recognizes the [`@EntryPoint()` attribute](xref:Microsoft.Quantum.Core.EntryPoint) rather requiring that entry points have a particular name (e.g.: `main`, `Main`, or `__main__`).</span></span>
<span data-ttu-id="22bb0-185">То есть с точки зрения :::no-loc(Q#)::: разработчика точки входа являются обычными операциями с заметками `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-185">That is, from the perspective of a :::no-loc(Q#)::: developer, entry points are ordinary operations annotated with `@EntryPoint()`.</span></span>
<span data-ttu-id="22bb0-186">Более того, :::no-loc(Q#)::: точки входа могут быть точками входа для всего приложения (например, в :::no-loc(Q#)::: автономных исполняемых программах) или интерфейсом между :::no-loc(Q#)::: программой и основной программой для приложения (т. е. при использовании :::no-loc(Q#)::: с Python или .NET), в результате чего имя «main» может быть ошибочным при применении к :::no-loc(Q#)::: точке входа.</span><span class="sxs-lookup"><span data-stu-id="22bb0-186">Moreover, :::no-loc(Q#)::: entry points may be entry points for an entire application (for example, in :::no-loc(Q#)::: standalone executable programs), or may be an interface between a :::no-loc(Q#)::: program and the host program for an application (i.e.: when using :::no-loc(Q#)::: with Python or .NET), such that the name "main" could be misleading when applied to a :::no-loc(Q#)::: entry point.</span></span>

<span data-ttu-id="22bb0-187">Рекомендуется использовать именование точек входа для отражения использования `@EntryPoint()` атрибута с помощью общих рекомендаций для операций именования, перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="22bb0-187">We suggest using naming entry points to reflect the use of the `@EntryPoint()` attribute by using the general advice for naming operations listed above.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="22bb0-188">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-188">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-189">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-189">We suggest:</span></span>

- <span data-ttu-id="22bb0-190">Не назовите операции точки входа как "Main".</span><span class="sxs-lookup"><span data-stu-id="22bb0-190">Do not name entry point operations as "main."</span></span>
- <span data-ttu-id="22bb0-191">Назовите операции точки входа как обычные операции.</span><span class="sxs-lookup"><span data-stu-id="22bb0-191">Name entry point operations as ordinary operations.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-192">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-192">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="22bb0-193">Имя</span><span class="sxs-lookup"><span data-stu-id="22bb0-193">Name</span></span> | <span data-ttu-id="22bb0-194">Описание</span><span class="sxs-lookup"><span data-stu-id="22bb0-194">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="22bb0-195">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-195">☑</span></span> | `@EntryPoint() operation RunSimulation` | <span data-ttu-id="22bb0-196">Явно сообщает назначение точки входа через имя операции.</span><span class="sxs-lookup"><span data-stu-id="22bb0-196">Clearly communicates purpose of entry point through operation name.</span></span> |
| <span data-ttu-id="22bb0-197">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-197">☒</span></span> | <s>`@EntryPoint() operation Main`</s> | <span data-ttu-id="22bb0-198">Использование объекта `Main` не позволяет явно передавать цель точки входа и является избыточным `@EntryPoint()` атрибутом.</span><span class="sxs-lookup"><span data-stu-id="22bb0-198">Use of `Main` doesn't clearly communicate purpose of entry point, and is redundant with `@EntryPoint()` attribute.</span></span> |

<span data-ttu-id="22bb0-199">\*\*_</span><span class="sxs-lookup"><span data-stu-id="22bb0-199">\*\*_</span></span>

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="22bb0-200">Сокращенные и сокращенные обозначения</span><span class="sxs-lookup"><span data-stu-id="22bb0-200">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="22bb0-201">Приведенный выше Совет не отменяется, существует множество форм сокращений, которые являются распространенным и распространенным использованием в тактовых вычислениях.</span><span class="sxs-lookup"><span data-stu-id="22bb0-201">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="22bb0-202">Мы рекомендуем использовать существующую и распространенную краткую форму, в которой он существует, особенно для операций, которые являются встроенными для работы целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="22bb0-202">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="22bb0-203">Например, мы выбираем имя, а не `X` `ApplyX` `Rz` `RotateAboutZ` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-203">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="22bb0-204">При использовании такой сокращенной формы имена операций должны быть все прописными (например: `MAJ` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-204">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="22bb0-205">При применении этого соглашения необходимо соблюдать осторожность в случае часто используемых акронимов и сокращений, например "Кфт" для "преобразования тактов в тактовой области".</span><span class="sxs-lookup"><span data-stu-id="22bb0-205">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="22bb0-206">Мы рекомендуем использовать следующие общие соглашения .NET для использования акронимов и сокращений в полных именах, которые предписывает:</span><span class="sxs-lookup"><span data-stu-id="22bb0-206">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="22bb0-207">двузначные акронимы и сокращений именуются в верхнем регистре (например, `BE` для «Big-endian»),</span><span class="sxs-lookup"><span data-stu-id="22bb0-207">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="22bb0-208">все более длинные акронимы и сокращений именуются в `CamelCase` (например, `Qft` для "преобразования в тактовую Фурье").</span><span class="sxs-lookup"><span data-stu-id="22bb0-208">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="22bb0-209">Таким образом, операция, реализующая Кфт, может быть либо вызвана `QFT` как краткая, либо записана как `ApplyQft` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-209">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="22bb0-210">Для наиболее часто используемых операций и функций может быть желательно предоставить сокращенное имя в качестве _псевдонима_ для более длинной формы:</span><span class="sxs-lookup"><span data-stu-id="22bb0-210">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[<span data-ttu-id="22bb0-211">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-211">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-212">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-212">We suggest:</span></span>

- <span data-ttu-id="22bb0-213">При необходимости рекомендуется использовать распространенные и распространенные сокращенные имена.</span><span class="sxs-lookup"><span data-stu-id="22bb0-213">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="22bb0-214">Для сокращения используйте прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="22bb0-214">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="22bb0-215">Используйте прописные буквы для коротких (двух букв) аббревиатур и сокращений.</span><span class="sxs-lookup"><span data-stu-id="22bb0-215">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="22bb0-216">Используйте `CamelCase` более длинные (три и более буквы) акронимы и сокращений.</span><span class="sxs-lookup"><span data-stu-id="22bb0-216">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-217">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-217">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="22bb0-218">Имя</span><span class="sxs-lookup"><span data-stu-id="22bb0-218">Name</span></span> | <span data-ttu-id="22bb0-219">Описание</span><span class="sxs-lookup"><span data-stu-id="22bb0-219">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="22bb0-220">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-220">☑</span></span> | `X` | <span data-ttu-id="22bb0-221">Хорошо понятная Краткая форма "применение преобразования $X $"</span><span class="sxs-lookup"><span data-stu-id="22bb0-221">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="22bb0-222">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-222">☑</span></span> | `CNOT` | <span data-ttu-id="22bb0-223">Хорошо понятная Краткая форма для «контролируемых»</span><span class="sxs-lookup"><span data-stu-id="22bb0-223">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="22bb0-224">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-224">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="22bb0-225">Сокращенная форма не должна находиться в `CamelCase` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-225">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="22bb0-226">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-226">☑</span></span> | `ApplyQft` | <span data-ttu-id="22bb0-227">Общий начальный вид "Кфт" отображается как часть имени длинной формы.</span><span class="sxs-lookup"><span data-stu-id="22bb0-227">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="22bb0-228">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-228">☑</span></span> | `QFT` | <span data-ttu-id="22bb0-229">Общий начальный вид "Кфт" отображается как часть сокращенного имени.</span><span class="sxs-lookup"><span data-stu-id="22bb0-229">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



_*_


### <a name="proper-nouns-in-names"></a><span data-ttu-id="22bb0-230">Собственные существительные в именах</span><span class="sxs-lookup"><span data-stu-id="22bb0-230">Proper Nouns in Names</span></span> ###

<span data-ttu-id="22bb0-231">Хотя в физике мы часто называете вещи, когда первый пользователь публикует их, большинство фисиЦистс не знакомы с именами всех участников и журналами.</span><span class="sxs-lookup"><span data-stu-id="22bb0-231">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="22bb0-232">Чрезмерная постановка в соглашениях об именовании от физикы может привести к значительному барьеру в записи, так как пользователи из других фоновых рисунков должны изучить большое количество непрозрачных имен, чтобы использовать общие операции и концепции.</span><span class="sxs-lookup"><span data-stu-id="22bb0-232">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="22bb0-233">Таким образом, рекомендуется, чтобы при разумных принципах обычные существительные, описывающие концепцию, были приняты строгими для правильного существительных, описывающих историю публикации концепции.</span><span class="sxs-lookup"><span data-stu-id="22bb0-233">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="22bb0-234">В качестве конкретного примера, управляемые с помощью одной и той же операции перестановки и управления удвоением часто называются операциями «Фредкин» и «Тоффоли» в учебных литературах, но в основном они определены :::no-loc(Q#)::: как `CSWAP` и `CCNOT` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-234">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in :::no-loc(Q#)::: primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="22bb0-235">В обоих случаях комментарии к документации по API предоставляют имена синонимов на основе правильных существительных, а также все соответствующие ссылки.</span><span class="sxs-lookup"><span data-stu-id="22bb0-235">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="22bb0-236">Этот приоритет особенно важен в тех случаях, когда необходимо всегда использовать собственные существительные — :::no-loc(Q#)::: в соответствии с традицией, установленной многими классическими языками, и ссылается на `Bool` типы в ссылке на логическую логику, которая, в свою очередь, имеет имя, соблюдающая bool.</span><span class="sxs-lookup"><span data-stu-id="22bb0-236">This preference is especially important given that some usage of proper nouns will always be necessary — :::no-loc(Q#)::: follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="22bb0-237">Несколько концепций такта аналогичным образом именуются, включая `Pauli` тип, встроенный в :::no-loc(Q#)::: язык.</span><span class="sxs-lookup"><span data-stu-id="22bb0-237">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the :::no-loc(Q#)::: language.</span></span>
<span data-ttu-id="22bb0-238">Свести к минимуму использование правильных существительных, если такое использование не является обязательным, мы уменьшаем влияние того, что их не удается избежать.</span><span class="sxs-lookup"><span data-stu-id="22bb0-238">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-239">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-239">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="22bb0-240">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-240">We suggest:</span></span>

- <span data-ttu-id="22bb0-241">Избегайте использования в именах правильных существительных.</span><span class="sxs-lookup"><span data-stu-id="22bb0-241">Avoid the use of proper nouns in names.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-242">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-242">Examples</span></span>](#tab/examples)

_*_

### <a name="type-conversions"></a><span data-ttu-id="22bb0-243">Преобразования типов</span><span class="sxs-lookup"><span data-stu-id="22bb0-243">Type Conversions</span></span> ###

<span data-ttu-id="22bb0-244">Поскольку :::no-loc(Q#)::: является строго и статически типизированным языком, значение одного типа может использоваться только как значение другого типа с помощью явного вызова функции преобразования типа.</span><span class="sxs-lookup"><span data-stu-id="22bb0-244">Since :::no-loc(Q#)::: is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="22bb0-245">Это отличается от языков, позволяющих неявным образом изменять типы значений (например, повышение типа) или путем приведения.</span><span class="sxs-lookup"><span data-stu-id="22bb0-245">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="22bb0-246">В результате функции преобразования типов играют важную роль при :::no-loc(Q#)::: разработке библиотеки и составляют одно из наиболее часто встречающихся решений по именованию.</span><span class="sxs-lookup"><span data-stu-id="22bb0-246">As a result, type conversion functions play an important role in :::no-loc(Q#)::: library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="22bb0-247">Однако обратите внимание, что поскольку преобразования типов всегда _детерминированы_ , они могут быть написаны как функции и, таким образом, находиться на приведенный выше Совет.</span><span class="sxs-lookup"><span data-stu-id="22bb0-247">We note, however, that since type conversions are always _deterministic_ , they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="22bb0-248">В частности, мы советуем, что функции преобразования типов никогда не должны называться как глаголы (например, `ConvertToX` ) или модификаторовные фразы ( `ToX` ), но они должны называться как прилагательные фразы, указывающие исходный и целевой типы ( `XAsY` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-248">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="22bb0-249">При перечислении типов массивов в именах функций преобразования типов рекомендуется использовать краткую форму `Arr` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-249">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="22bb0-250">При запрете исключительных обстоятельств рекомендуется, чтобы все функции преобразования типов были именованы с помощью, `As` чтобы их можно было быстро определить.</span><span class="sxs-lookup"><span data-stu-id="22bb0-250">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-251">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-251">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-252">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-252">We suggest:</span></span>

- <span data-ttu-id="22bb0-253">Если функция преобразует значение типа `X` в значение типа `Y` , используйте либо имя, `AsY` либо `XAsY` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-253">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-254">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-254">Examples</span></span>](#tab/examples)

| &nbsp;   | <span data-ttu-id="22bb0-255">Имя</span><span class="sxs-lookup"><span data-stu-id="22bb0-255">Name</span></span> | <span data-ttu-id="22bb0-256">Описание</span><span class="sxs-lookup"><span data-stu-id="22bb0-256">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="22bb0-257">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-257">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="22bb0-258">В качестве отстановки "до" задается Командная фраза, указывающая на операцию, а не на функцию.</span><span class="sxs-lookup"><span data-stu-id="22bb0-258">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="22bb0-259">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-259">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="22bb0-260">Тип входных данных не является понятным по имени функции.</span><span class="sxs-lookup"><span data-stu-id="22bb0-260">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="22bb0-261">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-261">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="22bb0-262">Входные и выходные типы отображаются в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="22bb0-262">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="22bb0-263">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-263">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="22bb0-264">Типы входных и выходных данных являются четкими.</span><span class="sxs-lookup"><span data-stu-id="22bb0-264">Both the input types and output types are clear.</span></span> |

_*_

### <a name="private-or-internal-names"></a><span data-ttu-id="22bb0-265">Частные или внутренние имена</span><span class="sxs-lookup"><span data-stu-id="22bb0-265">Private or Internal Names</span></span> ###

<span data-ttu-id="22bb0-266">Во многих случаях имя предназначено исключительно для внутреннего использования в библиотеке или проекте и не является гарантированной частью API, предоставляемой библиотекой.</span><span class="sxs-lookup"><span data-stu-id="22bb0-266">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="22bb0-267">Полезно четко указать, что это происходит при именовании функций и операций, так что случайные зависимости от внутреннего кода становятся очевидными.</span><span class="sxs-lookup"><span data-stu-id="22bb0-267">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="22bb0-268">Если операция или функция не предназначена для непосредственного использования, а должна использоваться соответствующим вызываемым методом, который действует частичным приложением, рассмотрите возможность использования имени, начинающегося с `internal` ключевого слова, для вызываемого частично применяемого метода.</span><span class="sxs-lookup"><span data-stu-id="22bb0-268">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with the `internal` keyword for the callable that is partially applied.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-269">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-269">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-270">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-270">We suggest:</span></span>

- <span data-ttu-id="22bb0-271">Если функция, операция или определяемый пользователем тип не являются частью общедоступного API для :::no-loc(Q#)::: библиотеки или программы, убедитесь, что она помечена как внутренняя, поместив `internal` ключевое слово перед `function` `operation` `newtype` объявлением, или.</span><span class="sxs-lookup"><span data-stu-id="22bb0-271">When a function, operation, or user-defined type is not a part of the public API for a :::no-loc(Q#)::: library or program, ensure that it is marked as internal by placing the `internal` keyword before the `function`, `operation`, or `newtype` declaration.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-272">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-272">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="22bb0-273">Имя</span><span class="sxs-lookup"><span data-stu-id="22bb0-273">Name</span></span> | <span data-ttu-id="22bb0-274">Описание</span><span class="sxs-lookup"><span data-stu-id="22bb0-274">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="22bb0-275">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-275">☒</span></span> | <s>`operation _ApplyDecomposedOperation`</s> | <span data-ttu-id="22bb0-276">Не используйте символ подчеркивания `_` , чтобы указать, что эта операция предназначена только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="22bb0-276">Do not use an underscore `_` to indicate that this operation is for internal use only.</span></span> |
| <span data-ttu-id="22bb0-277">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-277">☑</span></span> | `internal operation ApplyDecomposedOperation` | <span data-ttu-id="22bb0-278">`internal`Ключевое слово в начале ясно указывает, что эта операция предназначена только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="22bb0-278">The `internal` keyword at the beginning clearly indicates that this operation is for internal use only.</span></span> |

_*_
### <a name="variants"></a><span data-ttu-id="22bb0-279">Варианты</span><span class="sxs-lookup"><span data-stu-id="22bb0-279">Variants</span></span> ###

<span data-ttu-id="22bb0-280">Несмотря на то, что это ограничение может не сохраняться в будущих версиях :::no-loc(Q#)::: , оно, в своюмся случае, будет представлять собой группы связанных операций или функций, которые различаются операторов их входными данными или конкретными типами их аргументов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-280">Though this limitation may not persist in future versions of :::no-loc(Q#):::, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="22bb0-281">Эти группы можно отличать с помощью одного и того же корневого имени, за которым следует одна или две буквы, указывающие на вариант.</span><span class="sxs-lookup"><span data-stu-id="22bb0-281">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="22bb0-282">Суффикс</span><span class="sxs-lookup"><span data-stu-id="22bb0-282">Suffix</span></span> | <span data-ttu-id="22bb0-283">Значение</span><span class="sxs-lookup"><span data-stu-id="22bb0-283">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="22bb0-284">Ожидается ввод для поддержки `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="22bb0-284">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="22bb0-285">Ожидается ввод для поддержки `Controlled`</span><span class="sxs-lookup"><span data-stu-id="22bb0-285">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="22bb0-286">Ожидается ввод для поддержки `Controlled` и `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="22bb0-286">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="22bb0-287">Входные или входные данные имеют тип `Int`</span><span class="sxs-lookup"><span data-stu-id="22bb0-287">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="22bb0-288">Входные или входные данные имеют тип `Double`</span><span class="sxs-lookup"><span data-stu-id="22bb0-288">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="22bb0-289">Входные или входные данные имеют тип `BigInt`</span><span class="sxs-lookup"><span data-stu-id="22bb0-289">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidance"></a>[<span data-ttu-id="22bb0-290">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-290">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-291">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-291">We suggest:</span></span>

- <span data-ttu-id="22bb0-292">Если функция или операция не связаны с аналогичными функциями или операциями по типам и функтор поддерживают свои входные данные, не используйте суффикс.</span><span class="sxs-lookup"><span data-stu-id="22bb0-292">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="22bb0-293">Если функция или операция связана с любыми аналогичными функциями или операциями типов и функтор поддержки своих входных данных, используйте суффиксы, как показано в таблице выше, чтобы различать варианты.</span><span class="sxs-lookup"><span data-stu-id="22bb0-293">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-294">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-294">Examples</span></span>](#tab/examples)

_*_

### <a name="arguments-and-variables"></a><span data-ttu-id="22bb0-295">Аргументы и переменные</span><span class="sxs-lookup"><span data-stu-id="22bb0-295">Arguments and Variables</span></span> ###

<span data-ttu-id="22bb0-296">Ключевой целью :::no-loc(Q#)::: кода для функции или операции является простое чтение и понимание.</span><span class="sxs-lookup"><span data-stu-id="22bb0-296">A key goal of the :::no-loc(Q#)::: code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="22bb0-297">Аналогичным образом, имена входов и аргументов типа должны сообщать, как функция или аргумент будут использоваться по мере того, как они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="22bb0-297">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="22bb0-298">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-298">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-299">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-299">We suggest:</span></span>

- <span data-ttu-id="22bb0-300">Для всех переменных и входных имен используйте `pascalCase` строгое предпочтение в `CamelCase` , `snake_case` или `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-300">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="22bb0-301">Входные имена должны быть описательными; по возможности избегайте по одному или двум именам букв.</span><span class="sxs-lookup"><span data-stu-id="22bb0-301">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="22bb0-302">Операции и функции, принимающие ровно один аргумент типа, должны отметить этот аргумент типа, `T` если его роль очевидна.</span><span class="sxs-lookup"><span data-stu-id="22bb0-302">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="22bb0-303">Если функция или операция принимает несколько аргументов типа или если роль одного аргумента типа не очевидна, рассмотрите возможность использования короткого слова с прописной буквой, которое предшествует `T` (например, `TOutput` ) для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="22bb0-303">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="22bb0-304">Не включайте имена типов в имена аргументов и переменных. Эти сведения могут и должны предоставляться средой разработки.</span><span class="sxs-lookup"><span data-stu-id="22bb0-304">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="22bb0-305">Запишите скалярные типы по их литеральным именам ( `flagQubit` ) и типам массивов во множественном числе ( `measResults` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-305">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="22bb0-306">Для массивов Кубитс в частности, рассмотрите такие типы, в `Register` которых имя ссылается на последовательность Кубитс, тесно связанных каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="22bb0-306">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="22bb0-307">Переменные, используемые в качестве индексов в массивах, должны начинаться с `idx` и должны быть в единственном числе, например: `things[idxThing]` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-307">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="22bb0-308">В частности, настоятельно рекомендуется избегать использования однобуквенных имен переменных в качестве индексов; рекомендуется использовать `idx` как минимум.</span><span class="sxs-lookup"><span data-stu-id="22bb0-308">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="22bb0-309">Переменные, используемые для хранения длин массивов, должны начинаться с `n` и должны быть в множественном числе, например: `nThings` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-309">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-310">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-310">Examples</span></span>](#tab/examples)

_*_

### <a name="user-defined-type-named-items"></a><span data-ttu-id="22bb0-311">User-Defined именованные элементы типа</span><span class="sxs-lookup"><span data-stu-id="22bb0-311">User-Defined Type Named Items</span></span> ###

<span data-ttu-id="22bb0-312">Именованные элементы в определяемых пользователем типах должны называться как `CamelCase` , даже при вводе в конструкторы определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="22bb0-312">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="22bb0-313">Это помогает в четком разделении именованных элементов со ссылок на переменные в локальной области при использовании представления метода доступа (например, `callable::Apply` ) или нотации копирования и обновления ( `set arr w/= Data <- newData` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-313">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-314">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-314">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-315">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-315">We suggest:</span></span>

- <span data-ttu-id="22bb0-316">Именованные элементы в конструкторах определяемых пользователем типов должны называться как `CamelCase` ; то есть должны начинаться с прописной буквы.</span><span class="sxs-lookup"><span data-stu-id="22bb0-316">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="22bb0-317">Именованные элементы, которые разрешаются в операции, должны называться этапами глагола.</span><span class="sxs-lookup"><span data-stu-id="22bb0-317">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="22bb0-318">Именованные элементы, которые не разрешаются в операции, должны называться как субстантивные словосочетания.</span><span class="sxs-lookup"><span data-stu-id="22bb0-318">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="22bb0-319">Для определяемых пользователем типов, которые обносят операции, необходимо определить один именованный элемент `Apply` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-319">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-320">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-320">Examples</span></span>](#tab/examples)

| &nbsp;  | <span data-ttu-id="22bb0-321">Фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="22bb0-321">Snippet</span></span> | <span data-ttu-id="22bb0-322">Описание</span><span class="sxs-lookup"><span data-stu-id="22bb0-322">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="22bb0-323">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-323">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="22bb0-324">Имя `Apply` является `CamelCase` фразой-командой, предлагающей, что именованный элемент является операцией.</span><span class="sxs-lookup"><span data-stu-id="22bb0-324">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="22bb0-325">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-325">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="22bb0-326">Именованные элементы должны начинаться с первой прописной буквы.</span><span class="sxs-lookup"><span data-stu-id="22bb0-326">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="22bb0-327">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-327">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="22bb0-328">Именованные элементы, которые разрешаются в функции, должны называться как субстантивные словосочетания, а не как фразы глагола.</span><span class="sxs-lookup"><span data-stu-id="22bb0-328">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

_*_

## <a name="input-conventions"></a><span data-ttu-id="22bb0-329">Соглашения о входе</span><span class="sxs-lookup"><span data-stu-id="22bb0-329">Input Conventions</span></span> ##

<span data-ttu-id="22bb0-330">Когда разработчик обращается к операции или функции, различные входные данные этой операции или функции должны быть указаны в определенном порядке, увеличивая при этом функциональную нагрузку, которую разработчик может использовать для создания библиотеки.</span><span class="sxs-lookup"><span data-stu-id="22bb0-330">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="22bb0-331">В частности, задача по запоминанию порядка входных данных часто является отправной задачей: программированием реализации алгоритма такта.</span><span class="sxs-lookup"><span data-stu-id="22bb0-331">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="22bb0-332">Хотя широкая поддержка интегрированной среды разработки может снизить это до большого экстента, хорошая разработка и соблюдение общих соглашений также может помочь минимизировать неудачную загрузку, наложенную API.</span><span class="sxs-lookup"><span data-stu-id="22bb0-332">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="22bb0-333">Там, где это возможно, может быть полезно уменьшить количество входных данных, ожидаемых операцией или функцией, чтобы роль каждого входа была более очевидна для разработчиков, обращающихся к этой операции или функции, а также для разработчиков, считывающих этот код позже.</span><span class="sxs-lookup"><span data-stu-id="22bb0-333">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="22bb0-334">Особенно если невозможно или разумно уменьшить число аргументов для операции или функции, важно иметь единообразный порядок, позволяющий свести к сведению, что пользователь сталкивается с прогнозированием порядка входных данных.</span><span class="sxs-lookup"><span data-stu-id="22bb0-334">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="22bb0-335">Мы рекомендуем использовать соглашения о порядке ввода, которые во многом наследуют от мышления частичного приложения как обобщение карринг f (x, y) ≡ f (x) (y).</span><span class="sxs-lookup"><span data-stu-id="22bb0-335">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="22bb0-336">Таким образом, частичное применение первых аргументов должно привести к вызову, который будет полезен при любом разумном использовании.</span><span class="sxs-lookup"><span data-stu-id="22bb0-336">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="22bb0-337">Следуя этому принципу, рассмотрите возможность использования следующего порядка аргументов:</span><span class="sxs-lookup"><span data-stu-id="22bb0-337">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="22bb0-338">Классические не вызываемые аргументы, такие как углы, векторы степеней и т. д.</span><span class="sxs-lookup"><span data-stu-id="22bb0-338">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="22bb0-339">Вызываемые аргументы (функции и аргументы).</span><span class="sxs-lookup"><span data-stu-id="22bb0-339">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="22bb0-340">Если обе функции и операции выполняются в качестве аргументов, попробуйте разместить операции после функций.</span><span class="sxs-lookup"><span data-stu-id="22bb0-340">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="22bb0-341">Коллекции, обрабатываемые вызываемыми аргументами аналогично методу `Map` , `Iter` , `Enumerate` и `Fold` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-341">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="22bb0-342">Аргументы кубит, используемые в качестве элементов управления.</span><span class="sxs-lookup"><span data-stu-id="22bb0-342">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="22bb0-343">Аргументы кубит, используемые в качестве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-343">Qubit arguments used as targets.</span></span>

<span data-ttu-id="22bb0-344">Рассмотрим операцию `ApplyPhaseEstimationIteration` для использования в оценке этапа, которая принимает угол и Oracle, передает угол `Rz` , измененный массивом различных факторов масштабирования, а затем управляет приложениями Oracle.</span><span class="sxs-lookup"><span data-stu-id="22bb0-344">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="22bb0-345">Мы будем упорядочивать входные данные `ApplyPhaseEstimationIteration` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="22bb0-345">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

```qsharp
operation ApplyPhaseEstimationIteration(
    angle : Double,
    callable : (Qubit => () is Ctl),
    scaleFactors : Double[],
    controlQubit : Qubit,
    targetQubits : Qubit[]
)
: Unit
...
```
<span data-ttu-id="22bb0-346">В качестве особого случая минимизации неожиданности некоторые функции и операции воспроизводят поведение встроенных операторов `Adjoint` и `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="22bb0-346">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="22bb0-347">Например, `ControlledOnInt<'T>` имеет тип `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` , который `ControlledOnInt<Qubit[]>(5, _)` действует как `Controlled` функтор, но в условии, что регистр элемента управления представляет состояние $ \кет {5} = \кет {101} $.</span><span class="sxs-lookup"><span data-stu-id="22bb0-347">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="22bb0-348">Таким образом, разработчику требуется, чтобы входные данные `ControlledOnInt` были преобразованы последними, а Результирующая операция принимает в качестве входных данных `(Qubit[], 'T)` ---том же порядке, в котором следуют выходные данные `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="22bb0-348">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-349">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-349">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-350">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-350">We suggest:</span></span>

- <span data-ttu-id="22bb0-351">Используйте порядок ввода в соответствии с использованием частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="22bb0-351">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="22bb0-352">Используйте порядок ввода в соответствии со встроенными операторов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-352">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="22bb0-353">Разместите все классические входные данные перед любыми входными тактовыми тактами.</span><span class="sxs-lookup"><span data-stu-id="22bb0-353">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-354">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-354">Examples</span></span>](#tab/examples)

_*_

## <a name="documentation-conventions"></a><span data-ttu-id="22bb0-355">Обозначения в документации</span><span class="sxs-lookup"><span data-stu-id="22bb0-355">Documentation Conventions</span></span> ##

<span data-ttu-id="22bb0-356">:::no-loc(Q#):::Язык позволяет прикреплять документацию к операциям, функциям и определяемым пользователем типам с помощью специально отформатированных комментариев к документации.</span><span class="sxs-lookup"><span data-stu-id="22bb0-356">The :::no-loc(Q#)::: language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="22bb0-357">В соответствии с тройными косыми чертами ( `///` ) эти комментарии документации представляют собой небольшие [DocFX документы Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) , которые можно использовать для описания назначения каждой операции, функции и определяемого пользователем типа, возвращаемых входов и т. д.</span><span class="sxs-lookup"><span data-stu-id="22bb0-357">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="22bb0-358">Компилятор, поставляемый с пакетом разработки тактов, извлекает эти комментарии и использует их для помощи в документации по наборам типов, похожим на эту https://docs.microsoft.com/quantum .</span><span class="sxs-lookup"><span data-stu-id="22bb0-358">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="22bb0-359">Аналогичным образом, языковой сервер, поставляемый с пакетом разработки тактовой передачи, использует эти комментарии для предоставления помощи пользователям при наведении указателя мыши на символы в :::no-loc(Q#)::: коде.</span><span class="sxs-lookup"><span data-stu-id="22bb0-359">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their :::no-loc(Q#)::: code.</span></span>
<span data-ttu-id="22bb0-360">Использование комментариев к документации может помочь пользователям лучше понять код, предоставляя полезную ссылку для получения подробных сведений, которые не просто выражаются с помощью других соглашений в этом документе.</span><span class="sxs-lookup"><span data-stu-id="22bb0-360">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

> [!div class="nextstepaction"]
> <span data-ttu-id="22bb0-361">[Справочник по синтаксису комментариев документации](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span><span class="sxs-lookup"><span data-stu-id="22bb0-361">[Documentation comment syntax reference](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span></span>

<span data-ttu-id="22bb0-362">Чтобы эффективно использовать эту функцию для пользователей, рекомендуется учитывать некоторые моменты при написании комментариев к документации.</span><span class="sxs-lookup"><span data-stu-id="22bb0-362">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-363">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-363">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="22bb0-364">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-364">We suggest:</span></span>

- <span data-ttu-id="22bb0-365">Каждая открытая функция, операция и определяемый пользователем тип должны непосредственно предшествовать комментарию документации.</span><span class="sxs-lookup"><span data-stu-id="22bb0-365">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="22bb0-366">Каждый комментарий к документации должен содержать как минимум следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="22bb0-366">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="22bb0-367">Сводка</span><span class="sxs-lookup"><span data-stu-id="22bb0-367">Summary</span></span>
    - <span data-ttu-id="22bb0-368">Входные данные</span><span class="sxs-lookup"><span data-stu-id="22bb0-368">Input</span></span>
    - <span data-ttu-id="22bb0-369">Выходные данные (если применимо)</span><span class="sxs-lookup"><span data-stu-id="22bb0-369">Output (if applicable)</span></span>
- <span data-ttu-id="22bb0-370">Убедитесь, что все сводки имеют два предложения или меньше.</span><span class="sxs-lookup"><span data-stu-id="22bb0-370">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="22bb0-371">Если требуется больше места, укажите раздел, `# Description` приведенный сразу за `# Summary` полными сведениями.</span><span class="sxs-lookup"><span data-stu-id="22bb0-371">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="22bb0-372">В разумных случаях не включайте математические вычисления в сводки, так как не все клиенты поддерживают да нотацию в сводках.</span><span class="sxs-lookup"><span data-stu-id="22bb0-372">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="22bb0-373">Обратите внимание, что при написании документов prose (например, да или Markdown) может быть предпочтительнее использовать более длинные строки.</span><span class="sxs-lookup"><span data-stu-id="22bb0-373">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="22bb0-374">Укажите все соответствующие математические выражения в `# Description` разделе.</span><span class="sxs-lookup"><span data-stu-id="22bb0-374">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="22bb0-375">При описании входных данных не следует повторять типы всех входных данных, так как они могут выводиться компилятором и угрожать несогласованность.</span><span class="sxs-lookup"><span data-stu-id="22bb0-375">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="22bb0-376">Укажите нужные примеры, каждый в отдельном `# Example` разделе.</span><span class="sxs-lookup"><span data-stu-id="22bb0-376">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="22bb0-377">Кратко опишите каждый пример перед выводом кода.</span><span class="sxs-lookup"><span data-stu-id="22bb0-377">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="22bb0-378">В разделе представлены все соответствующие академические публикации (например, документы, материалы, записи в блоге и альтернативные реализации) `# References` раздела в виде маркированного списка ссылок.</span><span class="sxs-lookup"><span data-stu-id="22bb0-378">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="22bb0-379">Убедитесь, что, где это возможно, все ссылки ссылок относятся к постоянным и неизменяемым идентификаторам (Доис или номера Арксив версий).</span><span class="sxs-lookup"><span data-stu-id="22bb0-379">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="22bb0-380">Если операция или функция связана с другими операциями или функциями с помощью функтор Variant, перечислите другие варианты в виде маркеров в `# See Also` разделе.</span><span class="sxs-lookup"><span data-stu-id="22bb0-380">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="22bb0-381">Оставьте пустую строку комментария между разделами уровня 1 ( `/// #` ), но не оставляйте пустых строк между разделами уровня 2 ( `/// ##` ).</span><span class="sxs-lookup"><span data-stu-id="22bb0-381">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-382">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-382">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="22bb0-383">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-383">☑</span></span> ####

```
/// # Summary
/// Applies a rotation about the X-axis by a given angle.
///
///
/// # Description
/// This operation rotates a single qubit by the unitary operation
/// \begin{align}
///     R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2}.
/// \end{align}
///
/// # Input
/// ## theta
/// Angle about which the qubit is to be rotated.
/// ## qubit
/// Qubit to which the gate should be applied.
///
/// # Remarks
/// Equivalent to:
/// ```qsharp
/// R(PauliX, theta, qubit);
/// ```
///
/// # See Also
/// - Ry
/// - Rz
operation Rx(theta : Double, qubit : Qubit) : Unit
is Adj + Ctl {
    body (...) { R(PauliX, theta, qubit); }
    adjoint (...) { R(PauliX, -theta, qubit); }
}
```

_*_

## <a name="formatting-conventions"></a><span data-ttu-id="22bb0-384">Соглашения о форматировании</span><span class="sxs-lookup"><span data-stu-id="22bb0-384">Formatting Conventions</span></span> ##

<span data-ttu-id="22bb0-385">Помимо описанных выше предложений, рекомендуется сделать код максимально удобочитаемым, чтобы использовать единообразные правила форматирования.</span><span class="sxs-lookup"><span data-stu-id="22bb0-385">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="22bb0-386">Такие правила форматирования по сути, как правило, являются несколько произвольными и хорошо эстетичность.</span><span class="sxs-lookup"><span data-stu-id="22bb0-386">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="22bb0-387">Тем не менее рекомендуется поддерживать единообразный набор соглашений о форматировании в группе участников совместной работы, особенно для крупных :::no-loc(Q#)::: проектов, таких как сам пакет разработки такта.</span><span class="sxs-lookup"><span data-stu-id="22bb0-387">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large :::no-loc(Q#)::: projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="22bb0-388">Эти правила могут быть автоматически применены с помощью средства форматирования, интегрированного с :::no-loc(Q#)::: компилятором.</span><span class="sxs-lookup"><span data-stu-id="22bb0-388">These rules can be automatically applied by using the formatting tool integrated with the :::no-loc(Q#)::: compiler.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="22bb0-389">Руководство</span><span class="sxs-lookup"><span data-stu-id="22bb0-389">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="22bb0-390">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="22bb0-390">We suggest:</span></span>

- <span data-ttu-id="22bb0-391">Для переносимости используйте четыре пробела вместо вкладок.</span><span class="sxs-lookup"><span data-stu-id="22bb0-391">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="22bb0-392">Например, в VS Code:</span><span class="sxs-lookup"><span data-stu-id="22bb0-392">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="22bb0-393">Строка переносится в 79 символов, где это оправданно.</span><span class="sxs-lookup"><span data-stu-id="22bb0-393">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="22bb0-394">Используйте пробелы вокруг бинарных операторов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-394">Use spaces around binary operators.</span></span>
- <span data-ttu-id="22bb0-395">Используйте пробелы с обеих сторон двоеточий, используемых для заметок типов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-395">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="22bb0-396">Используйте один пробел после запятых, используемых в массивах и литералах кортежа (например, в входных данных для функций и операций).</span><span class="sxs-lookup"><span data-stu-id="22bb0-396">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="22bb0-397">Не используйте пробелы после имени функции, операции или определяемого пользователем типа или после `@` объявлений атрибута in.</span><span class="sxs-lookup"><span data-stu-id="22bb0-397">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="22bb0-398">Каждое объявление атрибута должно располагаться в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="22bb0-398">Each attribute declaration should be on its own line.</span></span>

# <a name="examples"></a>[<span data-ttu-id="22bb0-399">Примеры</span><span class="sxs-lookup"><span data-stu-id="22bb0-399">Examples</span></span>](#tab/examples)

| &nbsp; | <span data-ttu-id="22bb0-400">Фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="22bb0-400">Snippet</span></span> | <span data-ttu-id="22bb0-401">Описание</span><span class="sxs-lookup"><span data-stu-id="22bb0-401">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="22bb0-402">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-402">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="22bb0-403">Используйте пробелы вокруг бинарных операторов.</span><span class="sxs-lookup"><span data-stu-id="22bb0-403">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="22bb0-404">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-404">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="22bb0-405">Используйте пробелы вокруг заметок типа двоеточия.</span><span class="sxs-lookup"><span data-stu-id="22bb0-405">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="22bb0-406">☑</span><span class="sxs-lookup"><span data-stu-id="22bb0-406">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="22bb0-407">Элементы во входном кортеже имеют правильный размер для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="22bb0-407">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="22bb0-408">☒</span><span class="sxs-lookup"><span data-stu-id="22bb0-408">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="22bb0-409">Пробелы следует подавлять после имени функции, операции или определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="22bb0-409">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

<span data-ttu-id="22bb0-410">_\*\*</span><span class="sxs-lookup"><span data-stu-id="22bb0-410">_\*\*</span></span>
