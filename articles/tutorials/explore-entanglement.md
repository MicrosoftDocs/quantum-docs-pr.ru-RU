---
title: 'Изучите замкнутые с помощью Q#'
description: 'Узнайте, как написать тактовую программу в Q# . Разработка приложения, которое использует состояние Белла, с помощью Microsoft Quantum Development Kit'
author: geduardo
ms.author: v-edsanc
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 7a1a49e18ac9330ca6e3cc89b3e58c96eccb91db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691666"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="5fdc1-104">Руководство по Исследование запутанности с использованием Q\#</span><span class="sxs-lookup"><span data-stu-id="5fdc1-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="5fdc1-105">В этом учебнике мы покажем, как написать Q# программу, которая манипулирует и измеряет Кубитс и демонстрирует эффект замкнутые.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>

<span data-ttu-id="5fdc1-106">В результате у вас получится приложение Bell, которое демонстрирует квантовую запутанность.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-106">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="5fdc1-107">Имя Bell — это отсылка к состоянию Белла, которое обозначает особые квантовые состояния двух кубитов с простейшими примерами эффектов суперпозиции и квантовой запутанности.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-107">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="5fdc1-108">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="5fdc1-108">Pre-requisites</span></span>

<span data-ttu-id="5fdc1-109">Если вы готовы писать код, выполните следующие действия, прежде чем продолжать:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-109">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="5fdc1-110">[Установите](xref:microsoft.quantum.install) пакет средств разработки тактов, используя предпочитаемый язык и среду разработки.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-110">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your  preferred language and development environment.</span></span>
* <span data-ttu-id="5fdc1-111">Если эта платформа уже установлена, убедитесь, что она [обновлена](xref:microsoft.quantum.update) до последней версии.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-111">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="5fdc1-112">Вы также можете следовать инструкциям, не устанавливая КДК, просматривая обзоры Q# языка программирования и первые основные понятия тактовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-112">You can also follow along with the narrative without installing the QDK, reviewing  the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="5fdc1-113">Из этого руководства вы узнаете, как выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-113">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="5fdc1-114">Операции создания и объединения в Q\#</span><span class="sxs-lookup"><span data-stu-id="5fdc1-114">Create and combine operations in Q\#</span></span>
> * <span data-ttu-id="5fdc1-115">Создайте операции, чтобы поместить Кубитс в ентангле и измерять их.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-115">Create operations to put qubits in superposition, entangle and measure them.</span></span>
> * <span data-ttu-id="5fdc1-116">Демонстрация тактовой замкнутые с Q# программой, выполняемой в симуляторе.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-116">Demonstrate quantum entanglement with a Q# program run in a simulator.</span></span> 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a><span data-ttu-id="5fdc1-117">Демонстрация поведения кубит с помощью КДК</span><span class="sxs-lookup"><span data-stu-id="5fdc1-117">Demonstrating qubit behavior with the QDK</span></span>

<span data-ttu-id="5fdc1-118">В классическом бите хранится одно двоичное значение (0 или 1), а [кубит](xref:microsoft.quantum.glossary#qubit) может находиться в состоянии **суперпозиции** , принимая оба эти значения.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-118">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="5fdc1-119">По сути, состояние кубит можно рассматривать как направление в абстрактном пространстве (также называемом вектором).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-119">Conceptually, the state of a qubit can be thought of as a direction in an abstract space (also known as a vector).</span></span>  <span data-ttu-id="5fdc1-120">Состояние кубит может быть в любом из возможных направлений.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-120">A qubit state can be in any of the possible directions.</span></span> <span data-ttu-id="5fdc1-121">Два **классических состояния** в этой модели соответствуют двум направлениям: 100 % вероятности получить при измерении 0 и 100 % вероятности получить 1.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-121">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>

<span data-ttu-id="5fdc1-122">Измерение кубита возвращает двоичный результат и изменяет состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-122">The act of measurement produces a binary result and changes a qubit state.</span></span>
<span data-ttu-id="5fdc1-123">Измерение создает двоичное значение 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-123">Measurement  produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="5fdc1-124">При этом кубит переходит из состояния суперпозиции в одно из классических состояний.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-124">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="5fdc1-125">С этого момента все повторные измерения будут возвращать тот же двоичный результат, если не выполняются дополнительные промежуточные операции.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-125">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="5fdc1-126">Несколько кубитов могут находиться в состоянии [**запутанности**](xref:microsoft.quantum.glossary#entanglement).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-126">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span>  <span data-ttu-id="5fdc1-127">При измерении одного из запутанных кубитов мы получаем сведения о состоянии второго.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-127">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="5fdc1-128">Теперь мы готовы продемонстрировать, как Q# выражает это поведение.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-128">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="5fdc1-129">Вы начнете работу с самой простой программы и постепенно доработаете ее для демонстрации квантовой суперпозиции и квантовой запутанности.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-129">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="creating-a-no-locq-project"></a><span data-ttu-id="5fdc1-130">Создание Q# проекта</span><span class="sxs-lookup"><span data-stu-id="5fdc1-130">Creating a Q# project</span></span>

<span data-ttu-id="5fdc1-131">Первое, что нужно сделать, — это создать новый Q# проект.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-131">The first thing we have to do is to create a new Q# project.</span></span> <span data-ttu-id="5fdc1-132">В этом учебнике мы будем использовать среду на основе [ Q# приложений с VS Code](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-132">In this tutorial we are going to use the environment based on [Q# applications with VS Code](xref:microsoft.quantum.install.standalone).</span></span>

<span data-ttu-id="5fdc1-133">Чтобы создать новый проект, в VS Code:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-133">To create a new project, in VS Code:</span></span> 

1. <span data-ttu-id="5fdc1-134">Щелкните **Представление** -> **Палитра команд** и выберите **Q#: создать проект** .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-134">Click **View** -> **Command Palette** and select **Q#: Create New Project** .</span></span>
2. <span data-ttu-id="5fdc1-135">Щелкните **Standalone console application** (Автономное консольное приложение).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-135">Click **Standalone console application** .</span></span>
3. <span data-ttu-id="5fdc1-136">Перейдите к расположению, в котором нужно сохранить проект, и щелкните **Создать проект** .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-136">Navigate to the location to save the project and click **Create Project** .</span></span>
4. <span data-ttu-id="5fdc1-137">После успешного создания проекта нажмите **Открыть новый проект...** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-137">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="5fdc1-138">В этом случае мы назвали проект `Bell` .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-138">In this case we called the project `Bell`.</span></span> <span data-ttu-id="5fdc1-139">Это приводит к созданию двух файлов: `Bell.csproj` , файла проекта и `Program.qs` шаблона Q# приложения, которое будет использоваться для написания нашего приложения.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-139">This generates two files: `Bell.csproj`, the project file and `Program.qs`, a template of a Q# application that we will use to write our application.</span></span> <span data-ttu-id="5fdc1-140">Содержимое `Program.qs` должно быть следующим:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-140">The content of `Program.qs` should be:</span></span>

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a><span data-ttu-id="5fdc1-141">Написание \# приложения Q</span><span class="sxs-lookup"><span data-stu-id="5fdc1-141">Write the Q\# application</span></span>
 
<span data-ttu-id="5fdc1-142">Нашей целью является подготовка двух Кубитс в определенном состоянии такта, демонстрация работы с Кубитс с Q# целью изменения их состояния и демонстрации эффектов замкнутые.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-142">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="5fdc1-143">Мы создадим этот фрагмент по части для представления кубитных состояний, операций и измерений.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-143">We will build this up piece by piece to introduce qubit states, operations, and measurement.</span></span>

### <a name="initialize-qubit-using-measurement"></a><span data-ttu-id="5fdc1-144">Инициализация кубит с помощью измерения</span><span class="sxs-lookup"><span data-stu-id="5fdc1-144">Initialize qubit using measurement</span></span>

<span data-ttu-id="5fdc1-145">В первом фрагменте кода ниже показано, как работать с Кубитс в Q# .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-145">In the first code snippet below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="5fdc1-146">Мы предоставим две операции, [`M`](xref:Microsoft.Quantum.Intrinsic.m) [`X`](xref:Microsoft.Quantum.Intrinsic.X) которые преобразуют состояние кубит.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-146">We’ll introduce two operations, [`M`](xref:Microsoft.Quantum.Intrinsic.m) and [`X`](xref:Microsoft.Quantum.Intrinsic.X) that transform the state of a qubit.</span></span> <span data-ttu-id="5fdc1-147">В этом фрагменте кода определена операция `SetQubitState`, которая принимает в качестве параметров кубит и значение состояния `desired`, в котором должен находиться этот кубит.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-147">In this code snippet, an operation `SetQubitState` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="5fdc1-148">Операция `SetQubitState` выполняет измерение кубита с помощью операции `M`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-148">The operation `SetQubitState` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="5fdc1-149">В Q# кубит измерение всегда возвращает значение `Zero` или `One` .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-149">In Q#, a qubit measurement always returns either `Zero` or `One`.</span></span>  <span data-ttu-id="5fdc1-150">Если измерение возвращает значение, не равное желаемому значению, `SetQubitState` "переворачивает" кубит, то есть выполняет `X` операцию, которая изменяет состояние кубит на новое состояние, в котором вероятности возврата и изменения значений измерений меняются `Zero` `One` местами.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-150">If the measurement returns a value not equal to the desired value, `SetQubitState` “flips” the qubit; that is, it runs an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span> <span data-ttu-id="5fdc1-151">Таким образом `SetQubitState` Целевая кубит всегда помещается в нужное состояние.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-151">This way, `SetQubitState` always puts the target qubit in the desired state.</span></span>

<span data-ttu-id="5fdc1-152">Замените содержимое `Program.qs` следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-152">Replace the contents of `Program.qs` with the following code:</span></span>


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

<span data-ttu-id="5fdc1-153">Теперь вы можете вызвать эту операцию, чтобы установить кубит в классическое состояние, которое в 100 % случаев возвращает одно из значений: `Zero` или `One`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-153">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>
<span data-ttu-id="5fdc1-154">Константы `Zero` и `One` представляют все возможные результаты измерения кубита.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-154">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

<span data-ttu-id="5fdc1-155">Операция `SetQubitState` измеряет кубит.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-155">The operation `SetQubitState` measures the qubit.</span></span> <span data-ttu-id="5fdc1-156">Если кубит находится в нужном состоянии, `SetQubitState` оставляет его только один. в противном случае, выполнив `X` операцию, мы изменим состояние кубит на нужное.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-156">If the qubit is in the state we want, `SetQubitState` leaves it alone; otherwise, by running the `X` operation, we change the qubit state to the desired state.</span></span>

#### <a name="about-no-locq-operations"></a><span data-ttu-id="5fdc1-157">Сведения об Q# операциях</span><span class="sxs-lookup"><span data-stu-id="5fdc1-157">About Q# operations</span></span>

<span data-ttu-id="5fdc1-158">Q#Операция — это подпрограммы такта.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-158">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="5fdc1-159">То есть это вызываемая подпрограммы, которая содержит вызовы других тактовых операций.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-159">That is, it is a callable routine that contains calls to other quantum operations.</span></span>

<span data-ttu-id="5fdc1-160">Аргументы операции задаются в виде кортежа в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-160">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="5fdc1-161">Возвращаемый тип операции задается после двоеточия.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-161">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="5fdc1-162">В этом случае `SetQubitState` операция не имеет возвращаемого типа, поэтому она помечается как возвращаемая `Unit` .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-162">In this case, the `SetQubitState` operation has no return type, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="5fdc1-163">Это Q# эквивалент `unit` в F #, который примерно аналогичен `void` в C#, и пустой кортеж в Python ( `()` представленный указанием типа `Tuple[()]` ).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-163">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple in Python (`()`, represented by the type hint `Tuple[()]`).</span></span>

<span data-ttu-id="5fdc1-164">В первой операции вы использовали две тактовые операции Q# :</span><span class="sxs-lookup"><span data-stu-id="5fdc1-164">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="5fdc1-165">[`M`](xref:Microsoft.Quantum.Intrinsic.m)Операция, которая измеряет состояние кубит</span><span class="sxs-lookup"><span data-stu-id="5fdc1-165">The [`M`](xref:Microsoft.Quantum.Intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="5fdc1-166">[`X`](xref:Microsoft.Quantum.Intrinsic.X)Операция, которая отражает состояние кубит</span><span class="sxs-lookup"><span data-stu-id="5fdc1-166">The [`X`](xref:Microsoft.Quantum.Intrinsic.X) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="5fdc1-167">Квантовая операция преобразует состояние кубита.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-167">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="5fdc1-168">Иногда вместо термина "операция" применяют термин "вентиль", по аналогии с классическими логическими вентилями.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-168">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="5fdc1-169">Это связано с тем, что на ранних этапах квантовых вычислений все алгоритмы были только теоретическими конструкциями и оформлялись в виде схем, похожих на схемы электрических контуров для классических вычислений.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-169">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="counting-measurement-outcomes"></a><span data-ttu-id="5fdc1-170">Подсчет результатов измерения</span><span class="sxs-lookup"><span data-stu-id="5fdc1-170">Counting measurement outcomes</span></span>

<span data-ttu-id="5fdc1-171">Чтобы продемонстрировать выполнение операции `SetQubitState`, после этого добавляется операция `TestBellState`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-171">To demonstrate the effect of the `SetQubitState` operation, a `TestBellState` operation is then added.</span></span> <span data-ttu-id="5fdc1-172">Эта операция принимает в качестве входных данных `Zero` или `One`, вызывает для этого объекта операцию `SetQubitState` заданное количество раз, а также подсчитывает количество значений `Zero` и значений `One` в выполненных измерениях кубита.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-172">This operation takes as input a `Zero` or `One`, and calls the `SetQubitState` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="5fdc1-173">Разумеется, в нашей первой модели операции `TestBellState` мы ожидаем получить результат `Zero` для всех измерений кубита, определенного с помощью операции `Zero`, и результат `One` для всех измерений кубита, определенного с помощью операции `One`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-173">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span> <span data-ttu-id="5fdc1-174">Далее мы добавим код в, `TestBellState` чтобы продемонстрировать замкнутые.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-174">Further on, we’ll add code to `TestBellState` to demonstrate superposition and entanglement.</span></span>

<span data-ttu-id="5fdc1-175">В файле `Program.qs` добавьте следующую операцию в пространство имен, сразу после операции `SetQubitState`:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-175">Add the following operation to the `Program.qs` file, inside the namespace, after the end of the `SetQubitState` operation:</span></span>

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
<span data-ttu-id="5fdc1-176">Обратите внимание, что мы добавили строку перед `return` печатью пояснительного сообщения в консоли с помощью функции ( `Message` ) [Microsoft. тактов. Inline. Message].</span><span class="sxs-lookup"><span data-stu-id="5fdc1-176">Note that we added a line before the `return` to print an explanatory message in the console with the function (`Message`)[microsoft.quantum.intrinsic.message]</span></span>

<span data-ttu-id="5fdc1-177">Эта операция (`TestBellState`) выполняет `count` раз следующий цикл: устанавливает для кубита указанное значение `initial` и измеряет результат (`M`).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-177">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="5fdc1-178">Она собирает статистические данные о количестве нулей и единиц в измерениях, а затем возвращает эти данные вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-178">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="5fdc1-179">Она выполняет еще одну важную операцию —</span><span class="sxs-lookup"><span data-stu-id="5fdc1-179">It performs one other necessary operation.</span></span> <span data-ttu-id="5fdc1-180">восстановление известного состояния кубита (`Zero`) перед завершением работы, чтобы другие операции могли получить этот кубит в известном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-180">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="5fdc1-181">Это поведение диктуется инструкцией `using`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-181">This is required by the `using` statement.</span></span>

#### <a name="about-variables-in-q"></a><span data-ttu-id="5fdc1-182">О переменных в Q\#</span><span class="sxs-lookup"><span data-stu-id="5fdc1-182">About variables in Q\#</span></span>

<span data-ttu-id="5fdc1-183">По умолчанию переменные в Q# являются неизменяемыми; их значения не могут изменяться после их привязки.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-183">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="5fdc1-184">Ключевое слово `let` обозначает привязку неизменяемой переменной.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-184">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="5fdc1-185">Аргументы операций всегда остаются неизменяемыми.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-185">Operation arguments are always immutable.</span></span>

<span data-ttu-id="5fdc1-186">Если же вам нужна переменная, значение которой может меняться (в нашем примере это `numOnes`), объявите такую переменную с ключевым словом `mutable`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-186">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="5fdc1-187">Значение изменяемой переменной можно изменить с помощью инструкции `set`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-187">A mutable variable's value may be changed using a `set` statement.</span></span>

<span data-ttu-id="5fdc1-188">Тип переменной в обоих случаях выводится компилятором.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-188">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="5fdc1-189">Q# не требует никаких аннотаций типа для переменных.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-189">Q# doesn't require any type annotations for variables.</span></span>

#### <a name="about-using-statements-in-q"></a><span data-ttu-id="5fdc1-190">О `using` инструкциях в Q\#</span><span class="sxs-lookup"><span data-stu-id="5fdc1-190">About `using` statements in Q\#</span></span>

<span data-ttu-id="5fdc1-191">`using`Оператор также является специальным для Q# .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-191">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="5fdc1-192">Она выделяет кубиты для использования в блоке кода.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-192">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="5fdc1-193">В Q# все Кубитс динамически выделяются и освобождаются, вместо фиксированных ресурсов, которые находятся в течение всего времени существования сложного алгоритма.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-193">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="5fdc1-194">Оператор `using` выделяет набор кубитов в начале блока и освобождает их в конце блока.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-194">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="run-the-code-from-the-command-prompt"></a><span data-ttu-id="5fdc1-195">Запуск кода из командной строки</span><span class="sxs-lookup"><span data-stu-id="5fdc1-195">Run the code from the command prompt</span></span>

<span data-ttu-id="5fdc1-196">Чтобы выполнить код, необходимо сообщить компилятору, *что* вызываемый объект должен запускаться при вводе `dotnet run` команды.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-196">In order to run the code we need to tell the compiler *which* callable to run when we provide the `dotnet run` command.</span></span> <span data-ttu-id="5fdc1-197">Это делается простым изменением в Q# файле путем добавления строки, `@EntryPoint()` непосредственно предшествующей вызываемой: в `TestBellState` этом случае операция.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-197">This is done with a simple change in the Q# file by adding a line with `@EntryPoint()` directly preceding the callable: the `TestBellState` operation in this case.</span></span> <span data-ttu-id="5fdc1-198">Полный код должен быть следующим:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-198">The full code should be:</span></span>

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

<span data-ttu-id="5fdc1-199">Чтобы запустить программу, необходимо указать `count` аргументы и в `initial` командной строке.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-199">To run the program we need to specify `count` and `initial` arguments from the command prompt.</span></span> <span data-ttu-id="5fdc1-200">Давайте рассмотрим пример `count = 1000` и `initial = One` .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-200">Let's choose for example `count = 1000` and `initial = One`.</span></span> <span data-ttu-id="5fdc1-201">Введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-201">Enter the following command:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

<span data-ttu-id="5fdc1-202">Обратите внимание на следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-202">And you should observe the following output:</span></span>

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="5fdc1-203">Если вы попробуете с вами, выполните `initial = Zero` следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-203">If you try with `initial = Zero` you should observe:</span></span>

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a><span data-ttu-id="5fdc1-204">Подготовка суперпозиции</span><span class="sxs-lookup"><span data-stu-id="5fdc1-204">Prepare superposition</span></span>

<span data-ttu-id="5fdc1-205">Теперь давайте посмотрим, как Q# выражают способы размещения Кубитс в крайнем положении.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-205">Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="5fdc1-206">Как вы помните, кубит может находиться в суперпозиции значений 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-206">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="5fdc1-207">Для этого мы будем использовать операцию `Hadamard`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-207">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="5fdc1-208">Если кубит находится в одном из классических состояний (т. е. его измерение возвращает всегда `Zero` или `One`), операция `Hadamard` или `H` переведет этот кубит в такое состояние, в котором измерение с вероятностью 50 % вернет одно из значений: `Zero` или `One`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-208">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="5fdc1-209">В теории можно рассматривать состояние кубита как промежуточное между `Zero` и `One`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-209">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="5fdc1-210">Итак, мы смоделировали операцию `TestBellState`, и теперь в наших результатах после измерения будет примерно равное количество значений `Zero` и `One`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-210">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

### <a name="x-flips-qubit-state"></a><span data-ttu-id="5fdc1-211">`X` переворачивает состояние кубит</span><span class="sxs-lookup"><span data-stu-id="5fdc1-211">`X` flips qubit state</span></span>

<span data-ttu-id="5fdc1-212">Сначала мы попытаемся перевернуть кубит (если кубит находится в `Zero` состоянии, он будет перевернут `One` и наоборот).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-212">First we'll just try to flip the qubit (if the qubit is in `Zero` state it will flip to `One` and vice versa).</span></span> <span data-ttu-id="5fdc1-213">Для этого мы выполним операцию `X` до того, как измерять кубит в `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-213">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="5fdc1-214">Теперь результаты будут реверсированы:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-214">Now the results are reversed:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="5fdc1-215">Теперь давайте рассмотрим свойства такта Кубитс.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-215">Now let's explore the quantum properties of the qubits.</span></span>

### <a name="h-prepares-superposition"></a><span data-ttu-id="5fdc1-216">`H` подготавливает подстановку</span><span class="sxs-lookup"><span data-stu-id="5fdc1-216">`H` prepares superposition</span></span>

<span data-ttu-id="5fdc1-217">Нам нужно просто заменить операцию `X` в предыдущем коде операцией `H` (вентиль Адамара).</span><span class="sxs-lookup"><span data-stu-id="5fdc1-217">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="5fdc1-218">Теперь мы инвертируем кубит не полностью (с 0 на 1), а в промежуточное значение.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-218">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="5fdc1-219">Замененные строки в `TestBellState` теперь выглядят так:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-219">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="5fdc1-220">И результат сразу становится более интересным:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-220">Now the results get more interesting:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

<span data-ttu-id="5fdc1-221">При каждом измерении мы получаем классическое значение, но наш кубит находится в промежуточном состоянии (между 0 и 1), поэтому мы статистически получаем в половине случаев значение 0, а в другой половине — 1.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-221">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span>
<span data-ttu-id="5fdc1-222">Это и есть **суперпозиция** , которая дает первое реальное представление о квантовых состояниях.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-222">This is known as **superposition** and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="5fdc1-223">Подготовка запутанности</span><span class="sxs-lookup"><span data-stu-id="5fdc1-223">Prepare entanglement</span></span>

<span data-ttu-id="5fdc1-224">Теперь давайте посмотрим, как Q# выражает способы ентангле Кубитс.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-224">Now let’s look at how Q# expresses ways to entangle qubits.</span></span>
<span data-ttu-id="5fdc1-225">Прежде всего мы присвоим кубиту начальное состояние, а затем с помощью операции `H` переместим его в состояние суперпозиции.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-225">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="5fdc1-226">Затем, прежде чем измерять первый кубит, мы используем новую операцию ( `CNOT` ), которая означает *контролируемый* .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-226">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for *Controlled-NOT* .</span></span>  <span data-ttu-id="5fdc1-227">Результат выполнения этой операции с двумя кубитсами заключается в том, чтобы перевернуть второй кубит, если первый кубит имеет значение `One` .</span><span class="sxs-lookup"><span data-stu-id="5fdc1-227">The result of running this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="5fdc1-228">Теперь эти два кубита являются запутанными.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-228">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="5fdc1-229">Статистика значений для первого кубита не изменилась (распределение 50/50 для значений `Zero` и `One` после измерения), но при измерении второго кубита он теперь __всегда__ возвращает такое же состояние, как у первого кубита.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-229">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="5fdc1-230">Вентиль `CNOT` добавил запутанность кубитов, и любые изменения с одним из них теперь влияют и на другой.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-230">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="5fdc1-231">Если выполнять измерения в обратном порядке (сначала второй кубит, потом первый), результат будет таким же.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-231">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="5fdc1-232">Первое измерение дает случайный результат, а второе всегда дублирует то же значение, которое мы получили в первом.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-232">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="5fdc1-233">Первое, что нужно сделать, — это выделить два Кубитс вместо одного в `TestBellState` :</span><span class="sxs-lookup"><span data-stu-id="5fdc1-233">The first thing we'll need to do is allocate two qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="5fdc1-234">Это позволяет добавить новую операцию (`CNOT`) перед измерением (`M`) в `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-234">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="5fdc1-235">Также мы добавили операцию `SetQubitState` для инициализации первого кубита, чтобы при запуске алгоритма он всегда находился в состоянии `Zero`.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-235">We've added another `SetQubitState` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="5fdc1-236">Также нам нужно сбросить второй кубит перед освобождением.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-236">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

<span data-ttu-id="5fdc1-237">Полностью код метода теперь выглядит так:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-237">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="5fdc1-238">Выполнив этот код, мы получим такое же распределение результатов (50/50), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-238">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="5fdc1-239">Но нам нужно не это, а реакция второго кубита на измерения состояния первого кубита.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-239">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="5fdc1-240">Эту статистику мы будем собирать в новой версии операции `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-240">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

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
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="5fdc1-241">Новое возвращаемое значение (`agree`) отслеживает количество циклов, в которых измеренные состояния первого и второго кубитов совпадают.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-241">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span>

<span data-ttu-id="5fdc1-242">Выполнение полученного кода:</span><span class="sxs-lookup"><span data-stu-id="5fdc1-242">Running the code we obtain:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

<span data-ttu-id="5fdc1-243">Как мы уже писали выше, статистика значений для первого кубита не изменилась (распределение 50/50 для значений 0 и 1), но при измерении второго кубита он теперь __всегда__ возвращает такое же состояние, как у первого кубита. Это и есть эффект запутанности.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-243">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

## <a name="next-steps"></a><span data-ttu-id="5fdc1-244">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5fdc1-244">Next steps</span></span>

<span data-ttu-id="5fdc1-245">В руководстве по [поиску Гровер](xref:microsoft.quantum.quickstarts.search) показано, как создать и запустить поиск Гровер, один из наиболее популярных алгоритмов тактовой частоты и предлагает хороший пример Q# программы, которую можно использовать для решения реальных проблем с тактовыми вычислениями.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-245">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="5fdc1-246">Приступая к [работе с пакетом разработки тактовой](xref:microsoft.quantum.welcome) программы порекомендует больше способов изучения Q# и тактовой программирования.</span><span class="sxs-lookup"><span data-stu-id="5fdc1-246">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>
