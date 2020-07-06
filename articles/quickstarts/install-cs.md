---
title: Разработка на Q# в среде .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 714c15d9589095f0fe395fcd6941672167879dca
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885498"
---
# <a name="develop-with-q-and-net"></a><span data-ttu-id="5ee7a-102">Разработка на Q# в среде .NET</span><span class="sxs-lookup"><span data-stu-id="5ee7a-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="5ee7a-103">Язык Q# прекрасно сочетается с языками .NET, например C# и F#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="5ee7a-104">В этом руководстве мы покажем, как использовать Q# с основной программой, написанной на языке .NET.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-104">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="5ee7a-105">Сначала мы создадим приложение Q# и узел .NET, а затем покажем, как вызвать код Q# из узла.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-105">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5ee7a-106">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="5ee7a-106">Prerequisites</span></span>

- <span data-ttu-id="5ee7a-107">Установите Quantum Development Kit [для использования с проектами командной строки Q#](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="5ee7a-107">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="5ee7a-108">Создание библиотеки Q# и узла .NET</span><span class="sxs-lookup"><span data-stu-id="5ee7a-108">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="5ee7a-109">Первый шаг — создать проекты для библиотеки Q# и узла .NET, который будет вызывать операции и функции, определенные в библиотеке Q#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-109">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="5ee7a-110">Следуйте инструкциям на вкладке для вашей среды разработки.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-110">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="5ee7a-111">Если вы используете редактор, отличный от Visual Studio или VS Code, просто выполните действия из командной строки.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-111">If you are using an editor other than Visual Studio or VS Code, simply follow the command line steps.</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="5ee7a-112">Visual Studio Code или командная строка</span><span class="sxs-lookup"><span data-stu-id="5ee7a-112">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="5ee7a-113">Создайте библиотеку Q#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-113">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="5ee7a-114">Создайте новый консольный проект C# или F#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-114">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="5ee7a-115">Добавьте библиотеку Q# в качестве ссылки из основной программы.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-115">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="5ee7a-116">(Не обязательно.) Создайте решения для обоих проектов.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-116">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="5ee7a-117">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="5ee7a-117">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="5ee7a-118">Создайте библиотеку Q#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-118">Create a new Q# library</span></span>
  - <span data-ttu-id="5ee7a-119">Выберите **Файл** -> **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-119">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="5ee7a-120">Введите "Q#" в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-120">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="5ee7a-121">Выберите **Библиотека Q#** .</span><span class="sxs-lookup"><span data-stu-id="5ee7a-121">Select **Q# Library**</span></span>
  - <span data-ttu-id="5ee7a-122">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-122">Select **Next**</span></span>
  - <span data-ttu-id="5ee7a-123">Выберите имя и расположение библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-123">Choose a name and location for your library</span></span>
  - <span data-ttu-id="5ee7a-124">Убедитесь, что флажок "Поместить решение и проект в одной папке" **снят**.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-124">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="5ee7a-125">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="5ee7a-125">Select **Create**</span></span>
- <span data-ttu-id="5ee7a-126">Создайте основную программу на C# или F#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-126">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="5ee7a-127">Последовательно выберите **Файл** → **Создать** → **Проект**.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-127">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="5ee7a-128">Выберите "Консольное приложение (.NET Core)" для C# или F#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-128">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="5ee7a-129">Щелкните **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-129">Select **Next**</span></span>
  - <span data-ttu-id="5ee7a-130">В разделе *Решение* выберите "Добавить в решение".</span><span class="sxs-lookup"><span data-stu-id="5ee7a-130">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="5ee7a-131">Выберите имя основной программы.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-131">Choose a name for your host program</span></span>
  - <span data-ttu-id="5ee7a-132">Нажмите кнопку **Создать**</span><span class="sxs-lookup"><span data-stu-id="5ee7a-132">Select **Create**</span></span>

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="5ee7a-133">Вызов Q# из .NET</span><span class="sxs-lookup"><span data-stu-id="5ee7a-133">Calling into Q# from .NET</span></span>

<span data-ttu-id="5ee7a-134">После выполнения приведенных выше инструкций по настройке проекта вы можете вызвать Q# из консольного приложения .NET.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-134">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="5ee7a-135">Компилятор Q# будет создавать классы .NET для каждой операции и функции Q#, что позволит запускать в симуляторе квантовые программы.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-135">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="5ee7a-136">Например, [пример взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) содержит следующий пример операции Q#:</span><span class="sxs-lookup"><span data-stu-id="5ee7a-136">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="5ee7a-137">Чтобы вызвать эту операцию из .NET в квантовом симуляторе, можно использовать метод `Run` класса .NET `RunAlgorithm`, созданный компилятором Q#.</span><span class="sxs-lookup"><span data-stu-id="5ee7a-137">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="5ee7a-138">C#</span><span class="sxs-lookup"><span data-stu-id="5ee7a-138">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="5ee7a-139">F#</span><span class="sxs-lookup"><span data-stu-id="5ee7a-139">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="5ee7a-140">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5ee7a-140">Next steps</span></span>

<span data-ttu-id="5ee7a-141">Теперь, когда у вас настроен пакет Quantum Development Kit для программ командной строки Q# и для взаимодействия с .NET, вы можете написать и запустить свою [первую квантовую программу](xref:microsoft.quantum.quickstarts.qrng).</span><span class="sxs-lookup"><span data-stu-id="5ee7a-141">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
