---
title: Участвующий код | Документация Майкрософт
description: Участвующий код
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.code
ms.openlocfilehash: f9e0f0d9540102331aea64a1245cbaa4833e1e02
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819966"
---
# <a name="contributing-code"></a><span data-ttu-id="f37b2-103">Участие в написании кода</span><span class="sxs-lookup"><span data-stu-id="f37b2-103">Contributing Code</span></span> #

<span data-ttu-id="f37b2-104">Помимо составления отчетов о проблемах и улучшения документации, Добавление кода в пакет разработки тактов может быть очень прямым способом помочь вашим коллегам в сообществе разработчиков тактов.</span><span class="sxs-lookup"><span data-stu-id="f37b2-104">In addition to reporting issues and improving documentation, contributing code to the Quantum Development Kit can be a very direct way to help your peers in the quantum programming community.</span></span>
<span data-ttu-id="f37b2-105">Добавив код, вы можете помочь устранить проблемы, предоставить новые примеры, упростить использование существующих библиотек или даже добавить совершенно новые функции.</span><span class="sxs-lookup"><span data-stu-id="f37b2-105">By contributing code, you can help to fix issues, provide new examples, make existing libraries easier to use, or even add entirely new features.</span></span>

<span data-ttu-id="f37b2-106">В этом пошаговом окне мы подробно рассмотрим, что мы будем искать при просмотре запросов на вытягивание, чтобы помочь вашему участию.</span><span class="sxs-lookup"><span data-stu-id="f37b2-106">In this guide, we'll detail a bit of what we look for when we review pull requests to help your contribution do the most good.</span></span>

## <a name="what-we-look-for"></a><span data-ttu-id="f37b2-107">Что мы будем искать</span><span class="sxs-lookup"><span data-stu-id="f37b2-107">What We Look For</span></span> ##

<span data-ttu-id="f37b2-108">Идеальная публикация кода основана на существующей работе в репозитории пакета разработки такта для устранения проблем, расширения существующих функций или добавления новых функций, которые находятся в области репозитория.</span><span class="sxs-lookup"><span data-stu-id="f37b2-108">An ideal code contribution builds on the existing work in a Quantum Development Kit repository to fix issues, expand existing features, or to add new features that are within the scope of a repository.</span></span>
<span data-ttu-id="f37b2-109">Принимая участие в написании кода, он становится частью самого пакета разработки такта, поэтому новые функции будут выпущены, сохранены и разработаны так же, как и остальные компоненты пакета разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="f37b2-109">When we accept a code contribution, it becomes a part of the Quantum Development Kit itself, such that new features will be released, maintained, and developed in the same way as the rest of the Quantum Development Kit.</span></span>
<span data-ttu-id="f37b2-110">Таким образом, это полезно при тщательном тестировании функциональности, добавленной в публикацию, и документированной.</span><span class="sxs-lookup"><span data-stu-id="f37b2-110">Thus, it is helpful when functionality added by a contribution is well-tested and is documented.</span></span>

### <a name="unit-tests"></a><span data-ttu-id="f37b2-111">Модульные тесты</span><span class="sxs-lookup"><span data-stu-id="f37b2-111">Unit Tests</span></span> ###

<span data-ttu-id="f37b2-112">Функции Q #, операции и определяемые пользователем типы, составляющие библиотеки, такие как Canon, автоматически тестируются как часть разработки в репозитории [**Microsoft/куантумлибрариес**](https://github.com/Microsoft/QuantumLibraries/) .</span><span class="sxs-lookup"><span data-stu-id="f37b2-112">The Q# functions, operations, and user-defined types that make up libraries such as the canon are automatically tested as a part of development on the [**Microsoft/QuantumLibraries**](https://github.com/Microsoft/QuantumLibraries/) repository.</span></span>
<span data-ttu-id="f37b2-113">Например, при открытии нового запроса на вытягивание [Azure pipelines](https://azure.microsoft.com/services/devops/pipelines/) конфигурация будет проверять, что изменения в запросе на вытягивание не нарушают существующие функциональные возможности, от которых зависит сообщество программирования тактов.</span><span class="sxs-lookup"><span data-stu-id="f37b2-113">When a new pull request is opened, for instance, our [Azure Pipelines](https://azure.microsoft.com/services/devops/pipelines/) configuration will check that the changes in the pull request do not break any existing functionality that the quantum programming community depends on.</span></span>

<span data-ttu-id="f37b2-114">С последней версией Q # модульный тест определяется с помощью атрибута `@Test("QuantumSimulator")`.</span><span class="sxs-lookup"><span data-stu-id="f37b2-114">With the latest Q# version, unit test are defined using the `@Test("QuantumSimulator")` attribute.</span></span> <span data-ttu-id="f37b2-115">Аргумент может иметь значение "Куантумсимулатор", "Тоффолисимулатор", "Трацесимулатор" или любое полное имя, указывающее цель выполнения.</span><span class="sxs-lookup"><span data-stu-id="f37b2-115">The argument may be either "QuantumSimulator", "ToffoliSimulator", "TraceSimulator", or any fully qualified name specifying the execution target.</span></span> <span data-ttu-id="f37b2-116">Несколько атрибутов, определяющих различные цели выполнения, могут быть присоединены к одному и тому же вызываемому объекту.</span><span class="sxs-lookup"><span data-stu-id="f37b2-116">Several attributes defining different execution targets may be attached to the same callable.</span></span> <span data-ttu-id="f37b2-117">Некоторые из наших тестов по-прежнему используют устаревший пакет [Microsoft. тактов. xUnit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) , который предоставляет все функции и операции Q #, которые заканчиваются на `Test` Framework [xUnit](https://xunit.github.io/) .</span><span class="sxs-lookup"><span data-stu-id="f37b2-117">Some of our tests still use the deprecated [Microsoft.Quantum.Xunit](https://www.nuget.org/packages/Microsoft.Quantum.Xunit/) package that exposes all Q# functions and operations ending in `Test` to the [xUnit](https://xunit.github.io/) framework.</span></span> <span data-ttu-id="f37b2-118">Этот пакет больше не требуется для определения модульных тестов.</span><span class="sxs-lookup"><span data-stu-id="f37b2-118">This package is no longer needed for defining unit tests.</span></span> 

<span data-ttu-id="f37b2-119">Следующая функция используется для того, чтобы функции <xref:microsoft.quantum.canon.fst> и <xref:microsoft.quantum.canon.snd> возвращали правильные выходные данные в репрезентативном примере.</span><span class="sxs-lookup"><span data-stu-id="f37b2-119">The following function is used to ensure that the <xref:microsoft.quantum.canon.fst> and <xref:microsoft.quantum.canon.snd> functions both return the right outputs in a representative example.</span></span>
<span data-ttu-id="f37b2-120">Если выходные данные `Fst` или `Snd` неверны, используется инструкция `fail`, которая приводит к сбою теста.</span><span class="sxs-lookup"><span data-stu-id="f37b2-120">If the output of `Fst` or `Snd` is incorrect, the `fail` statement is used to cause the test to fail.</span></span>

```qsharp
@Test("QuantumSimulator")
function PairTest () : Unit {
    let pair = (12, PauliZ);

    if (Fst(pair) != 12) {
        let actual = Fst(pair);
        fail $"Expected 12, actual {actual}.";
    }

    if (Snd(pair) != PauliZ) {
        let actual = Snd(pair);
        fail $"Expected PauliZ, actual {actual}.";
    }
}
```

<span data-ttu-id="f37b2-121">Более сложные условия можно проверить с помощью методик, описанных в [разделе "тестирование](xref:microsoft.quantum.libraries.diagnostics) " в руководству стандартных библиотек.</span><span class="sxs-lookup"><span data-stu-id="f37b2-121">More complicated conditions can be checked using the techniques in the [testing section](xref:microsoft.quantum.libraries.diagnostics) of the standard libraries guide.</span></span>
<span data-ttu-id="f37b2-122">Например, следующий тест проверяет, что `H(q); X(q); H(q);`, как вызвано <xref:microsoft.quantum.canon.applywith>, выполняет то же самое, что и `Z(q)`.</span><span class="sxs-lookup"><span data-stu-id="f37b2-122">For instance, the following test checks that `H(q); X(q); H(q);` as called by <xref:microsoft.quantum.canon.applywith> does the same thing as `Z(q)`.</span></span>

```qsharp
@Test("QuantumSimulator")
operation TestApplyWith() : Unit {
    let actual = ApplyWith(H, X, _);
    let expected = Z;
    AssertOperationsEqualReferenced(ApplyToEach(actual, _), ApplyToEachA(expected, _), 4);
}
```

<span data-ttu-id="f37b2-123">При добавлении новых функций рекомендуется также добавить новые тесты, чтобы убедиться, что ваша публикация делает то, что он должен.</span><span class="sxs-lookup"><span data-stu-id="f37b2-123">When adding new features, it's a good idea to also add new tests to make sure that your contribution does what it's supposed to.</span></span>
<span data-ttu-id="f37b2-124">Это помогает остальным участникам сообщества поддерживать и разрабатывать свои функции, и в частности помогает другим разработчикам понять, что они могут полагаться на вашу функцию.</span><span class="sxs-lookup"><span data-stu-id="f37b2-124">This helps the rest of the community to maintain and develop your feature, and in particular helps other developers know that they can rely on your feature.</span></span>

> [!NOTE]
> <span data-ttu-id="f37b2-125">Это работает и в других случаях.</span><span class="sxs-lookup"><span data-stu-id="f37b2-125">This works the other way around, too!</span></span>
> <span data-ttu-id="f37b2-126">Если у вас есть функция, которая не содержит некоторых тестов, мы можем добавить покрытие тестирования, чтобы сделать его полезным для сообщества.</span><span class="sxs-lookup"><span data-stu-id="f37b2-126">If there's an existing feature that's missing some tests, helping us add test coverage would make a great contribution to the community.</span></span>

<span data-ttu-id="f37b2-127">Модульные тесты можно выполнять локально, с помощью обозревателя тестов Visual Studio или команды `dotnet test`, чтобы можно было проверить публикацию перед открытием запроса на вытягивание.</span><span class="sxs-lookup"><span data-stu-id="f37b2-127">Locally, unit tests can be run using the Visual Studio Test Explorer or the `dotnet test` command, so that you can check your contribution before opening up a pull request.</span></span>

<!-- TODO:
### Comments and Documentation ###

### Citations and References ### -->

## <a name="when-well-reject-a-pull-request"></a><span data-ttu-id="f37b2-128">Когда мы отклоним запрос на вытягивание</span><span class="sxs-lookup"><span data-stu-id="f37b2-128">When We'll Reject a Pull Request</span></span> ##

<span data-ttu-id="f37b2-129">Иногда мы отклоним запрос на вытягивание для вклада.</span><span class="sxs-lookup"><span data-stu-id="f37b2-129">Sometimes, we'll reject the pull request for a contribution.</span></span>
<span data-ttu-id="f37b2-130">Если это произойдет, это не значит, что оно плохо, так как существует ряд причин, по которым мы не можем принять конкретную публикацию.</span><span class="sxs-lookup"><span data-stu-id="f37b2-130">If this happens to you, it doesn't mean that it's bad, as there's a number of reasons why we might not be able to accept a particular contribution.</span></span>
<span data-ttu-id="f37b2-131">Возможно, чаще всего вклад в сообщество по программированию тактов является действительно хорошим, но репозитории комплекта для разработки тактов не подходят для разработки.</span><span class="sxs-lookup"><span data-stu-id="f37b2-131">Perhaps most commonly, a contribution to the quantum programming community is a really good one, but the Quantum Development Kit repositories aren't the right place to develop it.</span></span>
<span data-ttu-id="f37b2-132">В таких случаях мы настоятельно рекомендуем сделать собственный репозиторий---частью надежности пакета средств разработки тактов, что позволяет легко создавать и распространять собственные библиотеки с помощью GitHub и NuGet.org, аналогично распространению Canon и химия библиотеки уже сегодня.</span><span class="sxs-lookup"><span data-stu-id="f37b2-132">In such cases, we strongly encourage you to make your own repository --- part of the strength of the Quantum Development Kit is that it's easy to make and distribute your own libraries using GitHub and NuGet.org, the same way that we distribute the canon and chemistry libraries today.</span></span>

<span data-ttu-id="f37b2-133">В других случаях мы можем отклонить хороший вклад, просто потому, что мы еще не готовы поддерживать и разрабатывать ее.</span><span class="sxs-lookup"><span data-stu-id="f37b2-133">At other times, we may reject a good contribution simply because we aren't yet ready to maintain and develop it.</span></span>
<span data-ttu-id="f37b2-134">Это может быть затруднительно, так что мы планируем, какие функции лучше использовать в качестве стратегии.</span><span class="sxs-lookup"><span data-stu-id="f37b2-134">It can be difficult to do everything, so we plan out what features we're best able to work on as a roadmap.</span></span>
<span data-ttu-id="f37b2-135">Это может быть другой случай, когда возможность выпуска функции в качестве сторонней библиотеки может быть очень осмысленной.</span><span class="sxs-lookup"><span data-stu-id="f37b2-135">This can be another case where releasing a feature as a third-party library can make a lot of sense.</span></span>
<span data-ttu-id="f37b2-136">Кроме того, мы можем попросить помочь вам в изменении функции, чтобы она лучше соответствовала нашему плану, чтобы мы могли выполнить оптимальную работу с ней.</span><span class="sxs-lookup"><span data-stu-id="f37b2-136">Alternatively, we may ask for your help in modifying a feature to better fit into our roadmap so that we can do the best work we can with it.</span></span>

<span data-ttu-id="f37b2-137">Кроме того, мы будем запрашивать изменения в запросе на вытягивание, если ему требуется дополнительная документация или модульные тесты, чтобы помочь нам в его использовании, или, если она достаточно велика в стиле из остальных библиотек Q #, чтобы пользователи не могли найти вашу функцию.</span><span class="sxs-lookup"><span data-stu-id="f37b2-137">We'll also ask for changes to a pull request if it requires more documentation or unit tests to help us make use of it, or if it differs enough in style from the rest of the Q# libraries that it will make it harder for users to find your feature.</span></span>
<span data-ttu-id="f37b2-138">В этих случаях мы попытаемся предложить некоторые рекомендации по проверке кода о том, что можно добавить или изменить, чтобы упростить добавление изменений в публикацию.</span><span class="sxs-lookup"><span data-stu-id="f37b2-138">In these cases, we'll try to offer some advice in code reviews about what can be added or changed to make your contribution easier for us to include.</span></span>

<span data-ttu-id="f37b2-139">Наконец, мы не можем принять вклады, которые могут нанести вред сообществу для вычисления тактовой задержки, как описано в [кодексе поведения Microsoft с открытым исходным кодом](https://opensource.microsoft.com/codeofconduct/).</span><span class="sxs-lookup"><span data-stu-id="f37b2-139">Finally, we cannot accept contributions that cause harm the quantum computing community, as outlined in the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).</span></span>
<span data-ttu-id="f37b2-140">Мы хотим обеспечить, чтобы вклады обслужили все сообщество вычислительных вычислений, как в текущем замечательном разнородном мире, так и в будущем, так как он становится еще более широким.</span><span class="sxs-lookup"><span data-stu-id="f37b2-140">We want to ensure that contributions serve the entire quantum computing community, both in its current wonderful diversity, and in the future as it grows to become still more inclusive.</span></span>
<span data-ttu-id="f37b2-141">Мы ценим вашу помощь в реализации этой цели.</span><span class="sxs-lookup"><span data-stu-id="f37b2-141">We appreciate your help in realizing this goal.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f37b2-142">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f37b2-142">Next steps</span></span> ##

<span data-ttu-id="f37b2-143">Благодарим за помощь в создании пакета разработки такта — отличного ресурса для всего сообщества по программированию на такт!</span><span class="sxs-lookup"><span data-stu-id="f37b2-143">Thanks for helping to make the Quantum Development Kit a great resource for the entire quantum programming community!</span></span>
<span data-ttu-id="f37b2-144">Чтобы узнать больше, перейдите к следующему руководству по стилю Q #.</span><span class="sxs-lookup"><span data-stu-id="f37b2-144">To learn more, please continue with the following guide on Q# style.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="f37b2-145">Дополнительные сведения о рекомендациях по стилю Q #</span><span class="sxs-lookup"><span data-stu-id="f37b2-145">Learn about Q# style guidelines</span></span>](xref:microsoft.quantum.contributing.style)
