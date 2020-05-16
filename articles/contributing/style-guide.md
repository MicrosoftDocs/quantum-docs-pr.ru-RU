---
title: 'Рекомендации по стилю Microsoft Q #'
description: 'Сведения об именовании, вводе, документации и соглашениях по форматированию для Q # Programs and librarys.'
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
ms.openlocfilehash: dfb2b1779e3ddc77fc74697bc4dc2904b1a0c70f
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426927"
---
# <a name="q-style-guide"></a><span data-ttu-id="2f6bd-103">Инструкции в стиле Q #</span><span class="sxs-lookup"><span data-stu-id="2f6bd-103">Q# Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="2f6bd-104">Общие соглашения</span><span class="sxs-lookup"><span data-stu-id="2f6bd-104">General Conventions</span></span> ##

<span data-ttu-id="2f6bd-105">Соглашения, предлагаемые в этом разделе, призваны помочь сделать программы и библиотеки, написанные в Q #, проще читать и понимать.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-105">The conventions suggested in this guide are intended to help make programs and libraries written in Q# easier to read and understand.</span></span>

## <a name="guidance"></a><span data-ttu-id="2f6bd-106">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-106">Guidance</span></span>

<span data-ttu-id="2f6bd-107">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-107">We suggest:</span></span>

- <span data-ttu-id="2f6bd-108">Не следует игнорировать соглашение, если это не сделано намеренно, чтобы предоставить пользователям более понятный и понятный код.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="2f6bd-109">Соглашения об именах</span><span class="sxs-lookup"><span data-stu-id="2f6bd-109">Naming Conventions</span></span> ##

<span data-ttu-id="2f6bd-110">В составе пакета средств разработки тактов мы стремимся использовать имена функций и операций, которые помогают разработчикам создавать программы, которые просты в чтении, и сокращают их сюрприз.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-110">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="2f6bd-111">Важной частью является то, что при выборе имен для функций, операций и типов мы создаем *словарь* , используемый программистами для выражения тактовых концепций. с нашими вариантами мы можем либо отнестись к их усилиям, чтобы четко взаимодействовать.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-111">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="2f6bd-112">Это полагает ответственность за то, чтобы имена, которые мы предложит, были понятны, а не скрыты.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-112">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="2f6bd-113">В этом разделе мы подробно расскажу о том, как мы удовлетворены этим обязательством с точки зрения явных руководств, которые помогут нам лучше всего сделать это в сообществе разработчиков Q #.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-113">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the Q# development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="2f6bd-114">Операции и функции</span><span class="sxs-lookup"><span data-stu-id="2f6bd-114">Operations and Functions</span></span> ###

<span data-ttu-id="2f6bd-115">Одно из первых действий, которое должно установить имя, — это то, представляет ли заданный символ функцию или операцию.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-115">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="2f6bd-116">Разница между функциями и операциями крайне важна для понимания того, как работает блок кода.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-116">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="2f6bd-117">Чтобы обеспечить различие между функциями и операциями для пользователей, мы будем полагаться на то, что в Q # моделируется выполнение тактовых операций с помощью побочных эффектов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-117">To communicate the distinction between functions and operations to users, we rely on that Q# models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="2f6bd-118">Это значит, что операция *делает* что-то.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-118">That is, an operation *does* something.</span></span>

<span data-ttu-id="2f6bd-119">Функции, напротив, описывают математические связи между данными.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-119">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="2f6bd-120">Выражение `Sin(PI() / 2.0)` *имеет* значение `1.0` и не подразумевает ничего о состоянии программы или ее Кубитс.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-120">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="2f6bd-121">Формирование сводных данных, операции выполняются, когда функции являются объектами.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-121">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="2f6bd-122">Это различие подразумевает, что операции именования являются глаголами и функциями в качестве существительных.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-122">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="2f6bd-123">При объявлении определяемого пользователем типа Новая функция, которая конструирует экземпляры этого типа, неявно определяется в то же время.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-123">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="2f6bd-124">С этой точки зрения определяемые пользователем типы должны называться существительными, чтобы оба типа и функции конструктора имели одинаковые имена.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-124">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="2f6bd-125">В разумных случаях убедитесь, что имена операций начинаются с глаголов, которые четко указывают на результат операции.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-125">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="2f6bd-126">Пример:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-126">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="2f6bd-127">Одним из случаев, которым заслуживает особое упоминание, является то, что операция принимает в качестве входных данных другую операцию и вызывает ее.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-127">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="2f6bd-128">В таких случаях действие, выполняемое входной операцией, не ясно при определении внешней операции, что означает, что правая команда не будет немедленно очищена.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-128">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="2f6bd-129">Рекомендуется использовать команду `Apply` , как в `ApplyIf` , `ApplyToEach` и `ApplyToFirst` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-129">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="2f6bd-130">Другие глаголы также могут быть полезны в этом случае, как в `IterateThroughCartesianPower` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-130">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="2f6bd-131">Команда</span><span class="sxs-lookup"><span data-stu-id="2f6bd-131">Verb</span></span> | <span data-ttu-id="2f6bd-132">Ожидаемый результат</span><span class="sxs-lookup"><span data-stu-id="2f6bd-132">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="2f6bd-133">Применить</span><span class="sxs-lookup"><span data-stu-id="2f6bd-133">Apply</span></span> | <span data-ttu-id="2f6bd-134">Операция, предоставленная в качестве входных данных, называется</span><span class="sxs-lookup"><span data-stu-id="2f6bd-134">An operation provided as input is called</span></span> |
| <span data-ttu-id="2f6bd-135">Assert</span><span class="sxs-lookup"><span data-stu-id="2f6bd-135">Assert</span></span> | <span data-ttu-id="2f6bd-136">Гипотеза о результате возможного измерения такта проверяется симулятором.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-136">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="2f6bd-137">Оценка</span><span class="sxs-lookup"><span data-stu-id="2f6bd-137">Estimate</span></span> | <span data-ttu-id="2f6bd-138">Возвращается классический параметр, представляющий оценку, полученную от одного или нескольких измерений.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-138">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="2f6bd-139">Measure</span><span class="sxs-lookup"><span data-stu-id="2f6bd-139">Measure</span></span> | <span data-ttu-id="2f6bd-140">Выполняется измерение такта, и результат возвращается пользователю.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-140">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="2f6bd-141">Подготовка.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-141">Prepare</span></span> | <span data-ttu-id="2f6bd-142">Заданный регистр Кубитс инициализируется в определенном состоянии</span><span class="sxs-lookup"><span data-stu-id="2f6bd-142">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="2f6bd-143">Образец</span><span class="sxs-lookup"><span data-stu-id="2f6bd-143">Sample</span></span> | <span data-ttu-id="2f6bd-144">Классическое значение возвращается случайным образом из некоторого распределения</span><span class="sxs-lookup"><span data-stu-id="2f6bd-144">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="2f6bd-145">Для функций мы рекомендуем избегать использования глаголов в пользу общих существительных (см. Руководство по правильным существительным ниже) или прилагательные:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-145">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="2f6bd-146">В частности, в большинстве случаев мы рекомендуем использовать последние партиЦиплес, где нужно указать, что имя функции строго соединено с действием или побочным эффектов в другом месте в тактовой программе.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-146">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="2f6bd-147">Например, `ControlledOnInt` использует форму части причастий команды "Control", чтобы указать, что функция выступает в качестве прилагательного для изменения своего аргумента.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-147">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="2f6bd-148">Это имя имеет дополнительное преимущество в соответствии с семантикой встроенных `Controlled` функтор, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-148">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="2f6bd-149">Аналогичным образом можно использовать _существительные агентов_ для создания имен функций и определяемых пользователем типов из имен операций, как в случае имени `Encoder` определяемого пользователем типа, который строго связан с `Encode` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-149">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-150">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-150">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-151">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-151">We suggest:</span></span>

- <span data-ttu-id="2f6bd-152">Используйте глаголы для имен операций.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-152">Use verbs for operation names.</span></span>
- <span data-ttu-id="2f6bd-153">Для имен функций используйте существительные или прилагательные.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-153">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="2f6bd-154">Используйте существительные для определяемых пользователем типов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-154">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="2f6bd-155">Для всех вызываемых имен используйте `CamelCase` строгое предпочтение для `pascalCase` , `snake_case` или `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-155">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="2f6bd-156">В частности, убедитесь, что вызываемые имена начинаются с прописных букв.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-156">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="2f6bd-157">Для всех локальных переменных используйте `pascalCase` строгое предпочтение в `CamelCase` , `snake_case` или `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-157">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="2f6bd-158">В частности, убедитесь, что локальные переменные начинаются с строчных букв.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-158">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="2f6bd-159">Избегайте использования знаков подчеркивания `_` в именах функций и операций, где требуются дополнительные уровни иерархии, используйте пространства имен и псевдонимы пространств имен.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-159">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-160">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="2f6bd-161">Имя</span><span class="sxs-lookup"><span data-stu-id="2f6bd-161">Name</span></span> | <span data-ttu-id="2f6bd-162">Описание</span><span class="sxs-lookup"><span data-stu-id="2f6bd-162">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="2f6bd-163">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-163">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="2f6bd-164">Снимите флажок использовать глагол ("отражать"), чтобы указать результат операции.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-164">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="2f6bd-165">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-165">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="2f6bd-166">Использование фразы существительное предлагает функцию, а не операцию.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-166">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="2f6bd-167">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-167">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="2f6bd-168">Использование `snake_case` нотации Контравенес Q #.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-168">Use of `snake_case` contravenes Q# notation.</span></span> |
| <span data-ttu-id="2f6bd-169">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-169">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="2f6bd-170">Используйте символы подчеркивания internal в качестве внутренних для имени операции контравенес Q # Notation.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-170">Use of underscores internal to operation name contravenes Q# notation.</span></span> |
| <span data-ttu-id="2f6bd-171">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-171">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="2f6bd-172">Использование фразы с существительным предполагает, что функция возвращает операцию.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-172">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="2f6bd-173">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-173">☑</span></span> | `function EqualityFact` | <span data-ttu-id="2f6bd-174">Снимите флажок использовать существительное (факт), чтобы указать, что это функция, в то время как прилагательное.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-174">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="2f6bd-175">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-175">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="2f6bd-176">Использование глагола ("Get") предполагает, что это операция.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-176">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="2f6bd-177">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-177">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="2f6bd-178">Явное использование фразы с существительным означает результат вызова конструктора определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-178">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="2f6bd-179">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-179">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="2f6bd-180">Использование глагола-фразы предполагает, что конструктор определяемого пользователем типа является операцией.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-180">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="2f6bd-181">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-181">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="2f6bd-182">Использование фразы существительное сообщает об использовании атрибута.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-182">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="2f6bd-183">Сокращенные и сокращенные обозначения</span><span class="sxs-lookup"><span data-stu-id="2f6bd-183">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="2f6bd-184">Приведенный выше Совет не отменяется, существует множество форм сокращений, которые являются распространенным и распространенным использованием в тактовых вычислениях.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-184">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="2f6bd-185">Мы рекомендуем использовать существующую и распространенную краткую форму, в которой он существует, особенно для операций, которые являются встроенными для работы целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-185">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="2f6bd-186">Например, мы выбираем имя, а не `X` `ApplyX` `Rz` `RotateAboutZ` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-186">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="2f6bd-187">При использовании такой сокращенной формы имена операций должны быть все прописными (например: `MAJ` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-187">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="2f6bd-188">При применении этого соглашения необходимо соблюдать осторожность в случае часто используемых акронимов и сокращений, например "Кфт" для "преобразования тактов в тактовой области".</span><span class="sxs-lookup"><span data-stu-id="2f6bd-188">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="2f6bd-189">Мы рекомендуем использовать следующие общие соглашения .NET для использования акронимов и сокращений в полных именах, которые предписывает:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-189">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="2f6bd-190">двузначные акронимы и сокращений именуются в верхнем регистре (например, `BE` для «Big-endian»),</span><span class="sxs-lookup"><span data-stu-id="2f6bd-190">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="2f6bd-191">все более длинные акронимы и сокращений именуются в `CamelCase` (например, `Qft` для "преобразования в тактовую Фурье").</span><span class="sxs-lookup"><span data-stu-id="2f6bd-191">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="2f6bd-192">Таким образом, операция, реализующая Кфт, может быть либо вызвана `QFT` как краткая, либо записана как `ApplyQft` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-192">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="2f6bd-193">Для наиболее часто используемых операций и функций может быть желательно предоставить сокращенное имя в качестве _псевдонима_ для более длинной формы:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-193">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-194">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-194">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-195">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-195">We suggest:</span></span>

- <span data-ttu-id="2f6bd-196">При необходимости рекомендуется использовать распространенные и распространенные сокращенные имена.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-196">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="2f6bd-197">Для сокращения используйте прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-197">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="2f6bd-198">Используйте прописные буквы для коротких (двух букв) аббревиатур и сокращений.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-198">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="2f6bd-199">Используйте `CamelCase` более длинные (три и более буквы) акронимы и сокращений.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-199">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-200">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-200">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="2f6bd-201">Имя</span><span class="sxs-lookup"><span data-stu-id="2f6bd-201">Name</span></span> | <span data-ttu-id="2f6bd-202">Описание</span><span class="sxs-lookup"><span data-stu-id="2f6bd-202">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="2f6bd-203">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-203">☑</span></span> | `X` | <span data-ttu-id="2f6bd-204">Хорошо понятная Краткая форма "применение преобразования $X $"</span><span class="sxs-lookup"><span data-stu-id="2f6bd-204">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="2f6bd-205">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-205">☑</span></span> | `CNOT` | <span data-ttu-id="2f6bd-206">Хорошо понятная Краткая форма для «контролируемых»</span><span class="sxs-lookup"><span data-stu-id="2f6bd-206">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="2f6bd-207">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-207">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="2f6bd-208">Сокращенная форма не должна находиться в `CamelCase` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-208">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="2f6bd-209">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-209">☑</span></span> | `ApplyQft` | <span data-ttu-id="2f6bd-210">Общий начальный вид "Кфт" отображается как часть имени длинной формы.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-210">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="2f6bd-211">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-211">☑</span></span> | `QFT` | <span data-ttu-id="2f6bd-212">Общий начальный вид "Кфт" отображается как часть сокращенного имени.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-212">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



***


### <a name="proper-nouns-in-names"></a><span data-ttu-id="2f6bd-213">Собственные существительные в именах</span><span class="sxs-lookup"><span data-stu-id="2f6bd-213">Proper Nouns in Names</span></span> ###

<span data-ttu-id="2f6bd-214">Хотя в физике мы часто называете вещи, когда первый пользователь публикует их, большинство фисиЦистс не знакомы с именами всех участников и журналами.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-214">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="2f6bd-215">Чрезмерная постановка в соглашениях об именовании от физикы может привести к значительному барьеру в записи, так как пользователи из других фоновых рисунков должны изучить большое количество непрозрачных имен, чтобы использовать общие операции и концепции.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-215">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="2f6bd-216">Таким образом, рекомендуется, чтобы при разумных принципах обычные существительные, описывающие концепцию, были приняты строгими для правильного существительных, описывающих историю публикации концепции.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-216">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="2f6bd-217">В качестве конкретного примера, контролируемые с помощью управляемой операции переключения и удвоения часто называются операциями "Фредкин" и "Тоффоли" в учебных литературах, но они определяются в Q # преимущественно как `CSWAP` и `CCNOT` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-217">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in Q# primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="2f6bd-218">В обоих случаях комментарии к документации по API предоставляют имена синонимов на основе правильных существительных, а также все соответствующие ссылки.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-218">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="2f6bd-219">Этот приоритет особенно важен в тех случаях, когда необходимо всегда использовать собственные существительные: Q # соответствует традицию, заданному многими классическими языками, и ссылается на `Bool` типы в ссылке на логическую логику, которая в свою очередь имеет имя, соблюдающая bool.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-219">This preference is especially important given that some usage of proper nouns will always be necessary — Q# follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="2f6bd-220">Несколько концепций такта аналогичным образом именуются, включая `Pauli` тип, встроенный в язык Q #.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-220">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the Q# language.</span></span>
<span data-ttu-id="2f6bd-221">Свести к минимуму использование правильных существительных, если такое использование не является обязательным, мы уменьшаем влияние того, что их не удается избежать.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-221">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-222">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-222">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="2f6bd-223">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-223">We suggest:</span></span>

- <span data-ttu-id="2f6bd-224">Избегайте использования в именах правильных существительных.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-224">Avoid the use of proper nouns in names.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-225">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-225">Examples</span></span>](#tab/examples)

***

### <a name="type-conversions"></a><span data-ttu-id="2f6bd-226">Преобразования типов</span><span class="sxs-lookup"><span data-stu-id="2f6bd-226">Type Conversions</span></span> ###

<span data-ttu-id="2f6bd-227">Поскольку Q # является строго и статически типизированным языком, значение одного типа может использоваться только как значение другого типа с помощью явного вызова функции преобразования типа.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-227">Since Q# is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="2f6bd-228">Это отличается от языков, позволяющих неявным образом изменять типы значений (например, повышение типа) или путем приведения.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-228">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="2f6bd-229">В результате функции преобразования типов играют важную роль в вопросах разработки библиотеки Q # и составляют одно из наиболее часто встречающихся решений по именованию.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-229">As a result, type conversion functions play an important role in Q# library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="2f6bd-230">Однако обратите внимание, что поскольку преобразования типов всегда _детерминированы_, они могут быть написаны как функции и, таким образом, находиться на приведенный выше Совет.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-230">We note, however, that since type conversions are always _deterministic_, they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="2f6bd-231">В частности, мы советуем, что функции преобразования типов никогда не должны называться как глаголы (например, `ConvertToX` ) или модификаторовные фразы ( `ToX` ), но они должны называться как прилагательные фразы, указывающие исходный и целевой типы ( `XAsY` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-231">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="2f6bd-232">При перечислении типов массивов в именах функций преобразования типов рекомендуется использовать краткую форму `Arr` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-232">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="2f6bd-233">При запрете исключительных обстоятельств рекомендуется, чтобы все функции преобразования типов были именованы с помощью, `As` чтобы их можно было быстро определить.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-233">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-234">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-234">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-235">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-235">We suggest:</span></span>

- <span data-ttu-id="2f6bd-236">Если функция преобразует значение типа `X` в значение типа `Y` , используйте либо имя, `AsY` либо `XAsY` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-236">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-237">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-237">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="2f6bd-238">Имя</span><span class="sxs-lookup"><span data-stu-id="2f6bd-238">Name</span></span> | <span data-ttu-id="2f6bd-239">Описание</span><span class="sxs-lookup"><span data-stu-id="2f6bd-239">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="2f6bd-240">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-240">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="2f6bd-241">В качестве отстановки "до" задается Командная фраза, указывающая на операцию, а не на функцию.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-241">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="2f6bd-242">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-242">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="2f6bd-243">Тип входных данных не является понятным по имени функции.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-243">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="2f6bd-244">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-244">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="2f6bd-245">Входные и выходные типы отображаются в неправильном порядке.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-245">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="2f6bd-246">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-246">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="2f6bd-247">Типы входных и выходных данных являются четкими.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-247">Both the input types and output types are clear.</span></span> |

***

### <a name="private-or-internal-names"></a><span data-ttu-id="2f6bd-248">Частные или внутренние имена</span><span class="sxs-lookup"><span data-stu-id="2f6bd-248">Private or Internal Names</span></span> ###

<span data-ttu-id="2f6bd-249">Во многих случаях имя предназначено исключительно для внутреннего использования в библиотеке или проекте и не является гарантированной частью API, предоставляемой библиотекой.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-249">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="2f6bd-250">Полезно четко указать, что это происходит при именовании функций и операций, так что случайные зависимости от внутреннего кода становятся очевидными.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-250">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="2f6bd-251">Если операция или функция не предназначена для непосредственного использования, а должна использоваться соответствующим вызываемым методом, который действует частичным приложением, рассмотрите возможность использования имени, начинающегося с, `_` для частично примененного вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-251">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with `_` for the callable that is partially applied.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-252">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-252">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-253">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-253">We suggest:</span></span>

- <span data-ttu-id="2f6bd-254">Если функция, операция или определяемый пользователем тип не являются частью общедоступного API для библиотеки или программы Q #, убедитесь, что ее имя начинается с символа подчеркивания ( `_` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-254">When a function, operation, or user-defined type is not a part of the public API for a Q# library or program, ensure that its name begins with a leading underscore (`_`).</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-255">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-255">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="2f6bd-256">Имя</span><span class="sxs-lookup"><span data-stu-id="2f6bd-256">Name</span></span> | <span data-ttu-id="2f6bd-257">Описание</span><span class="sxs-lookup"><span data-stu-id="2f6bd-257">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="2f6bd-258">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-258">☒</span></span> | <s>`ApplyDecomposedOperation_`</s> | <span data-ttu-id="2f6bd-259">Символ подчеркивания `_` не должен располагаться в конце имени.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-259">The underscore `_` should not appear at the end of the name.</span></span> |
| <span data-ttu-id="2f6bd-260">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-260">☑</span></span> | `_ApplyDecomposedOperation` | <span data-ttu-id="2f6bd-261">Символ подчеркивания `_` в начале ясно указывает, что эта операция предназначена только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-261">The underscore `_` at the beginning clearly indicates that this operation is for internal use only.</span></span> |

***

### <a name="variants"></a><span data-ttu-id="2f6bd-262">Варианты</span><span class="sxs-lookup"><span data-stu-id="2f6bd-262">Variants</span></span> ###

<span data-ttu-id="2f6bd-263">Хотя это ограничение может не сохраняться в будущих версиях Q #, в настоящее время существует ситуация, когда часто встречаются группы связанных операций или функций, которые различаются операторов их входными данными, или конкретными типами их аргументов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-263">Though this limitation may not persist in future versions of Q#, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="2f6bd-264">Эти группы можно отличать с помощью одного и того же корневого имени, за которым следует одна или две буквы, указывающие на вариант.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-264">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="2f6bd-265">Суффикс</span><span class="sxs-lookup"><span data-stu-id="2f6bd-265">Suffix</span></span> | <span data-ttu-id="2f6bd-266">Значение</span><span class="sxs-lookup"><span data-stu-id="2f6bd-266">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="2f6bd-267">Ожидается ввод для поддержки`Adjoint`</span><span class="sxs-lookup"><span data-stu-id="2f6bd-267">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="2f6bd-268">Ожидается ввод для поддержки`Controlled`</span><span class="sxs-lookup"><span data-stu-id="2f6bd-268">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="2f6bd-269">Ожидается ввод для поддержки `Controlled` и`Adjoint`</span><span class="sxs-lookup"><span data-stu-id="2f6bd-269">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="2f6bd-270">Входные или входные данные имеют тип`Int`</span><span class="sxs-lookup"><span data-stu-id="2f6bd-270">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="2f6bd-271">Входные или входные данные имеют тип`Double`</span><span class="sxs-lookup"><span data-stu-id="2f6bd-271">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="2f6bd-272">Входные или входные данные имеют тип`BigInt`</span><span class="sxs-lookup"><span data-stu-id="2f6bd-272">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-273">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-273">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-274">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-274">We suggest:</span></span>

- <span data-ttu-id="2f6bd-275">Если функция или операция не связаны с аналогичными функциями или операциями по типам и функтор поддерживают свои входные данные, не используйте суффикс.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-275">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="2f6bd-276">Если функция или операция связана с любыми аналогичными функциями или операциями типов и функтор поддержки своих входных данных, используйте суффиксы, как показано в таблице выше, чтобы различать варианты.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-276">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-277">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-277">Examples</span></span>](#tab/examples)

***

### <a name="arguments-and-variables"></a><span data-ttu-id="2f6bd-278">Аргументы и переменные</span><span class="sxs-lookup"><span data-stu-id="2f6bd-278">Arguments and Variables</span></span> ###

<span data-ttu-id="2f6bd-279">Ключевой целью кода Q # для функции или операции является простое чтение и понимание.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-279">A key goal of the Q# code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="2f6bd-280">Аналогичным образом, имена входов и аргументов типа должны сообщать, как функция или аргумент будут использоваться по мере того, как они предоставлены.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-280">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="2f6bd-281">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-281">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-282">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-282">We suggest:</span></span>

- <span data-ttu-id="2f6bd-283">Для всех переменных и входных имен используйте `pascalCase` строгое предпочтение в `CamelCase` , `snake_case` или `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-283">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="2f6bd-284">Входные имена должны быть описательными; по возможности избегайте по одному или двум именам букв.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-284">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="2f6bd-285">Операции и функции, принимающие ровно один аргумент типа, должны отметить этот аргумент типа, `T` если его роль очевидна.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-285">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="2f6bd-286">Если функция или операция принимает несколько аргументов типа или если роль одного аргумента типа не очевидна, рассмотрите возможность использования короткого слова с прописной буквой, которое предшествует `T` (например, `TOutput` ) для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-286">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="2f6bd-287">Не включайте имена типов в имена аргументов и переменных. Эти сведения могут и должны предоставляться средой разработки.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-287">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="2f6bd-288">Запишите скалярные типы по их литеральным именам ( `flagQubit` ) и типам массивов во множественном числе ( `measResults` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-288">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="2f6bd-289">Для массивов Кубитс в частности, рассмотрите такие типы, в `Register` которых имя ссылается на последовательность Кубитс, тесно связанных каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-289">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="2f6bd-290">Переменные, используемые в качестве индексов в массивах, должны начинаться с `idx` и должны быть в единственном числе, например: `things[idxThing]` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-290">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="2f6bd-291">В частности, настоятельно рекомендуется избегать использования однобуквенных имен переменных в качестве индексов; рекомендуется использовать `idx` как минимум.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-291">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="2f6bd-292">Переменные, используемые для хранения длин массивов, должны начинаться с `n` и должны быть в множественном числе, например: `nThings` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-292">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-293">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-293">Examples</span></span>](#tab/examples)

***

### <a name="user-defined-type-named-items"></a><span data-ttu-id="2f6bd-294">Определяемый пользователем тип с именем Items</span><span class="sxs-lookup"><span data-stu-id="2f6bd-294">User Defined Type Named Items</span></span> ###

<span data-ttu-id="2f6bd-295">Именованные элементы в определяемых пользователем типах должны называться как `CamelCase` , даже при вводе в конструкторы определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-295">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="2f6bd-296">Это помогает в четком разделении именованных элементов со ссылок на переменные в локальной области при использовании представления метода доступа (например, `callable::Apply` ) или нотации копирования и обновления ( `set arr w/= Data <- newData` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-296">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-297">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-297">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-298">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-298">We suggest:</span></span>

- <span data-ttu-id="2f6bd-299">Именованные элементы в конструкторах определяемых пользователем типов должны называться как `CamelCase` ; то есть должны начинаться с прописной буквы.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-299">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="2f6bd-300">Именованные элементы, которые разрешаются в операции, должны называться этапами глагола.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-300">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="2f6bd-301">Именованные элементы, которые не разрешаются в операции, должны называться как субстантивные словосочетания.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-301">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="2f6bd-302">Для определяемых пользователем типов, которые обносят операции, необходимо определить один именованный элемент `Apply` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-302">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-303">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-303">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="2f6bd-304">Фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="2f6bd-304">Snippet</span></span> | <span data-ttu-id="2f6bd-305">Описание</span><span class="sxs-lookup"><span data-stu-id="2f6bd-305">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="2f6bd-306">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-306">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="2f6bd-307">Имя `Apply` является `CamelCase` фразой-командой, предлагающей, что именованный элемент является операцией.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-307">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="2f6bd-308">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-308">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="2f6bd-309">Именованные элементы должны начинаться с первой прописной буквы.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-309">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="2f6bd-310">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-310">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="2f6bd-311">Именованные элементы, которые разрешаются в функции, должны называться как субстантивные словосочетания, а не как фразы глагола.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-311">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

***

## <a name="input-conventions"></a><span data-ttu-id="2f6bd-312">Соглашения о входе</span><span class="sxs-lookup"><span data-stu-id="2f6bd-312">Input Conventions</span></span> ##

<span data-ttu-id="2f6bd-313">Когда разработчик обращается к операции или функции, различные входные данные этой операции или функции должны быть указаны в определенном порядке, увеличивая при этом функциональную нагрузку, которую разработчик может использовать для создания библиотеки.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-313">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="2f6bd-314">В частности, задача по запоминанию порядка входных данных часто является отправной задачей: программированием реализации алгоритма такта.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-314">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="2f6bd-315">Хотя широкая поддержка интегрированной среды разработки может снизить это до большого экстента, хорошая разработка и соблюдение общих соглашений также может помочь минимизировать неудачную загрузку, наложенную API.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-315">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="2f6bd-316">Там, где это возможно, может быть полезно уменьшить количество входных данных, ожидаемых операцией или функцией, чтобы роль каждого входа была более очевидна для разработчиков, обращающихся к этой операции или функции, а также для разработчиков, считывающих этот код позже.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-316">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="2f6bd-317">Особенно если невозможно или разумно уменьшить число аргументов для операции или функции, важно иметь единообразный порядок, позволяющий свести к сведению, что пользователь сталкивается с прогнозированием порядка входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-317">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="2f6bd-318">Мы рекомендуем использовать соглашения о порядке ввода, которые во многом наследуют от мышления частичного приложения как обобщение карринг f (x, y) ≡ f (x) (y).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-318">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="2f6bd-319">Таким образом, частичное применение первых аргументов должно привести к вызову, который будет полезен при любом разумном использовании.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-319">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="2f6bd-320">Следуя этому принципу, рассмотрите возможность использования следующего порядка аргументов:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-320">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="2f6bd-321">Классические не вызываемые аргументы, такие как углы, векторы степеней и т. д.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-321">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="2f6bd-322">Вызываемые аргументы (функции и аргументы).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-322">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="2f6bd-323">Если обе функции и операции выполняются в качестве аргументов, попробуйте разместить операции после функций.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-323">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="2f6bd-324">Коллекции, обрабатываемые вызываемыми аргументами аналогично методу `Map` , `Iter` , `Enumerate` и `Fold` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-324">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="2f6bd-325">Аргументы кубит, используемые в качестве элементов управления.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-325">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="2f6bd-326">Аргументы кубит, используемые в качестве целевых объектов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-326">Qubit arguments used as targets.</span></span>

<span data-ttu-id="2f6bd-327">Рассмотрим операцию `ApplyPhaseEstimationIteration` для использования в оценке этапа, которая принимает угол и Oracle, передает угол `Rz` , измененный массивом различных факторов масштабирования, а затем управляет приложениями Oracle.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-327">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="2f6bd-328">Мы будем упорядочивать входные данные `ApplyPhaseEstimationIteration` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-328">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

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
<span data-ttu-id="2f6bd-329">В качестве особого случая минимизации неожиданности некоторые функции и операции воспроизводят поведение встроенных операторов `Adjoint` и `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-329">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="2f6bd-330">Например, `ControlledOnInt<'T>` имеет тип `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` , который `ControlledOnInt<Qubit[]>(5, _)` действует как `Controlled` функтор, но в условии, что регистр элемента управления представляет состояние $ \кет {5} = \кет {101} $.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-330">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="2f6bd-331">Таким образом, разработчику требуется, чтобы входные данные `ControlledOnInt` были преобразованы последними, а Результирующая операция принимает в качестве входных данных `(Qubit[], 'T)` ---том же порядке, в котором следуют выходные данные `Controlled` функтор.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-331">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-332">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-332">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-333">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-333">We suggest:</span></span>

- <span data-ttu-id="2f6bd-334">Используйте порядок ввода в соответствии с использованием частичного приложения.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-334">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="2f6bd-335">Используйте порядок ввода в соответствии со встроенными операторов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-335">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="2f6bd-336">Разместите все классические входные данные перед любыми входными тактовыми тактами.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-336">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-337">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-337">Examples</span></span>](#tab/examples)

***

## <a name="documentation-conventions"></a><span data-ttu-id="2f6bd-338">Обозначения в документации</span><span class="sxs-lookup"><span data-stu-id="2f6bd-338">Documentation Conventions</span></span> ##

<span data-ttu-id="2f6bd-339">Язык Q # позволяет прикреплять документацию к операциям, функциям и определяемым пользователем типам с помощью специально отформатированных комментариев к документации.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-339">The Q# language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="2f6bd-340">В соответствии с тройными косыми чертами ( `///` ) эти комментарии документации представляют собой небольшие [DocFX документы Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) , которые можно использовать для описания назначения каждой операции, функции и определяемого пользователем типа, возвращаемых входов и т. д.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-340">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="2f6bd-341">Компилятор, поставляемый с пакетом разработки тактов, извлекает эти комментарии и использует их для помощи в документации по наборам типов, похожим на эту https://docs.microsoft.com/quantum .</span><span class="sxs-lookup"><span data-stu-id="2f6bd-341">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="2f6bd-342">Аналогичным образом, языковой сервер, поставляемый с пакетом разработки тактовой передачи, использует эти комментарии для предоставления помощи пользователям при наведении указателя мыши на символы в коде Q #.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-342">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their Q# code.</span></span>
<span data-ttu-id="2f6bd-343">Использование комментариев к документации может помочь пользователям лучше понять код, предоставляя полезную ссылку для получения подробных сведений, которые не просто выражаются с помощью других соглашений в этом документе.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-343">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

<div class="nextstepaction"><span data-ttu-id="2f6bd-344">
    [Справочник по синтаксису комментариев документации](xref:microsoft.quantum.guide.filestructure#documentation-comments)
</span><span class="sxs-lookup"><span data-stu-id="2f6bd-344">
    [Documentation comment syntax reference](xref:microsoft.quantum.guide.filestructure#documentation-comments)
</span></span></div>

<span data-ttu-id="2f6bd-345">Чтобы эффективно использовать эту функцию для пользователей, рекомендуется учитывать некоторые моменты при написании комментариев к документации.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-345">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-346">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-346">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="2f6bd-347">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-347">We suggest:</span></span>

- <span data-ttu-id="2f6bd-348">Каждая открытая функция, операция и определяемый пользователем тип должны непосредственно предшествовать комментарию документации.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-348">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="2f6bd-349">Каждый комментарий к документации должен содержать как минимум следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-349">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="2f6bd-350">Сводка</span><span class="sxs-lookup"><span data-stu-id="2f6bd-350">Summary</span></span>
    - <span data-ttu-id="2f6bd-351">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2f6bd-351">Input</span></span>
    - <span data-ttu-id="2f6bd-352">Выходные данные (если применимо)</span><span class="sxs-lookup"><span data-stu-id="2f6bd-352">Output (if applicable)</span></span>
- <span data-ttu-id="2f6bd-353">Убедитесь, что все сводки имеют два предложения или меньше.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-353">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="2f6bd-354">Если требуется больше места, укажите раздел, `# Description` приведенный сразу за `# Summary` полными сведениями.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-354">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="2f6bd-355">В разумных случаях не включайте математические вычисления в сводки, так как не все клиенты поддерживают да нотацию в сводках.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-355">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="2f6bd-356">Обратите внимание, что при написании документов prose (например, да или Markdown) может быть предпочтительнее использовать более длинные строки.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-356">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="2f6bd-357">Укажите все соответствующие математические выражения в `# Description` разделе.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-357">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="2f6bd-358">При описании входных данных не следует повторять типы всех входных данных, так как они могут выводиться компилятором и угрожать несогласованность.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-358">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="2f6bd-359">Укажите нужные примеры, каждый в отдельном `# Example` разделе.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-359">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="2f6bd-360">Кратко опишите каждый пример перед выводом кода.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-360">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="2f6bd-361">В разделе представлены все соответствующие академические публикации (например, документы, материалы, записи в блоге и альтернативные реализации) `# References` раздела в виде маркированного списка ссылок.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-361">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="2f6bd-362">Убедитесь, что, где это возможно, все ссылки ссылок относятся к постоянным и неизменяемым идентификаторам (Доис или номера Арксив версий).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-362">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="2f6bd-363">Если операция или функция связана с другими операциями или функциями с помощью функтор Variant, перечислите другие варианты в виде маркеров в `# See Also` разделе.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-363">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="2f6bd-364">Оставьте пустую строку комментария между разделами уровня 1 ( `/// #` ), но не оставляйте пустых строк между разделами уровня 2 ( `/// ##` ).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-364">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-365">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-365">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="2f6bd-366">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-366">☑</span></span> ####

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

## <a name="formatting-conventions"></a><span data-ttu-id="2f6bd-367">Соглашения о форматировании</span><span class="sxs-lookup"><span data-stu-id="2f6bd-367">Formatting Conventions</span></span> ##

<span data-ttu-id="2f6bd-368">Помимо описанных выше предложений, рекомендуется сделать код максимально удобочитаемым, чтобы использовать единообразные правила форматирования.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-368">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="2f6bd-369">Такие правила форматирования по сути, как правило, являются несколько произвольными и хорошо эстетичность.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-369">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="2f6bd-370">Тем не менее рекомендуется поддерживать единообразный набор соглашений о форматировании в группе участников совместной работы, особенно для больших проектов Q #, таких как сам пакет разработки такта.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-370">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large Q# projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="2f6bd-371">Эти правила могут быть автоматически применены с помощью средства форматирования, интегрированного с компилятором Q #.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-371">These rules can be automatically applied by using the formatting tool integrated with the Q# compiler.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="2f6bd-372">Руководство</span><span class="sxs-lookup"><span data-stu-id="2f6bd-372">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="2f6bd-373">Мы рекомендуем:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-373">We suggest:</span></span>

- <span data-ttu-id="2f6bd-374">Для переносимости используйте четыре пробела вместо вкладок.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-374">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="2f6bd-375">Например, в VS Code:</span><span class="sxs-lookup"><span data-stu-id="2f6bd-375">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="2f6bd-376">Строка переносится в 79 символов, где это оправданно.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-376">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="2f6bd-377">Используйте пробелы вокруг бинарных операторов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-377">Use spaces around binary operators.</span></span>
- <span data-ttu-id="2f6bd-378">Используйте пробелы с обеих сторон двоеточий, используемых для заметок типов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-378">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="2f6bd-379">Используйте один пробел после запятых, используемых в массивах и литералах кортежа (например, в входных данных для функций и операций).</span><span class="sxs-lookup"><span data-stu-id="2f6bd-379">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="2f6bd-380">Не используйте пробелы после имени функции, операции или определяемого пользователем типа или после `@` объявлений атрибута in.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-380">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="2f6bd-381">Каждое объявление атрибута должно располагаться в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-381">Each attribute declaration should be on its own line.</span></span>

# <a name="examples"></a>[<span data-ttu-id="2f6bd-382">Примеры</span><span class="sxs-lookup"><span data-stu-id="2f6bd-382">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="2f6bd-383">Фрагмент кода</span><span class="sxs-lookup"><span data-stu-id="2f6bd-383">Snippet</span></span> | <span data-ttu-id="2f6bd-384">Описание</span><span class="sxs-lookup"><span data-stu-id="2f6bd-384">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="2f6bd-385">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-385">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="2f6bd-386">Используйте пробелы вокруг бинарных операторов.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-386">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="2f6bd-387">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-387">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="2f6bd-388">Используйте пробелы вокруг заметок типа двоеточия.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-388">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="2f6bd-389">☑</span><span class="sxs-lookup"><span data-stu-id="2f6bd-389">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="2f6bd-390">Элементы во входном кортеже имеют правильный размер для удобочитаемости.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-390">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="2f6bd-391">☒</span><span class="sxs-lookup"><span data-stu-id="2f6bd-391">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="2f6bd-392">Пробелы следует подавлять после имени функции, операции или определяемого пользователем типа.</span><span class="sxs-lookup"><span data-stu-id="2f6bd-392">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

***

