---
title: Тестирование и отладка программ
description: Узнайте, как использовать модульные тесты, факты и утверждения, а также функции сброса для тестирования и отладки квантовых программ.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030588"
---
# <a name="testing-and-debugging"></a>Тестирование и отладка

Как и в классическом программировании, важно иметь возможность проверить, что квантовые программы действуют так, как предполагалось, и быть в состоянии диагностировать квантовую программу, которая неверна.
В этом разделе мы рассмотрим инструменты, предлагаемые «Зенитом» для тестирования и отладки квантовых программ.

## <a name="unit-tests"></a>Модульные тесты

Один из распространенных подходов к тестированию классических программ заключается в написании небольших программ, называемых *модульных тестов,* которые заражают код в библиотеке, и сравнивают его выход с ожидаемым выходом.
Например, мы можем захотеть, чтобы убедиться, что `Square(2)` возвращается, `4`так как мы *знаем, априори,* что $ 2 и 4 $ 4 .

Поддерживает создание модульных тестов для квантовых программ, которые могут быть выполнены в качестве тестов в рамках модульного тестирования [xUnit.](https://xunit.github.io/)

### <a name="creating-a-test-project"></a>Создание тестового проекта

#### <a name="visual-studio-2019"></a>[Визуальная студия 2019](#tab/tabid-vs2019)

Откройте Visual Studio 2019. Перейти `File` в меню `New`  >  `Project...`и выбрать .
В правом верхнем углу `Q#`ивыберите `Q# Test Project` шаблон.

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

Из вашей любимой командной строки выполнить следующую команду:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Ваш новый проект будет `Tests.qs`иметь единый файл, который обеспечивает удобное место для определения новых модульных тестов.
Первоначально этот файл содержит `AllocateQubit` один образец модульного теста, который проверяет,{0}что вновь выделенный кубит находится в состоянии $ $ и печатает сообщение:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:новое: Любая операция или функция, которая `Unit` принимает `Unit` аргумент типа и возвращает `@Test("...")` сярприза, может быть помечена как модульный тест через атрибут. Аргумент к этому `"QuantumSimulator"` атрибуту, выше, определяет цель, на которой выполняется тест. Один тест может быть выполнен на нескольких мишенях. Например, добавьте `@Test("ResourcesEstimator")` `AllocateQubit`атрибут выше . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Сохранить файл и выполнить все тесты. Теперь должно быть два модульных теста, один из которых выполняется на Квантовом Симуляторе, и один, где он выполняется в ResourceEstimator. 

Компилятор распознает встроенные цели «КвантоваяСимулятор», «ToffoliSimulator» и «ResourcesEstimator» в качестве действительных целей выполнения для модульных тестов. Также можно указать любое полностью квалифицированное имя для определения пользовательской цели выполнения. 

### <a name="running-q-unit-tests"></a>Запуск юнитовых тестов

#### <a name="visual-studio-2019"></a>[Визуальная студия 2019](#tab/tabid-vs2019)

В качестве одноразовой установки за `Test` решение, `Test Settings`  >  `Default Processor Architecture`  > перейдите в меню и выберите. `X64`

> [!TIP]
> Настройка архитектуры процессора по умолчанию для`.suo`Visual Studio хранится в вариантах решения () файл для каждого решения.
> Если вы удалите этот файл, `X64` то вам нужно будет выбрать в качестве архитектуры процессора снова.

Создайте проект, перейдите `Test` в `Windows`  >  `Test Explorer`меню и выберите . `AllocateQubit`появится в списке тестов в `Not Run Tests` группе. Выберите `Run All` или запустите этот индивидуальный тест, и он должен пройти!

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

Для выполнения тестов перейдите в папку проекта `Tests.csproj`(папку, содержащую) и выполнить команду:

```bash
$ dotnet restore
$ dotnet test
```

Должен отобразиться результат, аналогичный приведенному ниже.

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

Единие тесты могут быть отфильтрованы в зависимости от их имени и/или цели выполнения:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

Внутренняя функция <xref:microsoft.quantum.intrinsic.message> имеет тип `(String -> Unit)` и позволяет создавать диагностические сообщения.

#### <a name="visual-studio-2019"></a>[Визуальная студия 2019](#tab/tabid-vs2019)

После выполнения теста в тестовом explorer и нажатия на тест появится панель с информацией о выполнении теста: Пройденный/Невыполненный статус, прошедшее время и ссылка "Выход". При нажатии на ссылку "Выход" результат теста откроется в новом окне.

![выход теста](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

Статус пропуска/неудачи для каждого теста печатается на консоли `dotnet test`.
Для неудачных тестов выходы также печатаются на консоли, чтобы помочь диагностировать сбой.

***

## <a name="facts-and-assertions"></a>Факты и утверждения

Так как функции в «Кью» не имеют _логических_ побочных эффектов, любые `()` _другие виды_ эффектов выполнения функции, тип вывода которой является пустым tuple, никогда не могут наблюдаться в рамках программы.
То есть, целевая машина может выбрать `()` не выполнять любую функцию, которая возвращается с гарантией того, что это упущение не изменит поведение любого следующего кода.
Это делает `()` возвращение функций `Unit`(т.е.) полезным инструментом для встраивания утверждений и отладки логики в программы. 

Рассмотрим простой пример:

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

В данном случае `fail` ключевое слово указывает на то, что вычисление не должно продолжаться, что приводит к исключению в целевой машине, работающей в программе.
По определению, сбой такого рода не может наблюдаться изнутри, так `fail` как после достижения оператора код не запускается.
Таким образом, если мы `PositivityFact`протянем мимо призыва к, мы можем быть уверены, что его вклад был положительным.

Обратите внимание, что мы `PositivityFact` можем [`Fact`](xref:microsoft.quantum.diagnostics.fact) реализовать то <xref:microsoft.quantum.diagnostics> же поведение, что и использование функции из пространства имен:

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

*Утверждения,* с другой стороны, используются аналогично фактам, но могут зависеть от состояния целевой машины. Соответственно, они определяются как операции, в то время как факты определяются как функции (как указано выше).
Чтобы понять различие, рассмотрим следующее использование факта в утверждении:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Здесь мы используем операцию, <xref:microsoft.quantum.environment.getqubitsavailabletouse> чтобы вернуть количество кубитов, доступных для использования.
Поскольку это явно зависит от глобального состояния программы и `AssertQubitsAreAvailable` ее условия исполнения, наше определение должно быть операцией.
Тем не менее, мы можем использовать `Bool` это глобальное `Fact` состояние, чтобы дать простое значение в качестве вклада в функцию.

Опираясь на эти идеи, [прелюдия](xref:microsoft.quantum.libraries.standard.prelude) предлагает <xref:microsoft.quantum.intrinsic.assert> <xref:microsoft.quantum.intrinsic.assertprob> два особенно полезных `()`утверждений, и оба моделируется как операции на . Каждый из этих утверждений принимает оператора Паули, описывающего конкретное измерение интереса, квантовый регистр, на котором должно быть выполнено измерение, и гипотетический результат.
На целевых машинах, которые работают по симуляции, мы не связаны [теоремой неклонирования,](https://en.wikipedia.org/wiki/No-cloning_theorem)и можем выполнять такие измерения, не нарушая регистр, передаваемый таким утверждениям.
Тренажер может затем, подобно `PositivityFact` функции выше, прервать вычисления, если гипотетический результат не будет наблюдаться на практике:

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

На физическом квантовом оборудовании, где теорема `Assert` без `AssertProb` клонирования `()` препятствует изучению квантового состояния, и операции просто возвращаются без каких-либо других эффектов.

Пространство <xref:microsoft.quantum.diagnostics> имен предоставляет еще несколько функций `Assert` семейства, которые позволяют нам проверить более продвинутые условия. 

## <a name="dump-functions"></a>Функции свалки

Чтобы помочь устранять <xref:microsoft.quantum.diagnostics> квантовые программы, пространство имен предлагает две функции, которые могут сбросить в файл текущее состояние целевой машины: <xref:microsoft.quantum.diagnostics.dumpmachine> и <xref:microsoft.quantum.diagnostics.dumpregister>. Генерируемый выход каждого зависит от целевой машины.

### <a name="dumpmachine"></a>DumpMachine

Полное состояние квантового симулятора, распределенного как часть Квантового набора разработки, записывает в файл [волновую функцию](https://en.wikipedia.org/wiki/Wave_function) всей квантовой системы, как одномерный массив сложных чисел, в котором каждый элемент представляет амплитуду вероятности измерения вычислительной основы состояния $'ket'n's$, где $'ket'n b_» b_1b_0 $ за биты\{\}$ b_i $. Например, на машине, в котором выделено всего два кубитов, и в квантовом состоянии $${2}(начало){00} «кет»-пси»{2} {1}(кет) — «фрак» <xref:microsoft.quantum.diagnostics.dumpmachine> (1 й) »кет{10}, «конец»выровняйте»$$

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

Первый ряд содержит комментарий с идентизациями соответствующих кубитов в их значительном порядке.
Остальные строки описывают амплитуду вероятности измерения вектора состояния основы в как в картезийском, так и в полярном форматах. Подробно для первого ряда:

* **`∣0❭:`** эта строка соответствует `0` состоянию вычислительной основы
* **`0.707107 +  0.000000 i`**: амплитуда вероятности в декартовом формате.
* **` == `**: `equal` знак разрежывает оба эквивалентных представления.
* **`**********  `**: Графическое представление величины, количество `*` пропорционально вероятности измерения этого вектора состояния.
* **`[ 0.500000 ]`**: численное значение величины
* **`    ---`**: Графическое представление фазы амплитуды (см. ниже).
* **`[ 0.0000 rad ]`**: численное значение фазы (в радиане).

И величина, и фаза отображаются с графическим представлением. Представление величины прямо вперед: он показывает `*`бар , тем больше вероятность больше бар будет. На этапе мы показываем следующие символы для представления угла на основе диапазонов:

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

Ниже приведены `DumpMachine` следующие примеры для некоторых общих состояний:

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > Идентификатор кубита назначается во время выполнения, и он не обязательно выравнивается с порядком, в котором был выделен кубит, или его положением в регистре кубита.


#### <a name="visual-studio-2019"></a>[Визуальная студия 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Вы можете выяснить идентификатор qubit в Visual Studio, поставив точку разрыва в коде и проинспектируя значение переменной кубита, например:
  > 
  > ![показать кубит ID в визуальной студии](~/media/qubit_id.png)
  >
  > кубит с `0` индексом `register2` на`3`имеет id ' `1` ,`2`кубит с индексом имеет идентификатор .

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Вы можете выяснить идентификатор qubit, используя <xref:microsoft.quantum.intrinsic.message> функцию и передавая переменную кубита в сообщении, например:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > которые могут генерировать этот выход:
  >```
  > 0=q:3; 1=q:2
  >```
  > это означает, что кубит `register2` с`3`индексом `0` на имеет `1` id`2`' , кубит с индексом имеет идентификатор .


***

<xref:microsoft.quantum.diagnostics.dumpmachine>является частью <xref:microsoft.quantum.diagnostics> пространства имен, поэтому для того, `open` чтобы использовать его, необходимо добавить заявление:

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a>DumpRegister

<xref:microsoft.quantum.diagnostics.dumpregister>работает, <xref:microsoft.quantum.diagnostics.dumpmachine>как , за исключением он также занимает массив кубитов ограничить объем информации только, что отношение к соответствующим кубитов.

Как <xref:microsoft.quantum.diagnostics.dumpmachine>и в том, что информация, генерируемая, <xref:microsoft.quantum.diagnostics.dumpregister> зависит от целевой машины. Для полного состояния квантового симулятора он записывает в файл волновой функции до глобальной фазы <xref:microsoft.quantum.diagnostics.dumpmachine>квантовой подсистемы, генерируемой предоставленными кубитов в том же формате, что и .  Например, взять еще раз машину с выделением только двух кубитов, а в квантовом{1}состоянии $$ (начало{00} выровнять) (кет-пси){10} {1}{2}{0} {2} {1} {2}{0} {2}{2} ) ( («frac»sqrt , «кет» ( «frac» (1) »кет» (кет) «время» (frac) --(1) » » » кврт кет ) , <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[0]` «конец»-выровнял»$, требуя для генерации этого вывода:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

и <xref:microsoft.quantum.diagnostics.dumpregister> призыв `qubit[1]` к генерирует этот выход:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

В целом состояние регистра, запутавого с другим регистром, является не чистым, а смешанным состоянием. В этом <xref:microsoft.quantum.diagnostics.dumpregister> случае выводит следующее сообщение:

```
Qubits provided (0;) are entangled with some other qubit.
```

Следующий пример показывает, как <xref:microsoft.quantum.diagnostics.dumpregister> можно <xref:microsoft.quantum.diagnostics.dumpmachine> использовать как, так и в коде:

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a>Отладка

Помимо `Assert` `Dump` функций и операций, компания поддерживает подмножество стандартных возможностей отладки Visual Studio: [настройка точек разрыва строки,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [прохождение кода с помощью F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) и [проверка значений классических переменных](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) — все это возможно во время выполнения кода на симуляторе.

Отладка в Visual Studio Code использует возможности отладки, предоставляемые СЗ для расширения Visual Studio Code, работающего на OmniSharp, и требует установки [последней версии.](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp) 
