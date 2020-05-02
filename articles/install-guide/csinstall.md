---
title: Разработка на Q# + C#
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 5bcb036b0b32e64d43f90e9a068d9dcc237890ba
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680160"
---
# <a name="using-q-with-c-and-f"></a><span data-ttu-id="74379-102">Использование Q # с C\# и F\#</span><span class="sxs-lookup"><span data-stu-id="74379-102">Using Q# with C\# and F\#</span></span>

<span data-ttu-id="74379-103">Функция Q # разработана для корректного воспроизведения на языках .NET, таких как C# и F #.</span><span class="sxs-lookup"><span data-stu-id="74379-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="74379-104">В этом руководство мы покажем, как использовать Q # с основной программой, написанной на языке .NET.</span><span class="sxs-lookup"><span data-stu-id="74379-104">In this guide, we'll demonstrate how to use Q# with a host program written in a .NET language.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="74379-105">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="74379-105">Prerequisites</span></span>

- <span data-ttu-id="74379-106">Установите пакет средств разработки такта [для использования с проектами командной строки Q #](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="74379-106">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="74379-107">Создание библиотеки Q # и узла .NET</span><span class="sxs-lookup"><span data-stu-id="74379-107">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="74379-108">Первым шагом является создание проектов для библиотеки Q # и для узла .NET, который будет вызывать операции и функции, определенные в библиотеке Q #.</span><span class="sxs-lookup"><span data-stu-id="74379-108">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

### <a name="visual-studio-2019"></a>[<span data-ttu-id="74379-109">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="74379-109">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="74379-110">Создать новую библиотеку Q #</span><span class="sxs-lookup"><span data-stu-id="74379-110">Create a new Q# library</span></span>
  - <span data-ttu-id="74379-111">Переход к **файлу** -> **Новый** -> **проект**</span><span class="sxs-lookup"><span data-stu-id="74379-111">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="74379-112">Введите "Q #" в поле поиска</span><span class="sxs-lookup"><span data-stu-id="74379-112">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="74379-113">Выбор **Q # Library**</span><span class="sxs-lookup"><span data-stu-id="74379-113">Select **Q# Library**</span></span>
  - <span data-ttu-id="74379-114">Нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="74379-114">Select **Next**</span></span>
  - <span data-ttu-id="74379-115">Выберите имя и расположение для библиотеки</span><span class="sxs-lookup"><span data-stu-id="74379-115">Choose a name and location for your library</span></span>
  - <span data-ttu-id="74379-116">Убедитесь, что флажок "размещение проекта и решения в одном каталоге" **снят**</span><span class="sxs-lookup"><span data-stu-id="74379-116">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="74379-117">Выберите **создать** .</span><span class="sxs-lookup"><span data-stu-id="74379-117">Select **Create**</span></span>
- <span data-ttu-id="74379-118">Создание основной программы на C# или F #</span><span class="sxs-lookup"><span data-stu-id="74379-118">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="74379-119">Последовательно выберите пункты **файл** → **создать** → **проект** .</span><span class="sxs-lookup"><span data-stu-id="74379-119">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="74379-120">Выберите "консольное приложение (.NET Core") "для C# или F #</span><span class="sxs-lookup"><span data-stu-id="74379-120">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="74379-121">Нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="74379-121">Select **Next**</span></span>
  - <span data-ttu-id="74379-122">В разделе *решение*выберите "добавить в решение".</span><span class="sxs-lookup"><span data-stu-id="74379-122">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="74379-123">Выберите имя для своей основной программы</span><span class="sxs-lookup"><span data-stu-id="74379-123">Choose a name for your host program</span></span>
  - <span data-ttu-id="74379-124">Выберите **создать** .</span><span class="sxs-lookup"><span data-stu-id="74379-124">Select **Create**</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="74379-125">Visual Studio Code или Командная строка</span><span class="sxs-lookup"><span data-stu-id="74379-125">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="74379-126">Создать новую библиотеку Q #</span><span class="sxs-lookup"><span data-stu-id="74379-126">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="74379-127">Создание нового проекта консоли C# или F #</span><span class="sxs-lookup"><span data-stu-id="74379-127">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="74379-128">Добавление библиотеки Q # в качестве ссылки из основной программы</span><span class="sxs-lookup"><span data-stu-id="74379-128">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="74379-129">Используемых Создание решения для обоих проектов</span><span class="sxs-lookup"><span data-stu-id="74379-129">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="74379-130">Вызов в Q # из .NET</span><span class="sxs-lookup"><span data-stu-id="74379-130">Calling into Q# from .NET</span></span>

<span data-ttu-id="74379-131">После выполнения приведенных выше инструкций Вы можете обращаться к Q # из консольного приложения .NET.</span><span class="sxs-lookup"><span data-stu-id="74379-131">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="74379-132">Компилятор Q # будет создавать классы .NET для каждой операции и функции Q #, которые позволяют запускать в симуляторе программы-такты.</span><span class="sxs-lookup"><span data-stu-id="74379-132">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="74379-133">Например, [Пример взаимодействия с .NET](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) включает в себя следующий пример операции Q #:</span><span class="sxs-lookup"><span data-stu-id="74379-133">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="74379-134">Чтобы вызвать эту операцию из .NET в имитаторе такта, можно использовать `Run` метод класса `RunAlgorithm` .NET, созданный компилятором Q #:</span><span class="sxs-lookup"><span data-stu-id="74379-134">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="74379-135">C#</span><span class="sxs-lookup"><span data-stu-id="74379-135">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="74379-136">F#</span><span class="sxs-lookup"><span data-stu-id="74379-136">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="whats-next"></a><span data-ttu-id="74379-137">Что дальше?</span><span class="sxs-lookup"><span data-stu-id="74379-137">What's next?</span></span>

<span data-ttu-id="74379-138">Теперь, когда у вас есть пакет средств разработки такта для программ командной строки Q # и для взаимодействия с .NET, вы можете написать и запустить [первую тактовую программу](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="74379-138">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
