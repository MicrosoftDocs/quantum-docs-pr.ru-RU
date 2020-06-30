---
title: Разработка на Q# в среде .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 2b0b16bdd9fccc3b668036e6df2b20e11b32f8b6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274154"
---
# <a name="develop-with-q-and-net"></a><span data-ttu-id="5945f-102">Разработка на Q# в среде .NET</span><span class="sxs-lookup"><span data-stu-id="5945f-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="5945f-103">Язык Q# прекрасно сочетается с языками .NET, например C# и F#.</span><span class="sxs-lookup"><span data-stu-id="5945f-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="5945f-104">В этом руководстве мы покажем, как использовать Q# с основной программой, написанной на языке .NET.</span><span class="sxs-lookup"><span data-stu-id="5945f-104">In this guide, we'll demonstrate how to use Q# with a host program written in a .NET language.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5945f-105">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="5945f-105">Prerequisites</span></span>

- <span data-ttu-id="5945f-106">Установите Quantum Development Kit [для использования с проектами командной строки Q#](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="5945f-106">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="5945f-107">Создание библиотеки Q# и узла .NET</span><span class="sxs-lookup"><span data-stu-id="5945f-107">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="5945f-108">Первый шаг — создать проекты для библиотеки Q# и узла .NET, который будет вызывать операции и функции, определенные в библиотеке Q#.</span><span class="sxs-lookup"><span data-stu-id="5945f-108">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

### <a name="visual-studio-2019"></a>[<span data-ttu-id="5945f-109">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="5945f-109">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="5945f-110">Создайте библиотеку Q#.</span><span class="sxs-lookup"><span data-stu-id="5945f-110">Create a new Q# library</span></span>
  - <span data-ttu-id="5945f-111">Выберите **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="5945f-111">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="5945f-112">Введите "Q#" в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="5945f-112">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="5945f-113">Выберите **Библиотека Q#** .</span><span class="sxs-lookup"><span data-stu-id="5945f-113">Select **Q# Library**</span></span>
  - <span data-ttu-id="5945f-114">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5945f-114">Select **Next**</span></span>
  - <span data-ttu-id="5945f-115">Выберите имя и расположение библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5945f-115">Choose a name and location for your library</span></span>
  - <span data-ttu-id="5945f-116">Убедитесь, что флажок "Поместить решение и проект в одной папке" **снят**.</span><span class="sxs-lookup"><span data-stu-id="5945f-116">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="5945f-117">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="5945f-117">Select **Create**</span></span>
- <span data-ttu-id="5945f-118">Создайте основную программу на C# или F#.</span><span class="sxs-lookup"><span data-stu-id="5945f-118">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="5945f-119">Последовательно выберите **Файл** → **Создать** → **Проект**.</span><span class="sxs-lookup"><span data-stu-id="5945f-119">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="5945f-120">Выберите "Консольное приложение (.NET Core)" для C# или F#.</span><span class="sxs-lookup"><span data-stu-id="5945f-120">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="5945f-121">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5945f-121">Select **Next**</span></span>
  - <span data-ttu-id="5945f-122">В разделе *Решение* выберите "Добавить в решение".</span><span class="sxs-lookup"><span data-stu-id="5945f-122">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="5945f-123">Выберите имя основной программы.</span><span class="sxs-lookup"><span data-stu-id="5945f-123">Choose a name for your host program</span></span>
  - <span data-ttu-id="5945f-124">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="5945f-124">Select **Create**</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="5945f-125">Visual Studio Code или командная строка</span><span class="sxs-lookup"><span data-stu-id="5945f-125">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="5945f-126">Создайте библиотеку Q#.</span><span class="sxs-lookup"><span data-stu-id="5945f-126">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="5945f-127">Создайте новый консольный проект C# или F#.</span><span class="sxs-lookup"><span data-stu-id="5945f-127">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="5945f-128">Добавьте библиотеку Q# в качестве ссылки из основной программы.</span><span class="sxs-lookup"><span data-stu-id="5945f-128">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="5945f-129">(Не обязательно.) Создайте решения для обоих проектов.</span><span class="sxs-lookup"><span data-stu-id="5945f-129">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="5945f-130">Вызов Q# из .NET</span><span class="sxs-lookup"><span data-stu-id="5945f-130">Calling into Q# from .NET</span></span>

<span data-ttu-id="5945f-131">После выполнения приведенных выше инструкций по настройке проекта вы можете вызвать Q# из консольного приложения .NET.</span><span class="sxs-lookup"><span data-stu-id="5945f-131">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="5945f-132">Компилятор Q# будет создавать классы .NET для каждой операции и функции Q#, что позволит запускать в симуляторе квантовые программы.</span><span class="sxs-lookup"><span data-stu-id="5945f-132">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="5945f-133">Например, [пример взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) содержит следующий пример операции Q#:</span><span class="sxs-lookup"><span data-stu-id="5945f-133">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="5945f-134">Чтобы вызвать эту операцию из .NET в квантовом симуляторе, можно использовать метод `Run` класса .NET `RunAlgorithm`, созданный компилятором Q#.</span><span class="sxs-lookup"><span data-stu-id="5945f-134">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="5945f-135">C#</span><span class="sxs-lookup"><span data-stu-id="5945f-135">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="5945f-136">F#</span><span class="sxs-lookup"><span data-stu-id="5945f-136">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="5945f-137">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5945f-137">Next steps</span></span>

<span data-ttu-id="5945f-138">Теперь, когда у вас настроен пакет Quantum Development Kit для программ командной строки Q# и для взаимодействия с .NET, вы можете написать и запустить свою [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="5945f-138">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
