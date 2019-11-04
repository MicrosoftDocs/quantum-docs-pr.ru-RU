---
title: Вопросы и ответы по стилю | Документация Майкрософт
description: 'Инструкции в стиле Q #'
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
ms.openlocfilehash: 56455e9d5cd452b8620ee794f40563d1d3040193
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183851"
---
# <a name="q-style-guide"></a><span data-ttu-id="fd4e3-103">Инструкции в стиле Q #</span><span class="sxs-lookup"><span data-stu-id="fd4e3-103">Q# Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="fd4e3-104">Общие соглашения</span><span class="sxs-lookup"><span data-stu-id="fd4e3-104">General Conventions</span></span> ##

<span data-ttu-id="fd4e3-105">Соглашения, предлагаемые в этом разделе, призваны помочь сделать программы и библиотеки, написанные в Q #, проще читать и понимать.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-105">The conventions suggested in this guide are intended to help make programs and libraries written in Q# easier to read and understand.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-106">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-106">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-107">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-107">We suggest:</span></span>

- <span data-ttu-id="fd4e3-108">Не следует игнорировать соглашение, если это не сделано намеренно, чтобы предоставить пользователям более понятный и понятный код.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-109">Examples</span></span>](#tab/examples)

***

## <a name="naming-conventions"></a><span data-ttu-id="fd4e3-110">Соглашения об именовании</span><span class="sxs-lookup"><span data-stu-id="fd4e3-110">Naming Conventions</span></span> ##

<span data-ttu-id="fd4e3-111">В составе пакета средств разработки тактов мы стремимся использовать имена функций и операций, которые помогают разработчикам создавать программы, которые просты в чтении, и сокращают их сюрприз.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-111">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="fd4e3-112">Важной частью является то, что при выборе имен для функций, операций и типов мы создаем *словарь* , используемый программистами для выражения тактовых концепций. с нашими вариантами мы можем либо отнестись к их усилиям, чтобы четко взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-112">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="fd4e3-113">Это полагает ответственность за то, чтобы имена, которые мы предложит, были понятны, а не скрыты.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-113">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="fd4e3-114">В этом разделе мы подробно расскажу о том, как мы удовлетворены этим обязательством с точки зрения явных руководств, которые помогут нам лучше всего сделать это в сообществе разработчиков Q #.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-114">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the Q# development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="fd4e3-115">Операции и функции</span><span class="sxs-lookup"><span data-stu-id="fd4e3-115">Operations and Functions</span></span> ###

<span data-ttu-id="fd4e3-116">Одно из первых действий, которое должно установить имя, — это то, представляет ли заданный символ функцию или операцию.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-116">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="fd4e3-117">Разница между функциями и операциями крайне важна для понимания того, как работает блок кода.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-117">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="fd4e3-118">Чтобы обеспечить различие между функциями и операциями для пользователей, мы будем полагаться на то, что в Q # моделируется выполнение тактовых операций с помощью побочных эффектов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-118">To communicate the distinction between functions and operations to users, we rely on that Q# models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="fd4e3-119">Это значит, что операция *делает* что-то.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-119">That is, an operation *does* something.</span></span>

<span data-ttu-id="fd4e3-120">Функции, напротив, описывают математические связи между данными.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-120">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="fd4e3-121">Выражение *`Sin(PI() / 2.0)` `1.0`и не подразумевает* никакого состояния программы или ее Кубитс.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-121">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="fd4e3-122">Формирование сводных данных, операции выполняются, когда функции являются объектами.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-122">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="fd4e3-123">Это различие подразумевает, что операции именования являются глаголами и функциями в качестве существительных.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-123">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="fd4e3-124">При объявлении определяемого пользователем типа Новая функция, которая конструирует экземпляры этого типа, неявно определяется в то же время.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-124">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="fd4e3-125">С этой точки зрения определяемые пользователем типы должны называться существительными, чтобы оба типа и функции конструктора имели одинаковые имена.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-125">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="fd4e3-126">В разумных случаях убедитесь, что имена операций начинаются с глаголов, которые четко указывают на результат операции.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-126">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="fd4e3-127">Пример.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-127">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="fd4e3-128">Одним из случаев, которым заслуживает особое упоминание, является то, что операция принимает в качестве входных данных другую операцию и вызывает ее.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-128">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="fd4e3-129">В таких случаях действие, выполняемое входной операцией, не ясно при определении внешней операции, что означает, что правая команда не будет немедленно очищена.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-129">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="fd4e3-130">Рекомендуется использовать глагол `Apply`, как в `ApplyIf`, `ApplyToEach`и `ApplyToFirst`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-130">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="fd4e3-131">Другие глаголы также могут оказаться полезными в этом случае, как в `IterateThroughCartesianPower`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-131">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="fd4e3-132">Команда</span><span class="sxs-lookup"><span data-stu-id="fd4e3-132">Verb</span></span> | <span data-ttu-id="fd4e3-133">Ожидаемый результат</span><span class="sxs-lookup"><span data-stu-id="fd4e3-133">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="fd4e3-134">Применить</span><span class="sxs-lookup"><span data-stu-id="fd4e3-134">Apply</span></span> | <span data-ttu-id="fd4e3-135">Операция, предоставленная в качестве входных данных, называется</span><span class="sxs-lookup"><span data-stu-id="fd4e3-135">An operation provided as input is called</span></span> |
| <span data-ttu-id="fd4e3-136">Утверждающе</span><span class="sxs-lookup"><span data-stu-id="fd4e3-136">Assert</span></span> | <span data-ttu-id="fd4e3-137">Гипотеза о результате возможного измерения такта проверяется симулятором.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-137">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="fd4e3-138">Оценка</span><span class="sxs-lookup"><span data-stu-id="fd4e3-138">Estimate</span></span> | <span data-ttu-id="fd4e3-139">Возвращается классический параметр, представляющий оценку, полученную от одного или нескольких измерений.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-139">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="fd4e3-140">Measure</span><span class="sxs-lookup"><span data-stu-id="fd4e3-140">Measure</span></span> | <span data-ttu-id="fd4e3-141">Выполняется измерение такта, и результат возвращается пользователю.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-141">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="fd4e3-142">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-142">Prepare</span></span> | <span data-ttu-id="fd4e3-143">Заданный регистр Кубитс инициализируется в определенном состоянии</span><span class="sxs-lookup"><span data-stu-id="fd4e3-143">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="fd4e3-144">Пример</span><span class="sxs-lookup"><span data-stu-id="fd4e3-144">Sample</span></span> | <span data-ttu-id="fd4e3-145">Классическое значение возвращается случайным образом из некоторого распределения</span><span class="sxs-lookup"><span data-stu-id="fd4e3-145">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="fd4e3-146">Для функций мы рекомендуем избегать использования глаголов в пользу общих существительных (см. Руководство по правильным существительным ниже) или прилагательные:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-146">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="fd4e3-147">В частности, в большинстве случаев мы рекомендуем использовать последние партиЦиплес, где нужно указать, что имя функции строго соединено с действием или побочным эффектов в другом месте в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-147">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="fd4e3-148">Например, `ControlledOnInt` использует форму части причастий команды "Control", чтобы указать, что функция выступает в качестве прилагательной для изменения ее аргумента.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-148">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="fd4e3-149">Это имя имеет дополнительное преимущество в соответствии с семантикой встроенного `Controlled` функтор, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-149">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="fd4e3-150">Аналогичным образом можно использовать _существительные агентов_ для создания имен функций и определяемых пользователем типов из имен операций, как в случае с именем `Encoder` для определяемого пользователем типа, который строго связан с `Encode`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-150">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-151">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-151">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-152">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-152">We suggest:</span></span>

- <span data-ttu-id="fd4e3-153">Используйте глаголы для имен операций.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-153">Use verbs for operation names.</span></span>
- <span data-ttu-id="fd4e3-154">Для имен функций используйте существительные или прилагательные.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-154">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="fd4e3-155">Используйте существительные для определяемых пользователем типов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-155">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="fd4e3-156">Для всех вызываемых имен используйте `CamelCase` строгими предпочтениями для `pascalCase`, `snake_case`или `ANGRY_CASE`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-156">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="fd4e3-157">В частности, убедитесь, что вызываемые имена начинаются с прописных букв.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-157">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="fd4e3-158">Для всех локальных переменных используйте `pascalCase` строгими предпочтениями для `CamelCase`, `snake_case`или `ANGRY_CASE`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-158">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="fd4e3-159">В частности, убедитесь, что локальные переменные начинаются с строчных букв.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-159">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="fd4e3-160">Старайтесь не использовать знаки подчеркивания `_` в именах функций и операций; Если требуются дополнительные уровни иерархии, используйте пространства имен и псевдонимы пространств имен.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-160">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-161">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fd4e3-162">Name</span><span class="sxs-lookup"><span data-stu-id="fd4e3-162">Name</span></span> | <span data-ttu-id="fd4e3-163">Описание</span><span class="sxs-lookup"><span data-stu-id="fd4e3-163">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fd4e3-164">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-164">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="fd4e3-165">Снимите флажок использовать глагол ("отражать"), чтобы указать результат операции.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-165">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="fd4e3-166">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-166">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="fd4e3-167">Использование фразы существительное предлагает функцию, а не операцию.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-167">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="fd4e3-168">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-168">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="fd4e3-169">Используйте `snake_case` контравенес Q # Notation.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-169">Use of `snake_case` contravenes Q# notation.</span></span> |
| <span data-ttu-id="fd4e3-170">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-170">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="fd4e3-171">Используйте символы подчеркивания internal в качестве внутренних для имени операции контравенес Q # Notation.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-171">Use of underscores internal to operation name contravenes Q# notation.</span></span> |
| <span data-ttu-id="fd4e3-172">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-172">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="fd4e3-173">Использование фразы с существительным предполагает, что функция возвращает операцию.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-173">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="fd4e3-174">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-174">☑</span></span> | `function EqualityFact` | <span data-ttu-id="fd4e3-175">Снимите флажок использовать существительное (факт), чтобы указать, что это функция, в то время как прилагательное.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-175">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="fd4e3-176">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-176">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="fd4e3-177">Использование глагола ("Get") предполагает, что это операция.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-177">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="fd4e3-178">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-178">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="fd4e3-179">Явное использование фразы с существительным означает результат вызова конструктора определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-179">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="fd4e3-180">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-180">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="fd4e3-181">Использование глагола-фразы предполагает, что конструктор определяемого пользователем типа является операцией.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-181">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="fd4e3-182">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-182">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="fd4e3-183">Использование фразы существительное сообщает об использовании атрибута.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-183">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="fd4e3-184">Сокращенные и сокращенные обозначения</span><span class="sxs-lookup"><span data-stu-id="fd4e3-184">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="fd4e3-185">Приведенный выше Совет не отменяется, существует множество форм сокращений, которые являются распространенным и распространенным использованием в тактовых вычислениях.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-185">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="fd4e3-186">Мы рекомендуем использовать существующую и распространенную краткую форму, в которой он существует, особенно для операций, которые являются встроенными для работы целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-186">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="fd4e3-187">Например, можно выбрать имя `X` вместо `ApplyX`и `Rz` вместо `RotateAboutZ`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-187">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="fd4e3-188">При использовании такой сокращенной формы имена операций должны быть все прописными (например: `MAJ`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-188">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="fd4e3-189">При применении этого соглашения необходимо соблюдать осторожность в случае часто используемых акронимов и сокращений, например "Кфт" для "преобразования тактов в тактовой области".</span><span class="sxs-lookup"><span data-stu-id="fd4e3-189">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="fd4e3-190">Мы рекомендуем использовать следующие общие соглашения .NET для использования акронимов и сокращений в полных именах, которые предписывает:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-190">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="fd4e3-191">двузначные акронимы и сокращений именуются в верхнем регистре (например, `BE` для Big-endian).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-191">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="fd4e3-192">все более длинные акронимы и сокращенийы именуются в `CamelCase` (например, `Qft` для "преобразования в тактовую Фурье").</span><span class="sxs-lookup"><span data-stu-id="fd4e3-192">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="fd4e3-193">Таким образом, операция, реализующая Кфт, может либо `QFT` вызываться в качестве краткой, либо записываться как `ApplyQft`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-193">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="fd4e3-194">Для наиболее часто используемых операций и функций может быть желательно предоставить сокращенное имя в качестве _псевдонима_ для более длинной формы:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-194">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-195">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-195">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-196">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-196">We suggest:</span></span>

- <span data-ttu-id="fd4e3-197">При необходимости рекомендуется использовать распространенные и распространенные сокращенные имена.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-197">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="fd4e3-198">Для сокращения используйте прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-198">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="fd4e3-199">Используйте прописные буквы для коротких (двух букв) аббревиатур и сокращений.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-199">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="fd4e3-200">Используйте `CamelCase` для более длинных акронимов (три и более букв) и сокращений.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-200">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-201">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-201">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fd4e3-202">Name</span><span class="sxs-lookup"><span data-stu-id="fd4e3-202">Name</span></span> | <span data-ttu-id="fd4e3-203">Описание</span><span class="sxs-lookup"><span data-stu-id="fd4e3-203">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fd4e3-204">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-204">☑</span></span> | `X` | <span data-ttu-id="fd4e3-205">Хорошо понятная Краткая форма "применение преобразования $X $"</span><span class="sxs-lookup"><span data-stu-id="fd4e3-205">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="fd4e3-206">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-206">☑</span></span> | `CNOT` | <span data-ttu-id="fd4e3-207">Хорошо понятная Краткая форма для «контролируемых»</span><span class="sxs-lookup"><span data-stu-id="fd4e3-207">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="fd4e3-208">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-208">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="fd4e3-209">Краткая форма не должна находиться в `CamelCase`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-209">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="fd4e3-210">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-210">☑</span></span> | `ApplyQft` | <span data-ttu-id="fd4e3-211">Общий начальный вид "Кфт" отображается как часть имени длинной формы.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-211">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="fd4e3-212">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-212">☑</span></span> | `QFT` | <span data-ttu-id="fd4e3-213">Общий начальный вид "Кфт" отображается как часть сокращенного имени.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-213">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



***


### <a name="proper-nouns-in-names"></a><span data-ttu-id="fd4e3-214">Собственные существительные в именах</span><span class="sxs-lookup"><span data-stu-id="fd4e3-214">Proper Nouns in Names</span></span> ###

<span data-ttu-id="fd4e3-215">Хотя в физике мы часто называете вещи, когда первый пользователь публикует их, большинство фисиЦистс не знакомы с именами всех участников и журналами.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-215">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="fd4e3-216">Чрезмерная постановка в соглашениях об именовании от физикы может привести к значительному барьеру в записи, так как пользователи из других фоновых рисунков должны изучить большое количество непрозрачных имен, чтобы использовать общие операции и концепции.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-216">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="fd4e3-217">Таким образом, рекомендуется, чтобы при разумных принципах обычные существительные, описывающие концепцию, были приняты строгими для правильного существительных, описывающих историю публикации концепции.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-217">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="fd4e3-218">В качестве конкретного примера, контролируемые с помощью управляемой операции переключения и удвоения часто называются операциями "Фредкин" и "Тоффоли" в учебных литературах, но они определяются в Q # в основном как `CSWAP` и `CCNOT`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-218">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in Q# primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="fd4e3-219">В обоих случаях комментарии к документации по API предоставляют имена синонимов на основе правильных существительных, а также все соответствующие ссылки.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-219">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="fd4e3-220">Этот приоритет особенно важен в тех случаях, когда необходимо всегда использовать собственные существительные — Q # соответствует традиции, заданному многими классическими языками, и относится к `Bool`ным типам в ссылке на логическую логику, которая в свою очередь имеет имя. от Георгия.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-220">This preference is especially important given that some usage of proper nouns will always be necessary — Q# follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="fd4e3-221">Некоторые тактовые концепции аналогичны именам, включая тип `Pauli`, встроенный в язык Q #.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-221">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the Q# language.</span></span>
<span data-ttu-id="fd4e3-222">Свести к минимуму использование правильных существительных, если такое использование не является обязательным, мы уменьшаем влияние того, что их не удается избежать.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-222">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-223">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-223">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="fd4e3-224">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-224">We suggest:</span></span>

- <span data-ttu-id="fd4e3-225">Избегайте использования в именах правильных существительных.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-225">Avoid the use of proper nouns in names.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-226">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-226">Examples</span></span>](#tab/examples)

***

### <a name="type-conversions"></a><span data-ttu-id="fd4e3-227">Преобразования типов</span><span class="sxs-lookup"><span data-stu-id="fd4e3-227">Type Conversions</span></span> ###

<span data-ttu-id="fd4e3-228">Поскольку Q # является строго и статически типизированным языком, значение одного типа может использоваться только как значение другого типа с помощью явного вызова функции преобразования типа.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-228">Since Q# is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="fd4e3-229">Это отличается от языков, позволяющих неявным образом изменять типы значений (например, повышение типа) или путем приведения.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-229">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="fd4e3-230">В результате функции преобразования типов играют важную роль в вопросах разработки библиотеки Q # и составляют одно из наиболее часто встречающихся решений по именованию.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-230">As a result, type conversion functions play an important role in Q# library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="fd4e3-231">Однако обратите внимание, что поскольку преобразования типов всегда _детерминированы_, они могут быть написаны как функции и, таким образом, находиться на приведенный выше Совет.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-231">We note, however, that since type conversions are always _deterministic_, they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="fd4e3-232">В частности, мы советуем, что функции преобразования типов никогда не должны называться как глаголы (например, `ConvertToX`) или модификаторовные фразы (`ToX`), но должны называться как прилагательные фразы, которые указывают типы источника и назначения (`XAsY`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-232">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="fd4e3-233">При перечислении типов массивов в именах функций преобразования типов рекомендуется использовать краткую `Arr`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-233">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="fd4e3-234">При запрете исключительных обстоятельств рекомендуется, чтобы все функции преобразования типов были именованы с помощью `As`, чтобы их можно было быстро определить.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-234">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-235">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-235">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-236">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-236">We suggest:</span></span>

- <span data-ttu-id="fd4e3-237">Если функция преобразует значение типа `X` в значение типа `Y`, используйте либо имя `AsY`, либо `XAsY`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-237">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-238">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-238">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fd4e3-239">Name</span><span class="sxs-lookup"><span data-stu-id="fd4e3-239">Name</span></span> | <span data-ttu-id="fd4e3-240">Описание</span><span class="sxs-lookup"><span data-stu-id="fd4e3-240">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fd4e3-241">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-241">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="fd4e3-242">В качестве отстановки "до" задается Командная фраза, указывающая на операцию, а не на функцию.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-242">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="fd4e3-243">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-243">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="fd4e3-244">Тип входных данных не является понятным по имени функции.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-244">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="fd4e3-245">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-245">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="fd4e3-246">Входные и выходные типы отображаются в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-246">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="fd4e3-247">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-247">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="fd4e3-248">Типы входных и выходных данных являются четкими.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-248">Both the input types and output types are clear.</span></span> |

***

### <a name="private-or-internal-names"></a><span data-ttu-id="fd4e3-249">Частные или внутренние имена</span><span class="sxs-lookup"><span data-stu-id="fd4e3-249">Private or Internal Names</span></span> ###

<span data-ttu-id="fd4e3-250">Во многих случаях имя предназначено исключительно для внутреннего использования в библиотеке или проекте и не является гарантированной частью API, предоставляемой библиотекой.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-250">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="fd4e3-251">Полезно четко указать, что это происходит при именовании функций и операций, так что случайные зависимости от внутреннего кода становятся очевидными.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-251">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="fd4e3-252">Если операция или функция не предназначена для непосредственного использования, а должна использоваться соответствующим вызываемым методом, который действует частичным приложением, рекомендуется использовать имя, начинающееся с `_`, для частично примененного вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-252">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with `_` for the callable that is partially applied.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-253">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-253">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-254">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-254">We suggest:</span></span>

- <span data-ttu-id="fd4e3-255">Если функция, операция или определяемый пользователем тип не являются частью общедоступного API для библиотеки или программы Q #, убедитесь, что ее имя начинается с подчеркивания в начале (`_`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-255">When a function, operation, or user-defined type is not a part of the public API for a Q# library or program, ensure that its name begins with a leading underscore (`_`).</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-256">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-256">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fd4e3-257">Name</span><span class="sxs-lookup"><span data-stu-id="fd4e3-257">Name</span></span> | <span data-ttu-id="fd4e3-258">Описание</span><span class="sxs-lookup"><span data-stu-id="fd4e3-258">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fd4e3-259">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-259">☒</span></span> | <s>`ApplyDecomposedOperation_`</s> | <span data-ttu-id="fd4e3-260">Символ подчеркивания `_` не должен располагаться в конце имени.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-260">The underscore `_` should not appear at the end of the name.</span></span> |
| <span data-ttu-id="fd4e3-261">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-261">☑</span></span> | `_ApplyDecomposedOperation` | <span data-ttu-id="fd4e3-262">Символ подчеркивания `_` в начале ясно указывает, что эта операция предназначена только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-262">The underscore `_` at the beginning clearly indicates that this operation is for internal use only.</span></span> |

***

### <a name="variants"></a><span data-ttu-id="fd4e3-263">Случаях</span><span class="sxs-lookup"><span data-stu-id="fd4e3-263">Variants</span></span> ###

<span data-ttu-id="fd4e3-264">Хотя это ограничение может не сохраняться в будущих версиях Q #, в настоящее время существует ситуация, когда часто встречаются группы связанных операций или функций, которые различаются операторов их входными данными, или конкретными типами их аргументов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-264">Though this limitation may not persist in future versions of Q#, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="fd4e3-265">Эти группы можно отличать с помощью одного и того же корневого имени, за которым следует одна или две буквы, указывающие на вариант.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-265">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="fd4e3-266">Суффикс</span><span class="sxs-lookup"><span data-stu-id="fd4e3-266">Suffix</span></span> | <span data-ttu-id="fd4e3-267">Значение</span><span class="sxs-lookup"><span data-stu-id="fd4e3-267">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="fd4e3-268">Ожидается ввод для поддержки `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="fd4e3-268">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="fd4e3-269">Ожидается ввод для поддержки `Controlled`</span><span class="sxs-lookup"><span data-stu-id="fd4e3-269">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="fd4e3-270">Ожидается ввод для поддержки `Controlled` и `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="fd4e3-270">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="fd4e3-271">Входные или входные данные имеют тип `Int`</span><span class="sxs-lookup"><span data-stu-id="fd4e3-271">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="fd4e3-272">Входные или входные данные имеют тип `Double`</span><span class="sxs-lookup"><span data-stu-id="fd4e3-272">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="fd4e3-273">Входные или входные данные имеют тип `BigInt`</span><span class="sxs-lookup"><span data-stu-id="fd4e3-273">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-274">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-274">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-275">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-275">We suggest:</span></span>

- <span data-ttu-id="fd4e3-276">Если функция или операция не связаны с аналогичными функциями или операциями по типам и функтор поддерживают свои входные данные, не используйте суффикс.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-276">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="fd4e3-277">Если функция или операция связана с любыми аналогичными функциями или операциями типов и функтор поддержки своих входных данных, используйте суффиксы, как показано в таблице выше, чтобы различать варианты.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-277">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-278">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-278">Examples</span></span>](#tab/examples)

***

### <a name="arguments-and-variables"></a><span data-ttu-id="fd4e3-279">Аргументы и переменные</span><span class="sxs-lookup"><span data-stu-id="fd4e3-279">Arguments and Variables</span></span> ###

<span data-ttu-id="fd4e3-280">Ключевой целью кода Q # для функции или операции является простое чтение и понимание.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-280">A key goal of the Q# code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="fd4e3-281">Аналогичным образом, имена входов и аргументов типа должны сообщать, как функция или аргумент будут использоваться по мере того, как они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-281">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-282">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-282">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-283">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-283">We suggest:</span></span>

- <span data-ttu-id="fd4e3-284">Для всех переменных и входных имен используйте `pascalCase` строгими предпочтениями для `CamelCase`, `snake_case`или `ANGRY_CASE`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-284">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="fd4e3-285">Входные имена должны быть описательными; по возможности избегайте по одному или двум именам букв.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-285">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="fd4e3-286">Операции и функции, принимающие ровно один аргумент типа, должны отметить этот аргумент типа `T`, если его роль очевидна.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-286">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="fd4e3-287">Если функция или операция принимает несколько аргументов типа или если роль одного аргумента типа не очевидна, рассмотрите возможность использования короткого слова в заглавной букве, которое предшествует `T` (например, `TOutput`) для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-287">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="fd4e3-288">Не включайте имена типов в имена аргументов и переменных. Эти сведения могут и должны предоставляться средой разработки.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-288">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="fd4e3-289">Запишите скалярные типы по их литеральным именам (`flagQubit`) и типам массивов во множественном числе (`measResults`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-289">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="fd4e3-290">Для массивов Кубитс в частности, рассмотрите такие типы, `Register`, где имя относится к последовательности Кубитс, которые тесно связаны друг с другим способом.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-290">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="fd4e3-291">Переменные, используемые в качестве индексов в массивах, должны начинаться с `idx` и быть единственным (например: `things[idxThing]`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-291">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="fd4e3-292">В частности, настоятельно рекомендуется избегать использования однобуквенных имен переменных в качестве индексов; Рассмотрите возможность использования `idx` как минимум.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-292">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="fd4e3-293">Переменные, используемые для хранения длин массивов, должны начинаться с `n` и должны быть множественными (например: `nThings`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-293">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-294">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-294">Examples</span></span>](#tab/examples)

***

### <a name="user-defined-type-named-items"></a><span data-ttu-id="fd4e3-295">Определяемый пользователем тип с именем Items</span><span class="sxs-lookup"><span data-stu-id="fd4e3-295">User Defined Type Named Items</span></span> ###

<span data-ttu-id="fd4e3-296">Именованные элементы в определяемых пользователем типах должны называться как `CamelCase`, даже при вводе в конструкторы определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-296">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="fd4e3-297">Это помогает в явном отделении именованных элементов от ссылок на переменные в локальной области при использовании нотации метода доступа (например, `callable::Apply`) или нотации копирования и обновления (`set arr w/= Data <- newData`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-297">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-298">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-298">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-299">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-299">We suggest:</span></span>

- <span data-ttu-id="fd4e3-300">Именованные элементы в конструкторах определяемых пользователем типов должны называться как `CamelCase`; то есть они должны начинаться с начального верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-300">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="fd4e3-301">Именованные элементы, которые разрешаются в операции, должны называться этапами глагола.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-301">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="fd4e3-302">Именованные элементы, которые не разрешаются в операции, должны называться как субстантивные словосочетания.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-302">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="fd4e3-303">Для определяемых пользователем типов, которые обносят операции, необходимо определить один именованный элемент с именем `Apply`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-303">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-304">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-304">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fd4e3-305">Пример</span><span class="sxs-lookup"><span data-stu-id="fd4e3-305">Snippet</span></span> | <span data-ttu-id="fd4e3-306">Описание</span><span class="sxs-lookup"><span data-stu-id="fd4e3-306">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="fd4e3-307">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-307">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="fd4e3-308">Имя `Apply` — это `CamelCase`ая глаголовая фраза, предлагающая, что именованный элемент является операцией.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-308">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="fd4e3-309">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-309">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="fd4e3-310">Именованные элементы должны начинаться с первой прописной буквы.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-310">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="fd4e3-311">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-311">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="fd4e3-312">Именованные элементы, которые разрешаются в функции, должны называться как субстантивные словосочетания, а не как фразы глагола.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-312">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

***

## <a name="input-conventions"></a><span data-ttu-id="fd4e3-313">Соглашения о входе</span><span class="sxs-lookup"><span data-stu-id="fd4e3-313">Input Conventions</span></span> ##

<span data-ttu-id="fd4e3-314">Когда разработчик обращается к операции или функции, различные входные данные этой операции или функции должны быть указаны в определенном порядке, увеличивая при этом функциональную нагрузку, которую разработчик может использовать для создания библиотеки.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-314">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="fd4e3-315">В частности, задача по запоминанию порядка входных данных часто является отправной задачей: программированием реализации алгоритма такта.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-315">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="fd4e3-316">Хотя широкая поддержка интегрированной среды разработки может снизить это до большого экстента, хорошая разработка и соблюдение общих соглашений также может помочь минимизировать неудачную загрузку, наложенную API.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-316">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="fd4e3-317">Там, где это возможно, может быть полезно уменьшить количество входных данных, ожидаемых операцией или функцией, чтобы роль каждого входа была более очевидна для разработчиков, обращающихся к этой операции или функции, а также для разработчиков, считывающих этот код позже.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-317">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="fd4e3-318">Особенно если невозможно или разумно уменьшить число аргументов для операции или функции, важно иметь единообразный порядок, позволяющий свести к сведению, что пользователь сталкивается с прогнозированием порядка входных данных.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-318">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="fd4e3-319">Мы рекомендуем использовать соглашения о порядке ввода, которые во многом наследуют от мышления частичного приложения как обобщение карринг f (x, y) ≡ f (x) (y).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-319">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="fd4e3-320">Таким образом, частичное применение первых аргументов должно привести к вызову, который будет полезен при любом разумном использовании.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-320">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="fd4e3-321">Следуя этому принципу, рассмотрите возможность использования следующего порядка аргументов:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-321">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="fd4e3-322">Классические не вызываемые аргументы, такие как углы, векторы степеней и т. д.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-322">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="fd4e3-323">Вызываемые аргументы (функции и аргументы).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-323">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="fd4e3-324">Если обе функции и операции выполняются в качестве аргументов, попробуйте разместить операции после функций.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-324">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="fd4e3-325">Коллекции, обрабатываемые с помощью вызываемых аргументов аналогичным образом для `Map`, `Iter`, `Enumerate`и `Fold`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-325">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="fd4e3-326">Аргументы кубит, используемые в качестве элементов управления.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-326">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="fd4e3-327">Аргументы кубит, используемые в качестве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-327">Qubit arguments used as targets.</span></span>

<span data-ttu-id="fd4e3-328">Рассмотрим операцию `ApplyPhaseEstimationIteration` для использования в оценке этапа, которая принимает угол и Oracle, передает угол `Rz`, измененный массивом различных факторов масштабирования, а затем управляет приложениями Oracle.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-328">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="fd4e3-329">Мы упорядочиваем входные данные для `ApplyPhaseEstimationIteration` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-329">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

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
<span data-ttu-id="fd4e3-330">В качестве особого варианта минимизации неожиданности некоторые функции и операции имитируют поведение встроенных `Adjoint` операторов и `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-330">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="fd4e3-331">Например, `ControlledOnInt<'T>` имеет тип `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, так что `ControlledOnInt<Qubit[]>(5, _)` действует как `Controlled` функтор, но в случае, когда регистр элемента управления представляет состояние $ \кет{5} = \кет{101}$.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-331">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="fd4e3-332">Таким образом, разработчику требуется, чтобы входные данные `ControlledOnInt` поместились в последний раз вызываемый объект, а полученная операция принимает в качестве входных `(Qubit[], 'T)`---том же порядке, в котором следуют выходные данные `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-332">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-333">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-333">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-334">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-334">We suggest:</span></span>

- <span data-ttu-id="fd4e3-335">Используйте порядок ввода в соответствии с использованием частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-335">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="fd4e3-336">Используйте порядок ввода в соответствии со встроенными операторов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-336">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="fd4e3-337">Разместите все классические входные данные перед любыми входными тактовыми тактами.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-337">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-338">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-338">Examples</span></span>](#tab/examples)

***

## <a name="documentation-conventions"></a><span data-ttu-id="fd4e3-339">Соглашения о документации</span><span class="sxs-lookup"><span data-stu-id="fd4e3-339">Documentation Conventions</span></span> ##

<span data-ttu-id="fd4e3-340">Язык Q # позволяет прикреплять документацию к операциям, функциям и определяемым пользователем типам с помощью специально отформатированных комментариев к документации.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-340">The Q# language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="fd4e3-341">Эти комментарии к документации, обозначенные тройными косыми чертами (`///`), представляют собой небольшие [Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) документы, которые можно использовать для описания назначения каждой операции, функции и определяемого пользователем типа, возвращаемых входов и т. д.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-341">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="fd4e3-342">Компилятор, поставляемый с пакетом разработки тактов, извлекает эти комментарии и использует их для помощи в документации по типам, похожим на https://docs.microsoft.com/quantum.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-342">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="fd4e3-343">Аналогичным образом, языковой сервер, поставляемый с пакетом разработки тактовой передачи, использует эти комментарии для предоставления помощи пользователям при наведении указателя мыши на символы в коде Q #.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-343">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their Q# code.</span></span>
<span data-ttu-id="fd4e3-344">Использование комментариев к документации может помочь пользователям лучше понять код, предоставляя полезную ссылку для получения подробных сведений, которые не просто выражаются с помощью других соглашений в этом документе.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-344">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

<div class="nextstepaction"><span data-ttu-id="fd4e3-345">
    [Справочник по синтаксису комментариев документации](xref:microsoft.quantum.language.statements#documentation-comments)
</span><span class="sxs-lookup"><span data-stu-id="fd4e3-345">
    [Documentation comment syntax reference](xref:microsoft.quantum.language.statements#documentation-comments)
</span></span></div>

<span data-ttu-id="fd4e3-346">Чтобы эффективно использовать эту функцию для пользователей, рекомендуется учитывать некоторые моменты при написании комментариев к документации.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-346">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-347">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-347">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fd4e3-348">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-348">We suggest:</span></span>

- <span data-ttu-id="fd4e3-349">Каждая открытая функция, операция и определяемый пользователем тип должны непосредственно предшествовать комментарию документации.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-349">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="fd4e3-350">Каждый комментарий к документации должен содержать как минимум следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-350">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="fd4e3-351">Резюме</span><span class="sxs-lookup"><span data-stu-id="fd4e3-351">Summary</span></span>
    - <span data-ttu-id="fd4e3-352">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fd4e3-352">Input</span></span>
    - <span data-ttu-id="fd4e3-353">Выходные данные (если применимо)</span><span class="sxs-lookup"><span data-stu-id="fd4e3-353">Output (if applicable)</span></span>
- <span data-ttu-id="fd4e3-354">Убедитесь, что все сводки имеют два предложения или меньше.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-354">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="fd4e3-355">Если требуется больше места, предоставьте `# Description` раздел сразу после `# Summary` с подробными сведениями.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-355">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="fd4e3-356">В разумных случаях не включайте математические вычисления в сводки, так как не все клиенты поддерживают да нотацию в сводках.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-356">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="fd4e3-357">Обратите внимание, что при написании документов prose (например, да или Markdown) может быть предпочтительнее использовать более длинные строки.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-357">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="fd4e3-358">Укажите все соответствующие математические выражения в разделе `# Description`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-358">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="fd4e3-359">При описании входных данных не следует повторять типы всех входных данных, так как они могут выводиться компилятором и угрожать несогласованность.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-359">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="fd4e3-360">Укажите нужные примеры, каждый в отдельном разделе `# Example`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-360">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="fd4e3-361">Кратко опишите каждый пример перед выводом кода.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-361">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="fd4e3-362">Посвящены всем соответствующим академическим публикациям (например, документы, материалы, записи в блоге и альтернативные реализации) в разделе `# References` в виде маркированного списка ссылок.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-362">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="fd4e3-363">Убедитесь, что, где это возможно, все ссылки ссылок относятся к постоянным и неизменяемым идентификаторам (Доис или номера Арксив версий).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-363">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="fd4e3-364">Если операция или функция связана с другими операциями или функциями с помощью функтор Variant, перечислите другие варианты в виде маркеров в разделе `# See Also`.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-364">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="fd4e3-365">Оставьте пустую строку комментария между разделами уровня 1 (`/// #`), но не оставляйте пустую строку между разделами уровня 2 (`/// ##`).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-365">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-366">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-366">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="fd4e3-367">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-367">☑</span></span> ####

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

***

## <a name="formatting-conventions"></a><span data-ttu-id="fd4e3-368">Соглашения о форматировании</span><span class="sxs-lookup"><span data-stu-id="fd4e3-368">Formatting Conventions</span></span> ##

<span data-ttu-id="fd4e3-369">Помимо описанных выше предложений, рекомендуется сделать код максимально удобочитаемым, чтобы использовать единообразные правила форматирования.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-369">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="fd4e3-370">Такие правила форматирования по сути, как правило, являются несколько произвольными и хорошо эстетичность.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-370">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="fd4e3-371">Тем не менее рекомендуется поддерживать единообразный набор соглашений о форматировании в группе участников совместной работы, особенно для больших проектов Q #, таких как сам пакет разработки такта.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-371">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large Q# projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="fd4e3-372">Эти правила могут быть автоматически применены с помощью средства форматирования, интегрированного с компилятором Q #.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-372">These rules can be automatically applied by using the formatting tool integrated with the Q# compiler.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="fd4e3-373">Руководство</span><span class="sxs-lookup"><span data-stu-id="fd4e3-373">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="fd4e3-374">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-374">We suggest:</span></span>

- <span data-ttu-id="fd4e3-375">Для переносимости используйте четыре пробела вместо вкладок.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-375">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="fd4e3-376">Например, в VS Code:</span><span class="sxs-lookup"><span data-stu-id="fd4e3-376">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="fd4e3-377">Строка переносится в 79 символов, где это оправданно.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-377">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="fd4e3-378">Используйте пробелы вокруг бинарных операторов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-378">Use spaces around binary operators.</span></span>
- <span data-ttu-id="fd4e3-379">Используйте пробелы с обеих сторон двоеточий, используемых для заметок типов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-379">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="fd4e3-380">Используйте один пробел после запятых, используемых в массивах и литералах кортежа (например, в входных данных для функций и операций).</span><span class="sxs-lookup"><span data-stu-id="fd4e3-380">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="fd4e3-381">Не используйте пробелы после имени функции, операции или определяемого пользователем типа или после `@` в объявлениях атрибутов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-381">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="fd4e3-382">Каждое объявление атрибута должно располагаться в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-382">Each attribute declaration should be on its own line.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="fd4e3-383">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd4e3-383">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fd4e3-384">Пример</span><span class="sxs-lookup"><span data-stu-id="fd4e3-384">Snippet</span></span> | <span data-ttu-id="fd4e3-385">Описание</span><span class="sxs-lookup"><span data-stu-id="fd4e3-385">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="fd4e3-386">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-386">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="fd4e3-387">Используйте пробелы вокруг бинарных операторов.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-387">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="fd4e3-388">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-388">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="fd4e3-389">Используйте пробелы вокруг заметок типа двоеточия.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-389">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="fd4e3-390">☑</span><span class="sxs-lookup"><span data-stu-id="fd4e3-390">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="fd4e3-391">Элементы во входном кортеже имеют правильный размер для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-391">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="fd4e3-392">☒</span><span class="sxs-lookup"><span data-stu-id="fd4e3-392">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="fd4e3-393">Пробелы следует подавлять после имени функции, операции или определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="fd4e3-393">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

***

