---
title: Исследование запутанности с использованием Q#
description: Узнайте о том, как написать квантовую программу на Q#. Разработка приложения, которое использует состояние Белла, с помощью Microsoft Quantum Development Kit
author: natke
ms.author: nakersha
ms.date: 10/07/2019
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 7836e39227fa2282c6e2faa039f6e625103d5403
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426844"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="35487-104">Руководство по Исследование запутанности с использованием Q\#</span><span class="sxs-lookup"><span data-stu-id="35487-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="35487-105">В этом руководстве показано, как создать программу на Q#, которая управляет кубитами и измеряет их, демонстрируя эффекты суперпозиции и запутанности.</span><span class="sxs-lookup"><span data-stu-id="35487-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>
<span data-ttu-id="35487-106">Следуя этим инструкциям, вы установите QDK, напишете программу и выполните ее на квантовом симуляторе.</span><span class="sxs-lookup"><span data-stu-id="35487-106">This guides you on installing the QDK, building the program and executing that program on a quantum simulator.</span></span>  

<span data-ttu-id="35487-107">В результате у вас получится приложение Bell, которое демонстрирует квантовую запутанность.</span><span class="sxs-lookup"><span data-stu-id="35487-107">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="35487-108">Имя Bell — это отсылка к состоянию Белла, которое обозначает особые квантовые состояния двух кубитов с простейшими примерами эффектов суперпозиции и квантовой запутанности.</span><span class="sxs-lookup"><span data-stu-id="35487-108">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="35487-109">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="35487-109">Pre-requisites</span></span>

<span data-ttu-id="35487-110">Если вы готовы писать код, выполните следующие действия, прежде чем продолжать:</span><span class="sxs-lookup"><span data-stu-id="35487-110">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="35487-111">[Установите](xref:microsoft.quantum.install) Microsoft Quantum Development Kit для выбранного вами языка и среды разработки.</span><span class="sxs-lookup"><span data-stu-id="35487-111">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your preferred language and development environment</span></span>
* <span data-ttu-id="35487-112">Если эта платформа уже установлена, убедитесь, что она [обновлена](xref:microsoft.quantum.update) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="35487-112">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="35487-113">Вы также можете просто прочитать это руководство, не устанавливая QDK, чтобы получить общие сведения о языке программирования Q# и важнейших концепциях квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="35487-113">You can also follow along with the narrative without installing the QDK, reviewing the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="demonstrating-qubit-behavior-with-q"></a><span data-ttu-id="35487-114">Демонстрация поведения кубитов с использованием Q#</span><span class="sxs-lookup"><span data-stu-id="35487-114">Demonstrating qubit behavior with Q#</span></span>

<span data-ttu-id="35487-115">Давайте вспомним простейшее [определение кубита](xref:microsoft.quantum.overview.understanding).</span><span class="sxs-lookup"><span data-stu-id="35487-115">Recall our simple [definition of a qubit](xref:microsoft.quantum.overview.understanding).</span></span>  <span data-ttu-id="35487-116">В классическом бите хранится одно двоичное значение (0 или 1), а кубит может находиться в состоянии **суперпозиции** значений 0 и 1 одновременно.</span><span class="sxs-lookup"><span data-stu-id="35487-116">Where classical bits hold a single binary value such as a 0 or 1, the state of a qubit can be in a **superposition** of 0 and 1 simultaneously.</span></span>  <span data-ttu-id="35487-117">В теории кубит можно рассматривать как направление в пространстве (вектор).</span><span class="sxs-lookup"><span data-stu-id="35487-117">Conceptually, a qubit can be thought of as a direction in space (also known as a vector).</span></span>  <span data-ttu-id="35487-118">Кубит может содержать любое из возможных направлений.</span><span class="sxs-lookup"><span data-stu-id="35487-118">A qubit can be in any of the possible directions.</span></span> <span data-ttu-id="35487-119">Два **классических состояния** в этой модели соответствуют двум направлениям: 100 % вероятности получить при измерении 0 и 100 % вероятности получить 1.</span><span class="sxs-lookup"><span data-stu-id="35487-119">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>  <span data-ttu-id="35487-120">Такое представление более строго визуализируется в виде [сферы Блоха](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span><span class="sxs-lookup"><span data-stu-id="35487-120">This representation is also more formally visualized by the [bloch sphere](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>


<span data-ttu-id="35487-121">Измерение кубита возвращает двоичный результат и изменяет состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-121">The act of measurement produces a binary result and changes a qubit state.</span></span> <span data-ttu-id="35487-122">Результатом измерения будет классическое двоичное значение: 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="35487-122">Measurement produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="35487-123">При этом кубит переходит из состояния суперпозиции в одно из классических состояний.</span><span class="sxs-lookup"><span data-stu-id="35487-123">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="35487-124">С этого момента все повторные измерения будут возвращать тот же двоичный результат, если не выполняются дополнительные промежуточные операции.</span><span class="sxs-lookup"><span data-stu-id="35487-124">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="35487-125">Несколько кубитов могут находиться в состоянии **запутанности**.</span><span class="sxs-lookup"><span data-stu-id="35487-125">Multiple qubits can be **entangled**.</span></span> <span data-ttu-id="35487-126">При измерении одного из запутанных кубитов мы получаем сведения о состоянии второго.</span><span class="sxs-lookup"><span data-stu-id="35487-126">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="35487-127">Теперь мы готовы продемонстрировать, как это поведение моделируется с использованием Q#.</span><span class="sxs-lookup"><span data-stu-id="35487-127">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="35487-128">Вы начнете работу с самой простой программы и постепенно доработаете ее для демонстрации квантовой суперпозиции и квантовой запутанности.</span><span class="sxs-lookup"><span data-stu-id="35487-128">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="setup"></a><span data-ttu-id="35487-129">Настройка</span><span class="sxs-lookup"><span data-stu-id="35487-129">Setup</span></span>

<span data-ttu-id="35487-130">Приложения в Microsoft Quantum Development Kit состоят из двух частей:</span><span class="sxs-lookup"><span data-stu-id="35487-130">Applications developed with Microsoft's Quantum Development Kit consist of two parts:</span></span>

1. <span data-ttu-id="35487-131">Один или несколько квантовых алгоритмов реализуются на квантовом языке программирования Q#.</span><span class="sxs-lookup"><span data-stu-id="35487-131">One or more quantum algorithms, implemented using the Q# quantum programming language.</span></span>
1. <span data-ttu-id="35487-132">Основная программа на любом традиционном языке программирования, например Python или C#, используется в качестве основной точки входа и вызывает операции Q# для применения квантовых алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="35487-132">A host program, implemented in a programming language like Python or C# that serves as the main entry point and invokes Q# operations to execute a quantum algorithm.</span></span>

#### <a name="python"></a>[<span data-ttu-id="35487-133">Python</span><span class="sxs-lookup"><span data-stu-id="35487-133">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="35487-134">Выберите расположение для приложения.</span><span class="sxs-lookup"><span data-stu-id="35487-134">Choose a location for your application</span></span>

1. <span data-ttu-id="35487-135">Создайте файл с именем `Bell.qs`.</span><span class="sxs-lookup"><span data-stu-id="35487-135">Create a file called `Bell.qs`.</span></span> <span data-ttu-id="35487-136">Этот файл будет содержать код Q#.</span><span class="sxs-lookup"><span data-stu-id="35487-136">This file will contain your Q# code.</span></span>

1. <span data-ttu-id="35487-137">Создайте файл с именем `host.py`.</span><span class="sxs-lookup"><span data-stu-id="35487-137">Create a file called `host.py`.</span></span> <span data-ttu-id="35487-138">Этот файл будет содержать основной код Python.</span><span class="sxs-lookup"><span data-stu-id="35487-138">This file will contain your Python host code.</span></span>

#### <a name="c-command-line"></a>[<span data-ttu-id="35487-139">Командная строка C#</span><span class="sxs-lookup"><span data-stu-id="35487-139">C# Command Line</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="35487-140">Создайте проект Q#.</span><span class="sxs-lookup"><span data-stu-id="35487-140">Create a new Q# project:</span></span>

    ```bash
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    <span data-ttu-id="35487-141">Вы увидите файл `.csproj`, файл Q# с именем `Operations.qs` и файл основной программы с именем `Driver.cs`.</span><span class="sxs-lookup"><span data-stu-id="35487-141">You should see a `.csproj` file, a Q# file called `Operations.qs`, and a host program file called `Driver.cs`</span></span>

1. <span data-ttu-id="35487-142">Переименование файла Q#</span><span class="sxs-lookup"><span data-stu-id="35487-142">Rename the Q# file</span></span>

    ```bash
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[<span data-ttu-id="35487-143">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="35487-143">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="35487-144">Создание нового проекта</span><span class="sxs-lookup"><span data-stu-id="35487-144">Create a new project</span></span>

   * <span data-ttu-id="35487-145">Запустите Visual Studio</span><span class="sxs-lookup"><span data-stu-id="35487-145">Open Visual Studio</span></span>
   * <span data-ttu-id="35487-146">Откройте меню **Файл** и щелкните **Создать** -> **Проект**.</span><span class="sxs-lookup"><span data-stu-id="35487-146">Go to the **File** menu and select **New** -> **Project...**</span></span>
   * <span data-ttu-id="35487-147">В обозревателе шаблонов проектов введите `Q#` в поле поиска и выберите шаблон `Q# Application`.</span><span class="sxs-lookup"><span data-stu-id="35487-147">In the project template explorer, type `Q#` into the search field and select the `Q# Application` template</span></span>
   * <span data-ttu-id="35487-148">Присвойте проекту имя `Bell`.</span><span class="sxs-lookup"><span data-stu-id="35487-148">Give your project the name `Bell`</span></span>

1. <span data-ttu-id="35487-149">Переименование файла Q#</span><span class="sxs-lookup"><span data-stu-id="35487-149">Rename the Q# file</span></span>

   * <span data-ttu-id="35487-150">Перейдите к **обозревателю решений**.</span><span class="sxs-lookup"><span data-stu-id="35487-150">Navigate to the **Solution Explorer**</span></span>
   * <span data-ttu-id="35487-151">Щелкните правой кнопкой мыши файл `Operations.qs`.</span><span class="sxs-lookup"><span data-stu-id="35487-151">Right click on the `Operations.qs` file</span></span>
   * <span data-ttu-id="35487-152">Переименуйте его в `Bell.qs`.</span><span class="sxs-lookup"><span data-stu-id="35487-152">Rename it to `Bell.qs`</span></span>

* * *

## <a name="write-a-q-operation"></a><span data-ttu-id="35487-153">Создание операции Q#</span><span class="sxs-lookup"><span data-stu-id="35487-153">Write a Q# operation</span></span>

<span data-ttu-id="35487-154">Мы намерены подготовить два кубита в особом квантовом состоянии, на примере которых мы продемонстрируем работу с кубитами в Q#, изменяя их состояние и применяя эффекты суперпозиции и запутанности.</span><span class="sxs-lookup"><span data-stu-id="35487-154">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="35487-155">Мы создадим эту систему постепенно, описывая функции состояний кубитов, операций и измерений.</span><span class="sxs-lookup"><span data-stu-id="35487-155">We will build this up piece by piece to demonstrate qubit states, operations, and measurement.</span></span>

<span data-ttu-id="35487-156">**Обзор.**  В первом примере кода мы покажем, как работать с кубитами в Q#.</span><span class="sxs-lookup"><span data-stu-id="35487-156">**Overview:**  In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="35487-157">Мы вводим две операции `M` и `X`, которые преобразуют состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-157">We’ll introduce two operations, `M` and `X` that transform the state of a qubit.</span></span> 

<span data-ttu-id="35487-158">В этом фрагменте кода определена операция `Set`, которая принимает в качестве параметров кубит и значение состояния `desired`, в котором должен находиться этот кубит.</span><span class="sxs-lookup"><span data-stu-id="35487-158">In this code snippet, an operation `Set` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="35487-159">Операция `Set` выполняет измерение кубита с помощью операции `M`.</span><span class="sxs-lookup"><span data-stu-id="35487-159">The operation `Set` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="35487-160">В Q# измерение кубита всегда возвращает `Zero` или `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-160">In Q#, a qubit measurement always returns either  `Zero` or `One`.</span></span>  <span data-ttu-id="35487-161">Если значение, полученное в результате измерения, не совпадает с желаемым значением, операция Set инвертирует кубит. При этом выполняется операция `X`, которая изменяет состояние кубит на обратное, т. е. с противоположными вероятностями измерения значений `Zero` и `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-161">If the measurement returns a value not equal to a desired value, Set “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span>  <span data-ttu-id="35487-162">Чтобы продемонстрировать выполнение операции `Set`, после этого добавляется операция `TestBellState`.</span><span class="sxs-lookup"><span data-stu-id="35487-162">To demonstrate the effect of the `Set` operation, a `TestBellState` operation is then added.</span></span>  <span data-ttu-id="35487-163">Эта операция принимает в качестве входных данных `Zero` или `One`, вызывает для этого объекта операцию `Set` заданное количество раз, а также подсчитывает количество значений `Zero` и значений `One` в выполненных измерениях кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-163">This operation takes as input a `Zero` or `One`, and calls the `Set` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="35487-164">Разумеется, в нашей первой модели операции `TestBellState` мы ожидаем получить результат `Zero` для всех измерений кубита, определенного с помощью операции `Zero`, и результат `One` для всех измерений кубита, определенного с помощью операции `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-164">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span>  <span data-ttu-id="35487-165">Далее мы добавим в `TestBellState` код для демонстрации суперпозиции и запутанности.</span><span class="sxs-lookup"><span data-stu-id="35487-165">Further on, we’ll add code to `TestBellState` to demonstrating superposition and entanglement.</span></span>


### <a name="q-operation-code"></a><span data-ttu-id="35487-166">Код операции Q#</span><span class="sxs-lookup"><span data-stu-id="35487-166">Q# operation code</span></span>

1. <span data-ttu-id="35487-167">Замените содержимое файла Bell.qs следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="35487-167">Replace the contents of the Bell.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    <span data-ttu-id="35487-168">Теперь вы можете вызвать эту операцию, чтобы установить кубит в классическое состояние, которое в 100 % случаев возвращает одно из значений: `Zero` или `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-168">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>  <span data-ttu-id="35487-169">Константы `Zero` и `One` представляют все возможные результаты измерения кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-169">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

    <span data-ttu-id="35487-170">Операция `Set` измеряет кубит.</span><span class="sxs-lookup"><span data-stu-id="35487-170">The operation `Set` measures the qubit.</span></span>
    <span data-ttu-id="35487-171">Если кубит находится в нужном состоянии, `Set` больше не влияет на него, в противном случае мы выполняем операцию `X`, чтобы изменить состояние кубита на требуемое.</span><span class="sxs-lookup"><span data-stu-id="35487-171">If the qubit is in the state we want, `Set` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

### <a name="about-q-operations"></a><span data-ttu-id="35487-172">Сведения об операциях Q#</span><span class="sxs-lookup"><span data-stu-id="35487-172">About Q# operations</span></span>

<span data-ttu-id="35487-173">Операцией в Q# называется квантовая подпрограмма.</span><span class="sxs-lookup"><span data-stu-id="35487-173">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="35487-174">Такая вызываемая подпрограмма содержит квантовые операции.</span><span class="sxs-lookup"><span data-stu-id="35487-174">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="35487-175">Аргументы операции задаются в виде кортежа в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="35487-175">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="35487-176">Возвращаемый тип операции задается после двоеточия.</span><span class="sxs-lookup"><span data-stu-id="35487-176">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="35487-177">В нашем примере операция `Set` ничего не возвращает, поэтому для нее указан возвращаемый тип `Unit`.</span><span class="sxs-lookup"><span data-stu-id="35487-177">In this case, the `Set` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="35487-178">Эта конструкция Q# эквивалентна `unit` в F# и похожа на `void` в C# или пустой кортеж (`Tuple[()]`) в Python.</span><span class="sxs-lookup"><span data-stu-id="35487-178">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="35487-179">В первой операции на Q# вы применили две квантовые операции:</span><span class="sxs-lookup"><span data-stu-id="35487-179">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="35487-180">операция [M](xref:microsoft.quantum.intrinsic.m) измеряет состояние кубита;</span><span class="sxs-lookup"><span data-stu-id="35487-180">The [M](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="35487-181">операция [X](xref:microsoft.quantum.intrinsic.x) инвертирует состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-181">The [X](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="35487-182">Квантовая операция преобразует состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-182">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="35487-183">Иногда вместо термина "операция" применяют термин "вентиль", по аналогии с классическими логическими вентилями.</span><span class="sxs-lookup"><span data-stu-id="35487-183">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="35487-184">Это связано с тем, что на ранних этапах квантовых вычислений все алгоритмы были только теоретическими конструкциями и оформлялись в виде схем, похожих на схемы электрических контуров для классических вычислений.</span><span class="sxs-lookup"><span data-stu-id="35487-184">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="add-q-test-code"></a><span data-ttu-id="35487-185">Добавление тестового кода Q#</span><span class="sxs-lookup"><span data-stu-id="35487-185">Add Q# test code</span></span>

1. <span data-ttu-id="35487-186">В файле `Bell.qs` добавьте следующую операцию в пространство имен, сразу после операции `Set`:</span><span class="sxs-lookup"><span data-stu-id="35487-186">Add the following operation to the `Bell.qs` file, inside the namespace, after the end of the `Set` operation:</span></span>

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    <span data-ttu-id="35487-187">Эта операция (`TestBellState`) выполняет `count` раз следующий цикл: устанавливает для кубита указанное значение `initial` и измеряет результат (`M`).</span><span class="sxs-lookup"><span data-stu-id="35487-187">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="35487-188">Она собирает статистические данные о количестве нулей и единиц в измерениях, а затем возвращает эти данные вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="35487-188">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="35487-189">Она выполняет еще одну важную операцию —</span><span class="sxs-lookup"><span data-stu-id="35487-189">It performs one other necessary operation.</span></span> <span data-ttu-id="35487-190">восстановление известного состояния кубита (`Zero`) перед завершением работы, чтобы другие операции могли получить этот кубит в известном состоянии.</span><span class="sxs-lookup"><span data-stu-id="35487-190">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="35487-191">Это поведение диктуется инструкцией `using`.</span><span class="sxs-lookup"><span data-stu-id="35487-191">This is required by the `using` statement.</span></span>

### <a name="about-variables-in-q"></a><span data-ttu-id="35487-192">Сведения о переменных в Q#</span><span class="sxs-lookup"><span data-stu-id="35487-192">About variables in Q#</span></span>

<span data-ttu-id="35487-193">По умолчанию все переменные в Q# являются неизменяемыми, т. е. их значение нельзя изменить после привязки.</span><span class="sxs-lookup"><span data-stu-id="35487-193">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="35487-194">Ключевое слово `let` обозначает привязку неизменяемой переменной.</span><span class="sxs-lookup"><span data-stu-id="35487-194">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="35487-195">Аргументы операций всегда остаются неизменяемыми.</span><span class="sxs-lookup"><span data-stu-id="35487-195">Operation arguments are always immutable.</span></span>

<span data-ttu-id="35487-196">Если же вам нужна переменная, значение которой может меняться (в нашем примере это `numOnes`), объявите такую переменную с ключевым словом `mutable`.</span><span class="sxs-lookup"><span data-stu-id="35487-196">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="35487-197">Значение изменяемой переменной можно изменить с помощью инструкции `set`.</span><span class="sxs-lookup"><span data-stu-id="35487-197">A mutable variable's value may be changed using a `set` statement.</span></span>

<span data-ttu-id="35487-198">Тип переменной в обоих случаях выводится компилятором.</span><span class="sxs-lookup"><span data-stu-id="35487-198">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="35487-199">В Q# не требуется объявлять тип для переменных.</span><span class="sxs-lookup"><span data-stu-id="35487-199">Q# doesn't require any type annotations for variables.</span></span>

### <a name="about-using-statements-in-q"></a><span data-ttu-id="35487-200">Сведения об инструкциях `using` в Q#</span><span class="sxs-lookup"><span data-stu-id="35487-200">About `using` statements in Q#</span></span>

<span data-ttu-id="35487-201">В Q# есть уникальная инструкция `using`.</span><span class="sxs-lookup"><span data-stu-id="35487-201">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="35487-202">Она выделяет кубиты для использования в блоке кода.</span><span class="sxs-lookup"><span data-stu-id="35487-202">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="35487-203">Все кубиты в Q# выделяются и освобождаются динамически, а не закрепляются как фиксированные ресурсы на весь период работы сложного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="35487-203">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="35487-204">Оператор `using` выделяет набор кубитов в начале блока и освобождает их в конце блока.</span><span class="sxs-lookup"><span data-stu-id="35487-204">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="create-the-host-application-code"></a><span data-ttu-id="35487-205">Создание кода для основного приложения</span><span class="sxs-lookup"><span data-stu-id="35487-205">Create the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="35487-206">Python</span><span class="sxs-lookup"><span data-stu-id="35487-206">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="35487-207">Откройте файл `host.py` и добавьте в него следующий код.</span><span class="sxs-lookup"><span data-stu-id="35487-207">Open the `host.py` file and add the following code:</span></span>

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[<span data-ttu-id="35487-208">C#</span><span class="sxs-lookup"><span data-stu-id="35487-208">C#</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="35487-209">Замените содержимое файла `Driver.cs` приведенным ниже кодом.</span><span class="sxs-lookup"><span data-stu-id="35487-209">Replace the contents of the `Driver.cs` file with the following code:</span></span>

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a><span data-ttu-id="35487-210">Сведения о коде основного приложения</span><span class="sxs-lookup"><span data-stu-id="35487-210">About the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="35487-211">Python</span><span class="sxs-lookup"><span data-stu-id="35487-211">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="35487-212">Основное приложение на языке Python состоит из трех частей, которые выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="35487-212">The Python host application has three parts:</span></span>

* <span data-ttu-id="35487-213">Вычисление всех аргументов для квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="35487-213">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="35487-214">В нашем примере `count` получает фиксированное значение 1000, а `initial` содержит начальное состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-214">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="35487-215">Выполняет квантовый алгоритм, вызывая метод `simulate()` из импортированной операции Q#.</span><span class="sxs-lookup"><span data-stu-id="35487-215">Run the quantum algorithm by calling the `simulate()` method of the imported Q# operation.</span></span>
* <span data-ttu-id="35487-216">Обработка результата операции.</span><span class="sxs-lookup"><span data-stu-id="35487-216">Process the result of the operation.</span></span> <span data-ttu-id="35487-217">В нашем примере результат операции сохраняется в `res`.</span><span class="sxs-lookup"><span data-stu-id="35487-217">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="35487-218">Результатом здесь является кортеж с информацией о количестве нулей (`num_zeros`) и единиц (`num_ones`), полученных симулятором при измерениях.</span><span class="sxs-lookup"><span data-stu-id="35487-218">Here the result is a tuple of the number of zeros (`num_zeros`) and number of ones (`num_ones`) measured by the simulator.</span></span> <span data-ttu-id="35487-219">Мы разбираем этот кортеж на два поля и выводим эти результаты.</span><span class="sxs-lookup"><span data-stu-id="35487-219">We deconstruct the tuple to get the two fields, and print the results.</span></span>

#### <a name="c"></a>[<span data-ttu-id="35487-220">C#</span><span class="sxs-lookup"><span data-stu-id="35487-220">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="35487-221">Основное приложение на языке C# состоит из четырех частей, которые выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="35487-221">The C# host application has four parts:</span></span>

* <span data-ttu-id="35487-222">Создание квантового симулятора.</span><span class="sxs-lookup"><span data-stu-id="35487-222">Construct a quantum simulator.</span></span> <span data-ttu-id="35487-223">В нашем примере это `qsim`.</span><span class="sxs-lookup"><span data-stu-id="35487-223">In the example, `qsim` is the simulator.</span></span>
* <span data-ttu-id="35487-224">Вычисление всех аргументов для квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="35487-224">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="35487-225">В нашем примере `count` получает фиксированное значение 1000, а `initial` содержит начальное состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-225">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="35487-226">Выполнение квантового алгоритма.</span><span class="sxs-lookup"><span data-stu-id="35487-226">Run the quantum algorithm.</span></span> <span data-ttu-id="35487-227">Для каждой операции Q# создается класс C# с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="35487-227">Each Q# operation generates a C# class with the same name.</span></span> <span data-ttu-id="35487-228">Этот класс содержит метод `Run`, который **асинхронно** выполняет соответствующую операцию.</span><span class="sxs-lookup"><span data-stu-id="35487-228">This class has a `Run` method that **asynchronously** executes the operation.</span></span> <span data-ttu-id="35487-229">Асинхронное выполнение имитирует асинхронный процесс на реальном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="35487-229">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> <span data-ttu-id="35487-230">Так как метод `Run` является асинхронным, мы получаем свойство `Result`. Выполнение блокируется до тех пор, пока задача не завершится, и результат возвращается уже в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="35487-230">Because the `Run` method is asynchronous, we fetch the `Result` property; this blocks execution until the task completes and returns the result synchronously.</span></span>
* <span data-ttu-id="35487-231">Обработка результата операции.</span><span class="sxs-lookup"><span data-stu-id="35487-231">Process the result of the operation.</span></span> <span data-ttu-id="35487-232">В нашем примере результат операции сохраняется в `res`.</span><span class="sxs-lookup"><span data-stu-id="35487-232">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="35487-233">Результатом здесь является кортеж с информацией о количестве нулей (`numZeros`) и единиц (`numOnes`), полученных симулятором при измерениях.</span><span class="sxs-lookup"><span data-stu-id="35487-233">Here the result is a tuple of the number of zeros (`numZeros`) and number of ones (`numOnes`) measured by the simulator.</span></span> <span data-ttu-id="35487-234">Он возвращается в C# с типом ValueTuple.</span><span class="sxs-lookup"><span data-stu-id="35487-234">This is returned as a ValueTuple in C#.</span></span> <span data-ttu-id="35487-235">Мы разбираем этот кортеж на два поля, выводим эти результаты и ожидаем нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="35487-235">We deconstruct the tuple to get the two fields, print the results, and wait for a keypress.</span></span>

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a><span data-ttu-id="35487-236">Сборка и запуск</span><span class="sxs-lookup"><span data-stu-id="35487-236">Build and run</span></span>

#### <a name="python"></a>[<span data-ttu-id="35487-237">Python</span><span class="sxs-lookup"><span data-stu-id="35487-237">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="35487-238">Выполните следующую команду в окне терминала:</span><span class="sxs-lookup"><span data-stu-id="35487-238">Run the following command at your terminal:</span></span>

    ```
    python host.py
    ```

    <span data-ttu-id="35487-239">Эта команда запускает основное приложение, которое имитирует операцию Q#.</span><span class="sxs-lookup"><span data-stu-id="35487-239">This command runs the host application, which simulates the Q# operation.</span></span>

<span data-ttu-id="35487-240">Результаты должны выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="35487-240">The results should be:</span></span>

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="35487-241">Командная строка и Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="35487-241">Command Line / Visual Studio Code</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="35487-242">В окне терминала выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="35487-242">Run the following at your terminal:</span></span>

    ```bash
    dotnet run
    ```

    <span data-ttu-id="35487-243">Эта команда автоматически скачает все необходимые пакеты, скомпилирует приложение и запустит его в командной строке.</span><span class="sxs-lookup"><span data-stu-id="35487-243">This command will automatically download all required packages, build the application, then run it at the command line.</span></span>

1. <span data-ttu-id="35487-244">Вы также можете нажать клавишу **F1**, чтобы открыть палитру команд, и выбрать команду **Отладка: запустить без отладки.**</span><span class="sxs-lookup"><span data-stu-id="35487-244">Alternatively, press **F1** to open the Command Palette and select **Debug: Start Without Debugging.**</span></span>
<span data-ttu-id="35487-245">Возможно, вам будет предложено создать новый файл ``launch.json`` с описанием того, как запускать программу.</span><span class="sxs-lookup"><span data-stu-id="35487-245">You may be prompted to create a new ``launch.json`` file describing how to start the program.</span></span>
<span data-ttu-id="35487-246">Используемый по умолчанию вариант ``launch.json`` хорошо подходит для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="35487-246">The default ``launch.json`` should work well for most applications.</span></span>

<span data-ttu-id="35487-247">Результаты должны выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="35487-247">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[<span data-ttu-id="35487-248">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="35487-248">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="35487-249">Просто нажмите `F5` — программа автоматически скомпилируется и запустится!</span><span class="sxs-lookup"><span data-stu-id="35487-249">Just hit `F5`, and your program should build and run!</span></span>

<span data-ttu-id="35487-250">Результаты должны выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="35487-250">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

<span data-ttu-id="35487-251">Программа завершает работу после нажатия любой клавиши.</span><span class="sxs-lookup"><span data-stu-id="35487-251">The program will exit after you press a key.</span></span>

* * *

## <a name="prepare-superposition"></a><span data-ttu-id="35487-252">Подготовка суперпозиции</span><span class="sxs-lookup"><span data-stu-id="35487-252">Prepare superposition</span></span>

<span data-ttu-id="35487-253">**Обзор** Теперь давайте посмотрим, как Q# выражает методы создания суперпозиции для кубитов.</span><span class="sxs-lookup"><span data-stu-id="35487-253">**Overview** Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="35487-254">Как вы помните, кубит может находиться в суперпозиции значений 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="35487-254">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="35487-255">Для этого мы будем использовать операцию `Hadamard`.</span><span class="sxs-lookup"><span data-stu-id="35487-255">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="35487-256">Если кубит находится в одном из классических состояний (т. е. его измерение возвращает всегда `Zero` или `One`), операция `Hadamard` или `H` переведет этот кубит в такое состояние, в котором измерение с вероятностью 50 % вернет одно из значений: `Zero` или `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-256">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="35487-257">В теории можно рассматривать состояние кубита как промежуточное между `Zero` и `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-257">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="35487-258">Итак, мы смоделировали операцию `TestBellState`, и теперь в наших результатах после измерения будет примерно равное количество значений `Zero` и `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-258">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

<span data-ttu-id="35487-259">Для начала мы попробуем инвертировать кубит (если он находится в состоянии `Zero`, он перейдет в состояние `One`, и наоборот).</span><span class="sxs-lookup"><span data-stu-id="35487-259">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="35487-260">Для этого мы выполним операцию `X` до того, как измерять кубит в `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="35487-260">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="35487-261">Мы увидим, что возвращаемые после нажатия `F5` результаты теперь инвертированы:</span><span class="sxs-lookup"><span data-stu-id="35487-261">Now the results (after pressing `F5`) are reversed:</span></span>

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

<span data-ttu-id="35487-262">Но все эти действия пока не отличаются от классических вычислений.</span><span class="sxs-lookup"><span data-stu-id="35487-262">However, everything we've seen so far is classical.</span></span> <span data-ttu-id="35487-263">А мы хотим получить квантовый результат.</span><span class="sxs-lookup"><span data-stu-id="35487-263">Let's get a quantum result.</span></span> <span data-ttu-id="35487-264">Нам нужно просто заменить операцию `X` в предыдущем коде операцией `H` (вентиль Адамара).</span><span class="sxs-lookup"><span data-stu-id="35487-264">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="35487-265">Теперь мы инвертируем кубит не полностью (с 0 на 1), а в промежуточное значение.</span><span class="sxs-lookup"><span data-stu-id="35487-265">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="35487-266">Замененные строки в `TestBellState` теперь выглядят так:</span><span class="sxs-lookup"><span data-stu-id="35487-266">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="35487-267">И результат сразу становится более интересным:</span><span class="sxs-lookup"><span data-stu-id="35487-267">Now the results get more interesting:</span></span>

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

<span data-ttu-id="35487-268">При каждом измерении мы получаем классическое значение, но наш кубит находится в промежуточном состоянии (между 0 и 1), поэтому мы статистически получаем в половине случаев значение 0, а в другой половине — 1.</span><span class="sxs-lookup"><span data-stu-id="35487-268">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span> <span data-ttu-id="35487-269">Это и есть __суперпозиция__, которая дает первое реальное представление о квантовых состояниях.</span><span class="sxs-lookup"><span data-stu-id="35487-269">This is known as __superposition__ and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="35487-270">Подготовка запутанности</span><span class="sxs-lookup"><span data-stu-id="35487-270">Prepare entanglement</span></span>

<span data-ttu-id="35487-271">**Обзор.**  Теперь мы покажем, как выразить в Q# запутанность кубитов.</span><span class="sxs-lookup"><span data-stu-id="35487-271">**Overview:**  Now let’s look at how Q# expresses ways to entangle qubits.</span></span>  <span data-ttu-id="35487-272">Прежде всего мы присвоим кубиту начальное состояние, а затем с помощью операции `H` переместим его в состояние суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="35487-272">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="35487-273">Далее, прежде чем измерять первый кубит, мы применим новую операцию контролируемого отрицания `CNOT`.</span><span class="sxs-lookup"><span data-stu-id="35487-273">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-Not.</span></span>  <span data-ttu-id="35487-274">В результате выполнения этой операции второй кубит инвертируется, только если первый кубит имеет значение `One`.</span><span class="sxs-lookup"><span data-stu-id="35487-274">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="35487-275">Теперь эти два кубита являются запутанными.</span><span class="sxs-lookup"><span data-stu-id="35487-275">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="35487-276">Статистика значений для первого кубита не изменилась (распределение 50/50 для значений `Zero` и `One` после измерения), но при измерении второго кубита он теперь __всегда__ возвращает такое же состояние, как у первого кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-276">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="35487-277">Вентиль `CNOT` добавил запутанность кубитов, и любые изменения с одним из них теперь влияют и на другой.</span><span class="sxs-lookup"><span data-stu-id="35487-277">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="35487-278">Если выполнять измерения в обратном порядке (сначала второй кубит, потом первый), результат будет таким же.</span><span class="sxs-lookup"><span data-stu-id="35487-278">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="35487-279">Первое измерение дает случайный результат, а второе всегда дублирует то же значение, которое мы получили в первом.</span><span class="sxs-lookup"><span data-stu-id="35487-279">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="35487-280">Для этого мы прежде всего выделим в `TestBellState` два кубита вместо одного:</span><span class="sxs-lookup"><span data-stu-id="35487-280">The first thing we'll need to do is allocate 2 qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="35487-281">Это позволяет добавить новую операцию (`CNOT`) перед измерением (`M`) в `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="35487-281">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="35487-282">Также мы добавили операцию `Set` для инициализации первого кубита, чтобы при запуске алгоритма он всегда находился в состоянии `Zero`.</span><span class="sxs-lookup"><span data-stu-id="35487-282">We've added another `Set` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="35487-283">Также нам нужно сбросить второй кубит перед освобождением.</span><span class="sxs-lookup"><span data-stu-id="35487-283">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

<span data-ttu-id="35487-284">Полностью код метода теперь выглядит так:</span><span class="sxs-lookup"><span data-stu-id="35487-284">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="35487-285">Выполнив этот код, мы получим такое же распределение результатов (50/50), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="35487-285">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="35487-286">Но нам нужно не это, а реакция второго кубита на измерения состояния первого кубита.</span><span class="sxs-lookup"><span data-stu-id="35487-286">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="35487-287">Эту статистику мы будем собирать в новой версии операции `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="35487-287">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="35487-288">Новое возвращаемое значение (`agree`) отслеживает количество циклов, в которых измеренные состояния первого и второго кубитов совпадают.</span><span class="sxs-lookup"><span data-stu-id="35487-288">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span> <span data-ttu-id="35487-289">Также мы внесем соответствующие изменения в основное приложение:</span><span class="sxs-lookup"><span data-stu-id="35487-289">We also have to update the host application accordingly:</span></span>

#### <a name="python"></a>[<span data-ttu-id="35487-290">Python</span><span class="sxs-lookup"><span data-stu-id="35487-290">Python</span></span>](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[<span data-ttu-id="35487-291">C#</span><span class="sxs-lookup"><span data-stu-id="35487-291">C#</span></span>](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

<span data-ttu-id="35487-292">Выполнив этот проект, мы получим удивительный результат:</span><span class="sxs-lookup"><span data-stu-id="35487-292">Now when we run, we get something pretty amazing:</span></span>

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

<span data-ttu-id="35487-293">Как мы уже писали выше, статистика значений для первого кубита не изменилась (распределение 50/50 для значений 0 и 1), но при измерении второго кубита он теперь __всегда__ возвращает такое же состояние, как у первого кубита. Это и есть эффект запутанности.</span><span class="sxs-lookup"><span data-stu-id="35487-293">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

<span data-ttu-id="35487-294">Поздравляем, вы создали первую квантовую программу!</span><span class="sxs-lookup"><span data-stu-id="35487-294">Congratulations, you've written your first quantum program!</span></span>

## <a name="whats-next"></a><span data-ttu-id="35487-295">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="35487-295">What's next?</span></span>

<span data-ttu-id="35487-296">В руководстве по [алгоритму поиска Гровера](xref:microsoft.quantum.quickstarts.search) показано, как создать и применить алгоритм Гровера, один из самых популярных квантовых алгоритмов. Там вы найдете хороший пример программы на Q# для решения реальных проблем с помощью квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="35487-296">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="35487-297">В руководстве по [началу работы с Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome) вы найдете дополнительные рекомендации по изучению Q# и квантового программирования.</span><span class="sxs-lookup"><span data-stu-id="35487-297">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>

