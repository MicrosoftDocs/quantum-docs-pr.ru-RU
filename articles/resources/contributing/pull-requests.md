---
title: Открытие запросов на включение внесенных изменений
description: Узнайте, как отправить запрос на вытягивание GitHub, когда вы будете готовы к отправке кода или документации на Microsoft Quantum Development Kit.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.pulls
ms.openlocfilehash: 82af3b5123588cc06882f746ffcb0402ad3f0f2e
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275475"
---
# <a name="opening-pull-requests"></a><span data-ttu-id="3127b-103">Открытие запросов на вытягивание</span><span class="sxs-lookup"><span data-stu-id="3127b-103">Opening Pull Requests</span></span> #

<span data-ttu-id="3127b-104">Вся документация по пакету разработки такта управляется с помощью системы управления версиями Git с помощью нескольких репозиториев, размещенных на GitHub.</span><span class="sxs-lookup"><span data-stu-id="3127b-104">All of the documentation for the Quantum Development Kit is managed using the Git version control system through the use of several repositories hosted on GitHub.</span></span>
<span data-ttu-id="3127b-105">Совместное использование Git и GitHub упрощает совместную работу с пакетом разработки тактов.</span><span class="sxs-lookup"><span data-stu-id="3127b-105">Using Git and GitHub together makes it easy to collaborate widely on the Quantum Development Kit.</span></span>
<span data-ttu-id="3127b-106">В частности, любой репозиторий Git можно клонировать или разветвление, чтобы создать полностью независимую копию этого репозитория.</span><span class="sxs-lookup"><span data-stu-id="3127b-106">In particular, any Git repository can be cloned or forked to make a completely independent copy of that repository.</span></span>
<span data-ttu-id="3127b-107">Это позволяет вам работать с инструментами и в удобном для вас темпе.</span><span class="sxs-lookup"><span data-stu-id="3127b-107">This allows you to work on your contribution with the tools and at a pace that you prefer.</span></span>

<span data-ttu-id="3127b-108">Когда вы будете готовы, вы можете отправить нам запрос на включение вашего вклада в наш репозиториев с помощью функции _запроса на вытягивание_ GitHub.</span><span class="sxs-lookup"><span data-stu-id="3127b-108">When you're ready, you can send us a request to include your contribution into our repos, using GitHub's _pull request_ functionality.</span></span>
<span data-ttu-id="3127b-109">Страница для каждого запроса на включение внесенных изменений содержит сведения обо всех изменениях, внесенных в публикацию, список комментариев к публикации и набор средств проверки, которые другие члены сообщества могут использовать для предоставления отзывов и рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="3127b-109">The page for each pull request includes details of all the changes that make your contribution, a list of comments on your contribution, and a set of review tools that other members of the community can use to provide feedback and advice.</span></span>

> [!NOTE]
> <span data-ttu-id="3127b-110">Хотя полное руководство по Git выходит за рамки данного руководства, мы можем предложить следующие ссылки для получения дополнительных материалов по изучению Git:</span><span class="sxs-lookup"><span data-stu-id="3127b-110">While a full tutorial on Git is beyond the scope of this guide, we can suggest the following links for more resources on learning Git:</span></span>
>
> - <span data-ttu-id="3127b-111">[Изучение Git](https://www.atlassian.com/git). набор руководств по Git из Atlassian.</span><span class="sxs-lookup"><span data-stu-id="3127b-111">[Learn Git](https://www.atlassian.com/git): A set of Git tutorials from Atlassian.</span></span>
> - <span data-ttu-id="3127b-112">[Управление версиями в Visual Studio Code](https://code.visualstudio.com/docs/editor/versioncontrol): руководство по использованию Visual Studio Code в качестве графического пользовательского интерфейса для Git.</span><span class="sxs-lookup"><span data-stu-id="3127b-112">[Version Control in Visual Studio Code](https://code.visualstudio.com/docs/editor/versioncontrol): A guide on how to use Visual Studio Code as a GUI for Git.</span></span>
> - <span data-ttu-id="3127b-113">[Учебная лаборатория GitHub](https://lab.github.com/): набор онлайн-курсов по использованию Git, GitHub и связанных с ним технологий.</span><span class="sxs-lookup"><span data-stu-id="3127b-113">[GitHub Learning Lab](https://lab.github.com/): A set of online courses for using Git, GitHub, and related technologies.</span></span>
> - <span data-ttu-id="3127b-114">[Визуализация Git](https://git-school.github.io/visualizing-git/): интерактивное средство для визуализации изменения состояния репозитория командами Git.</span><span class="sxs-lookup"><span data-stu-id="3127b-114">[Visualizing Git](https://git-school.github.io/visualizing-git/): An interactive tool for visualizing how Git commands change the state of a repository.</span></span>
> - <span data-ttu-id="3127b-115">[Управление версиями с помощью Git (епкис 2016)](https://nbviewer.jupyter.org/github/QuinnPhys/PythonWorkshop-science/blob/master/lecture-1-scicomp-tools-part1.ipynb#Version-Control-with-Git-(50-Minutes)): руководство по Git, ориентированное на научные вычисления.</span><span class="sxs-lookup"><span data-stu-id="3127b-115">[Version Control with Git (EPQIS 2016)](https://nbviewer.jupyter.org/github/QuinnPhys/PythonWorkshop-science/blob/master/lecture-1-scicomp-tools-part1.ipynb#Version-Control-with-Git-(50-Minutes)): A Git tutorial oriented towards scientific computing.</span></span>
> - <span data-ttu-id="3127b-116">[Знакомство с ветвями Git](https://learngitbranching.js.org/). Интерактивный набор головоломок и реорганизации головоломки для получения сведений о новых функциях Git.</span><span class="sxs-lookup"><span data-stu-id="3127b-116">[Learn Git Branching](https://learngitbranching.js.org/): An interactive set of branching and rebasing puzzles to help learn new Git features.</span></span>

## <a name="what-is-a-pull-request"></a><span data-ttu-id="3127b-117">Что такое запрос на вытягивание?</span><span class="sxs-lookup"><span data-stu-id="3127b-117">What is a Pull Request?</span></span> ##

<span data-ttu-id="3127b-118">Если говорить о чем-то выше, очень важно сказать, что **такое запрос на**вытягивание.</span><span class="sxs-lookup"><span data-stu-id="3127b-118">Having said the above, it's helpful to take a few moments to say what a pull request **is**.</span></span>
<span data-ttu-id="3127b-119">При работе с Git все изменения представляются как _фиксации_ , которые описывают, как эти изменения связаны с состоянием репозитория перед этими изменениями.</span><span class="sxs-lookup"><span data-stu-id="3127b-119">When working with Git, any changes are represented as _commits_ that describe how those changes are related to the state of the repository before those changes.</span></span>
<span data-ttu-id="3127b-120">Мы будем часто рисовать диаграммы, в которых фиксации рисуются как круги со стрелками от предыдущих фиксаций.</span><span class="sxs-lookup"><span data-stu-id="3127b-120">We'll often draw diagrams in which commits are drawn as circles with arrows from previous commits.</span></span>

<span data-ttu-id="3127b-121">Предположим, что вы начали публикацию в _ветви_ с именем `feature` .</span><span class="sxs-lookup"><span data-stu-id="3127b-121">Suppose you have started a contribution in a _branch_ called `feature`.</span></span>
<span data-ttu-id="3127b-122">Затем вилка **Microsoft/такта** может выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="3127b-122">Then your fork of **Microsoft/Quantum** might look something like this:</span></span>

![Рабочая ветвь в GitHub](~/media/git-workflow-step0.png)

<span data-ttu-id="3127b-124">Если внести изменения в локальный репозиторий, вы можете _извлечь_ изменения из другого репозитория, чтобы отследить все изменения, произошедшие из вышестоящего.</span><span class="sxs-lookup"><span data-stu-id="3127b-124">If you make your changes in your local repository, you can _pull_ changes from another repository into yours to catch up to any changes that happened upstream.</span></span>

![Извлечение и слияние изменений из вышестоящего репозитория](~/media/git-workflow-step1.png)

<span data-ttu-id="3127b-126">Запросы на вытягивание работают таким же образом, но в обратную: при открытии запроса на включение внесенных изменений запрос к вышестоящему репозиторию будет извлекаться в.</span><span class="sxs-lookup"><span data-stu-id="3127b-126">Pull requests work the same way, but in reverse: when you open a pull request, you ask for the upstream repository to pull your contribution in.</span></span>

![Запрос на извлечение изменений в исходном репозитории](~/media/git-workflow-step2.png)

<span data-ttu-id="3127b-128">Когда вы открываете запрос на вытягивание в одном из наших репозиториев, GitHub предлагает другим пользователям в сообществе просматривать сводку изменений, комментарии к ним и предлагать, как сделать еще более качественную публикацию.</span><span class="sxs-lookup"><span data-stu-id="3127b-128">When you open a pull request to one of our repositories, GitHub will offer an opportunity for others in the community to see a summary of your changes, to comment on them, and to make suggestions for how to help make an even better contribution.</span></span>

![Снимок экрана запроса на вытягивание в GitHub](~/media/pull-request-header.png)

<span data-ttu-id="3127b-130">С помощью этого процесса мы можем использовать функции GitHub для улучшения вклада и поддержки высококачественного продукта для сообщества по программированию на основе тактов.</span><span class="sxs-lookup"><span data-stu-id="3127b-130">Using this process helps us use GitHub functionality to improve contributions and to maintain a high-quality product for the quantum programming community.</span></span>

## <a name="how-to-make-a-pull-request"></a><span data-ttu-id="3127b-131">Как создать запрос на вытягивание</span><span class="sxs-lookup"><span data-stu-id="3127b-131">How to Make a Pull Request</span></span> ##

<span data-ttu-id="3127b-132">Существует два основных способа выполнения запроса на включение внесенных изменений.</span><span class="sxs-lookup"><span data-stu-id="3127b-132">There are two main ways to make a pull request.</span></span>  
<span data-ttu-id="3127b-133">Для небольших изменений, которые влияют только на один файл, веб-интерфейс GitHub можно использовать для того, чтобы сделать запрос на вытягивание полностью доступным.</span><span class="sxs-lookup"><span data-stu-id="3127b-133">For small changes that only affect a single file, the GitHub web interface can be used to make a pull request entirely online.</span></span> <span data-ttu-id="3127b-134">Просто перейдите к файлу, который нужно изменить, и используйте значок редактирования.</span><span class="sxs-lookup"><span data-stu-id="3127b-134">Simply navigate to the file you want to edit and use the edit icon.</span></span>  
<span data-ttu-id="3127b-135">Для более сложных публикаций чаще всего проще клонировать репозиторий на локальный компьютер, чтобы сначала подготовиться к запросу на вытягивание.</span><span class="sxs-lookup"><span data-stu-id="3127b-135">For more complicated contributions, it's most often easier to clone the repository to your local computer to prepare for a pull request first.</span></span>

<!--
### Using the Web Interface ###

**TODO**

### Command-Line and GitHub Flow ###

Most of the time, it's easier to prepare a pull request on your own computer; that makes it easier to work incrementally, and to test your changes.
If you haven't already done so, the first step is to _fork_ the repository that you'd like to contribute to.
Forking makes a complete clone of the original repository, but under your GitHub account instead of under [Microsoft](http://github.com/Microsoft/) or [MicrosoftDocs](http://github.com/MicrosoftDocs/).
This way, you can edit your personal fork to your heart's content before making a pull request for your work.

**TODO: pick up here**

## Code Review and Etiquette ##

**TODO: PR ettiquette, reviews, etc.**

-->

## <a name="next-steps"></a><span data-ttu-id="3127b-136">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3127b-136">Next steps</span></span> ##

<span data-ttu-id="3127b-137">Поздравляем с использованием Git, чтобы помочь сообществу пакета разработки тактов!</span><span class="sxs-lookup"><span data-stu-id="3127b-137">Congratulations on using Git to help out the Quantum Development Kit community!</span></span>
<span data-ttu-id="3127b-138">Чтобы узнать больше о том, как доработать код, перейдите к следующему руководству.</span><span class="sxs-lookup"><span data-stu-id="3127b-138">To learn more about how to contribute code, please continue with the following guide.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="3127b-139">Сведения о том, как дополнять код</span><span class="sxs-lookup"><span data-stu-id="3127b-139">Learn how to contribute code</span></span>](xref:microsoft.quantum.contributing.code)
