---
title: Разработка на Q# в среде .NET
description: Сведения о том, как создать приложение Q# с помощью языков .NET.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: e8733918daa02afaea0fc1994d5f0851d4be9b93
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834335"
---
# <a name="develop-with-no-locq-and-net"></a><span data-ttu-id="60710-103">Разработка на Q# в среде .NET</span><span class="sxs-lookup"><span data-stu-id="60710-103">Develop with Q# and .NET</span></span>

<span data-ttu-id="60710-104">Язык Q# прекрасно сочетается с языками .NET, например C# и F#.</span><span class="sxs-lookup"><span data-stu-id="60710-104">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="60710-105">В этом руководстве мы покажем, как использовать Q# с ведущей программой, написанной на языке .NET.</span><span class="sxs-lookup"><span data-stu-id="60710-105">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="60710-106">Сначала мы создадим приложение Q# и ведущую программу .NET, а затем покажем, как вызвать код Q# из ведущей программы.</span><span class="sxs-lookup"><span data-stu-id="60710-106">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="60710-107">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="60710-107">Prerequisites</span></span>

- <span data-ttu-id="60710-108">Установите пакет средств разработки Quantum [для использования с проектами Q#](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="60710-108">Install the Quantum Development Kit [for use with Q# projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-no-locq-library-and-a-net-host"></a><span data-ttu-id="60710-109">Создание библиотеки Q# и ведущей программы .NET</span><span class="sxs-lookup"><span data-stu-id="60710-109">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="60710-110">Первый шаг — создать проекты для библиотеки Q# и ведущей программы .NET, которая будет вызывать операции и функции, определенные в библиотеке Q#.</span><span class="sxs-lookup"><span data-stu-id="60710-110">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="60710-111">Следуйте инструкциям на вкладке для вашей среды разработки.</span><span class="sxs-lookup"><span data-stu-id="60710-111">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="60710-112">Если вы используете редактор, отличный от Visual Studio или VS Code, просто выполните действия из командной строки.</span><span class="sxs-lookup"><span data-stu-id="60710-112">If you are using an editor other than Visual Studio or VS Code, simply follow the command prompt steps.</span></span>

### <a name="visual-studio-code-or-command-prompt"></a>[<span data-ttu-id="60710-113">Visual Studio Code или командная строка</span><span class="sxs-lookup"><span data-stu-id="60710-113">Visual Studio Code or command prompt</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="60710-114">Создайте новую библиотеку Q#:</span><span class="sxs-lookup"><span data-stu-id="60710-114">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="60710-115">Создайте новый консольный проект C# или F#.</span><span class="sxs-lookup"><span data-stu-id="60710-115">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="60710-116">Добавьте библиотеку Q# в качестве ссылки из ведущей программы:</span><span class="sxs-lookup"><span data-stu-id="60710-116">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="60710-117">(Не обязательно.) Создайте решения для обоих проектов.</span><span class="sxs-lookup"><span data-stu-id="60710-117">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="60710-118">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="60710-118">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="60710-119">Создайте новую библиотеку Q#:</span><span class="sxs-lookup"><span data-stu-id="60710-119">Create a new Q# library</span></span>
  - <span data-ttu-id="60710-120">Выберите **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="60710-120">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="60710-121">Введите "Q#"в поле поиска:</span><span class="sxs-lookup"><span data-stu-id="60710-121">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="60710-122">Выберите **библиотеку Q#** :</span><span class="sxs-lookup"><span data-stu-id="60710-122">Select **Q# Library**</span></span>
  - <span data-ttu-id="60710-123">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="60710-123">Select **Next**</span></span>
  - <span data-ttu-id="60710-124">Выберите имя и расположение библиотеки.</span><span class="sxs-lookup"><span data-stu-id="60710-124">Choose a name and location for your library</span></span>
  - <span data-ttu-id="60710-125">Убедитесь, что флажок "Поместить решение и проект в одной папке" **снят**.</span><span class="sxs-lookup"><span data-stu-id="60710-125">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="60710-126">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="60710-126">Select **Create**</span></span>
- <span data-ttu-id="60710-127">Создайте основную программу на C# или F#.</span><span class="sxs-lookup"><span data-stu-id="60710-127">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="60710-128">Последовательно выберите **Файл** → **Создать** → **Проект**.</span><span class="sxs-lookup"><span data-stu-id="60710-128">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="60710-129">Выберите "Консольное приложение (.NET Core)" для C# или F#.</span><span class="sxs-lookup"><span data-stu-id="60710-129">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="60710-130">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="60710-130">Select **Next**</span></span>
  - <span data-ttu-id="60710-131">В разделе *Решение* выберите "Добавить в решение".</span><span class="sxs-lookup"><span data-stu-id="60710-131">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="60710-132">Выберите имя основной программы.</span><span class="sxs-lookup"><span data-stu-id="60710-132">Choose a name for your host program</span></span>
  - <span data-ttu-id="60710-133">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="60710-133">Select **Create**</span></span>

***

## <a name="calling-into-no-locq-from-net"></a><span data-ttu-id="60710-134">Вызов Q# из .NET</span><span class="sxs-lookup"><span data-stu-id="60710-134">Calling into Q# from .NET</span></span>

<span data-ttu-id="60710-135">После выполнения приведенных выше инструкций по настройке проекта вы можете вызвать Q# из консольного приложения .NET.</span><span class="sxs-lookup"><span data-stu-id="60710-135">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="60710-136">Компилятор Q# будет создавать классы .NET для каждой операции и функции Q#, что позволит запускать в симуляторе квантовые программы.</span><span class="sxs-lookup"><span data-stu-id="60710-136">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="60710-137">[Пример взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) содержит следующий пример операции Q#:</span><span class="sxs-lookup"><span data-stu-id="60710-137">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="60710-138">Чтобы вызвать эту операцию из .NET в квантовом симуляторе, можно использовать метод `Run` класса .NET `RunAlgorithm`, созданный компилятором Q#:</span><span class="sxs-lookup"><span data-stu-id="60710-138">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="60710-139">C#</span><span class="sxs-lookup"><span data-stu-id="60710-139">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="60710-140">F#</span><span class="sxs-lookup"><span data-stu-id="60710-140">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="60710-141">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="60710-141">Next steps</span></span>

<span data-ttu-id="60710-142">Теперь, когда у вас настроен пакет средств разработки Quantum для приложений Q# и для взаимодействия с .NET, вы можете написать и запустить [свою первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="60710-142">Now that you have the Quantum Development Kit set up for both Q# applications and interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
