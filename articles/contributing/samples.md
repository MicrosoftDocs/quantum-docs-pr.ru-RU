---
title: Участвующие примеры для Microsoft КДК
description: Сведения о том, как внести пример кода в Microsoft Quantum Development Kit (КДК).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024157"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a><span data-ttu-id="f441c-103">Участвующие примеры в пакете разработки тактов</span><span class="sxs-lookup"><span data-stu-id="f441c-103">Contributing Samples to the Quantum Development Kit</span></span>

<span data-ttu-id="f441c-104">Если вы заинтересованы в создании кода в [репозитории примеров](https://github.com/Microsoft/Quantum), благодарим вас за то, что вы пожелаете сделать сообщество разработчиков тактов лучше!</span><span class="sxs-lookup"><span data-stu-id="f441c-104">If you're interested in contributing code to the [samples repository](https://github.com/Microsoft/Quantum), thank you for making the quantum development community a better place!</span></span>

## <a name="the-quantum-development-kit-samples-repository"></a><span data-ttu-id="f441c-105">Репозиторий примеров для пакета разработки тактов</span><span class="sxs-lookup"><span data-stu-id="f441c-105">The Quantum Development Kit Samples Repository</span></span>

<span data-ttu-id="f441c-106">Чтобы помочь вам подготовить публикацию для максимально эффективного использования, полезно ознакомиться с расположением репозитория Samples:</span><span class="sxs-lookup"><span data-stu-id="f441c-106">To help you prepare your contribution to help out as much as possible, it's helpful to take a quick look at how the samples repository is laid out:</span></span>

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

<span data-ttu-id="f441c-107">Это значит, что образцы в [репозитории Microsoft/такта](https://github.com/microsoft/Quantum) разбиваются по предметной области на разные папки, такие как `algorithms/`, `arithmetic/`или `characterization/`.</span><span class="sxs-lookup"><span data-stu-id="f441c-107">That is, the samples in the [microsoft/Quantum repository](https://github.com/microsoft/Quantum) are broken down by subject area into different folders such as `algorithms/`, `arithmetic/`, or `characterization/`.</span></span>
<span data-ttu-id="f441c-108">В папке для каждой предметной области каждый пример состоит из одной папки, которая собирает все, что пользователю потребуется для изучения и использования этого примера.</span><span class="sxs-lookup"><span data-stu-id="f441c-108">Within the folder for each subject area, each sample consists of a single folder that collects everything a user will need to explore and make use of that sample.</span></span>

## <a name="how-samples-are-structured"></a><span data-ttu-id="f441c-109">Структурирование образцов</span><span class="sxs-lookup"><span data-stu-id="f441c-109">How Samples are Structured</span></span>

<span data-ttu-id="f441c-110">Просмотрев файлы, составляющие каждую папку, давайте подробно рассмотрим пример [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) .</span><span class="sxs-lookup"><span data-stu-id="f441c-110">Looking at the files that make up each folder, let's dive into the [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) sample.</span></span>

| <span data-ttu-id="f441c-111">Файл</span><span class="sxs-lookup"><span data-stu-id="f441c-111">File</span></span>              | <span data-ttu-id="f441c-112">Description</span><span class="sxs-lookup"><span data-stu-id="f441c-112">Description</span></span>                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | <span data-ttu-id="f441c-113">Q # проект, используемый для построения примера с пакет SDK для .NET Core</span><span class="sxs-lookup"><span data-stu-id="f441c-113">Q# project used to build the sample with the .NET Core SDK</span></span> |
| `Game.qs`         | <span data-ttu-id="f441c-114">Q # операции и функции для примера</span><span class="sxs-lookup"><span data-stu-id="f441c-114">Q# operations and functions for the sample</span></span>                 |
| `Host.cs`         | <span data-ttu-id="f441c-115">C#ведущее приложение, используемое для запуска примера</span><span class="sxs-lookup"><span data-stu-id="f441c-115">C# host program used to run the sample</span></span>                     |
| `host.py`         | <span data-ttu-id="f441c-116">Главное приложение Python, используемое для запуска примера</span><span class="sxs-lookup"><span data-stu-id="f441c-116">Python host program used to run the sample</span></span>                 |
| `README.md`       | <span data-ttu-id="f441c-117">Документация о том, что делает пример и как его использовать</span><span class="sxs-lookup"><span data-stu-id="f441c-117">Documentation on what the sample does and how to use it</span></span>    |

<span data-ttu-id="f441c-118">Не все выборки будут иметь одинаковый набор файлов (например, некоторые примеры могут быть C#только что-либо, другие могут не иметь узла Python, или для некоторых примеров может потребоваться работать с файлами данных ауксиллари).</span><span class="sxs-lookup"><span data-stu-id="f441c-118">Not all samples will have the exact same set of files (e.g.: some samples may be C#-only, others may not have a Python host, or some samples may require auxillary data files to work).</span></span>

## <a name="anatomy-of-a-helpful-readme-file"></a><span data-ttu-id="f441c-119">Анатомия полезного файла сведений</span><span class="sxs-lookup"><span data-stu-id="f441c-119">Anatomy of a Helpful README File</span></span>

<span data-ttu-id="f441c-120">Один из особенно важных файлов, однако, является файлом `README.md`, так как именно это необходимо для начала работы с вашим примером.</span><span class="sxs-lookup"><span data-stu-id="f441c-120">One especially important file, though, is the `README.md` file, as that's what users need to get started with your sample!</span></span>

<span data-ttu-id="f441c-121">Каждый `README.md` должен начинаться с некоторых метаданных, которые помогают docs.microsoft.com/samples найти вашу публикацию.</span><span class="sxs-lookup"><span data-stu-id="f441c-121">Each `README.md` should start with some metadata that helps docs.microsoft.com/samples find your contribution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="f441c-122">Посмотрите, как готовится пример ЧШ-Game</span><span class="sxs-lookup"><span data-stu-id="f441c-122">See how the chsh-game sample is rendered</span></span>](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

<span data-ttu-id="f441c-123">Эти метаданные предоставляются в виде [заголовка YAML](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) , который указывает, какие языки охватывает ваш образец (как правило, это `qsharp`, `csharp`и `python`) и какие продукты ваш образец охватывает (как правило, просто `qdk`).</span><span class="sxs-lookup"><span data-stu-id="f441c-123">This metadata is provided as a [YAML header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) that indicates what languages your sample covers (typically, this will be `qsharp`, `csharp`, and `python`), and what products your sample covers (typically, just `qdk`).</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> <span data-ttu-id="f441c-124">Для отображения примера в docs.microsoft.com/samples требуется ключ `page_type: sample` в заголовке.</span><span class="sxs-lookup"><span data-stu-id="f441c-124">The `page_type: sample` key in the header is required for your sample to appear at docs.microsoft.com/samples.</span></span>
> <span data-ttu-id="f441c-125">Аналогичным образом, ключи `product` и `language` важны для того, чтобы помочь пользователям найти и запустить пример.</span><span class="sxs-lookup"><span data-stu-id="f441c-125">Similarly, the `product` and `language` keys are critical for helping users to find and run your sample.</span></span>

<span data-ttu-id="f441c-126">После этого полезно дать краткое введение в том, что делает новый пример:</span><span class="sxs-lookup"><span data-stu-id="f441c-126">After that, it's helpful to give a short intro that says what your new sample does:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

<span data-ttu-id="f441c-127">Пользователи вашего примера также оценят знание того, что им нужно для его запуска (например: сделать так, чтобы пользователям просто был нужен сам пакет разработки такта, или требуется дополнительное программное обеспечение, например node. js?):</span><span class="sxs-lookup"><span data-stu-id="f441c-127">Users of your sample will also appreciate knowing what they need to run it (e.g.: do users just need the Quantum Development Kit itself, or do they need additional software such as node.js?):</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

<span data-ttu-id="f441c-128">Все это на месте, вы можете сообщить пользователям, как запустить пример:</span><span class="sxs-lookup"><span data-stu-id="f441c-128">With all that in place, you can tell users how to run your sample:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

<span data-ttu-id="f441c-129">И, наконец, полезно рассказать пользователям о том, что делает каждый файл в примере, и где их можно найти, чтобы получить дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="f441c-129">Finally, it's helpful to tell users what each file in your sample does, and where they can go for more information:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> <span data-ttu-id="f441c-130">Обязательно используйте абсолютные URL-адреса, так как ваш пример будет отображаться по другому URL-адресу при подготовке к просмотру в docs.microsoft.com/samples!</span><span class="sxs-lookup"><span data-stu-id="f441c-130">Make sure to use absolute URLs here, since your sample will appear at a different URL when rendered at docs.microsoft.com/samples!</span></span>
