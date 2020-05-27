---
title: Тестирование и отладка
description: Узнайте, как использовать модульные тесты, факты и утверждения и функции дампа для тестирования и отладки тактовых программ.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
ms.openlocfilehash: 374ac42255ab6b2c5eff8ab7879b3a5103181f7f
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430923"
---
# <a name="testing-and-debugging"></a>Тестирование и отладка

Как и в случае с классическим программированием, важно иметь возможность проверить, правильно ли работают тактовые программы и может ли она диагностировать неправильные тактовые программы.
В этом разделе мы рассмотрим средства, предлагаемые Q # для тестирования и отладки тактовых программ.

## <a name="unit-tests"></a>Модульные тесты

Одним из распространенных подходов к тестированию классических программ является написание небольших программ, именуемых *модульными тестами* , которые выполняют код в библиотеке и сравнивают выходные данные с ожидаемыми выходными данными.
Например, мы можем гарантировать, что возвраты будут возникать `Square(2)` `4` , так как мы узнали *приори* , что $2 ^ 2 = $4.

Q # поддерживает создание модульных тестов для тактовых программ и может выполняться как тесты в среде модульного тестирования [xUnit](https://xunit.github.io/) .

### <a name="creating-a-test-project"></a>Создание тестового проекта

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Запустите Visual Studio 2019. Перейдите в `File` меню и выберите `New`  >  `Project...` .
В верхнем правом углу найдите `Q#` и выберите `Q# Test Project` шаблон.

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

В командной строке избранного выполните следующую команду:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Новый проект будет иметь один файл `Tests.qs` , который предоставляет удобное место для определения новых модульных тестов Q #.
Изначально этот файл содержит один пример модульного теста, `AllocateQubit` который проверяет, что вновь выделенное кубит находится в {0} состоянии $ \кет $, и выводит сообщение:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

: New. Любая операция или функция Q #, которая принимает аргумент типа `Unit` и возвращает значение, `Unit` может быть помечена как модульный тест с помощью `@Test("...")` атрибута. Аргумент для этого атрибута `"QuantumSimulator"` выше указывает целевой объект, на котором выполняется тест. Один тест может выполняться на нескольких целевых объектах. Например, добавьте атрибут `@Test("ResourcesEstimator")` выше `AllocateQubit` . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Сохраните файл и выполните все тесты. Теперь должно быть два модульных теста: один, где Аллокатекубит выполняется в Куантумсимулатор, и один, где он выполняется в Ресаурцеестиматор. 

Компилятор Q # распознает встроенные целевые объекты "Куантумсимулатор", "Тоффолисимулатор" и "Ресаурцесестиматор" как допустимые целевые объекты выполнения для модульных тестов. Можно также указать любое полное имя для определения пользовательского целевого объекта выполнения. 

### <a name="running-q-unit-tests"></a>Выполнение модульных тестов Q #

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

В качестве одноразовой настройки для каждого решения перейдите в `Test` меню и выберите `Test Settings`  >  `Default Processor Architecture`  >  `X64` .

> [!TIP]
> Параметр архитектуры процессора по умолчанию для Visual Studio хранится в файле параметров решения ( `.suo` ) для каждого решения.
> При удалении этого файла необходимо `X64` снова выбрать архитектуру процессора.

Выполните сборку проекта, перейдите в `Test` меню и выберите `Windows`  >  `Test Explorer` . `AllocateQubit`будет отображаться в списке тестов в `Not Run Tests` группе. Выберите `Run All` или запустите этот отдельный тест, и он должен пройти!

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

Чтобы запустить тесты, перейдите в папку проекта (папку, содержащую `Tests.csproj` ) и выполните команду:

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

Модульные тесты можно фильтровать в соответствии с их именем и (или) целевым объектом выполнения:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

Встроенная функция <xref:microsoft.quantum.intrinsic.message> имеет тип `(String -> Unit)` и позволяет создавать сообщения диагностики.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

После выполнения теста в обозревателе тестов и нажатия кнопки тест появится панель со сведениями о выполнении теста: состояние пройдено/неудачно, затраченное время и ссылка "выходные данные". Если щелкнуть ссылку "выходные данные", тестовый вывод откроется в новом окне.

![выходные данные теста](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

Состояние "успех/сбой" для каждого теста выводится на консоль `dotnet test` .
Для неудачных тестов выходные данные также выводятся на консоль для облегчения диагностики сбоя.

***

## <a name="facts-and-assertions"></a>Факты и утверждения

Поскольку функции в Q # не имеют _логических_ побочных эффектов, любые _другие виды_ эффектов выполнения функции, тип вывода которой является пустым кортежем, `()` никогда не могут рассматриваться в программе Q #.
Таким образом, целевой компьютер может не выполнять какую-либо функцию, которая возвращает, `()` что это не приведет к изменению поведения любого следующего кода Q #.
Это позволяет функциям возвращать `()` (т. е. `Unit` ) полезные средства для внедрения утверждений и логики отладки в программы Q #. 

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

Здесь ключевое слово `fail` указывает, что вычисления не должны продолжаться, вызывая исключение на целевом компьютере, на котором выполняется программа Q #.
По определению, сбой этого вида не может рассматриваться в Q #, так как дальнейший код Q # не будет выполняться после `fail` достижения оператора.
Таким же, если мы продолжением вызова `PositivityFact` , мы можем быть уверены, что его входные данные были положительными.

Обратите внимание, что мы можем реализовать такое же поведение, как и при `PositivityFact` использовании [`Fact`](xref:microsoft.quantum.diagnostics.fact) функции из <xref:microsoft.quantum.diagnostics> пространства имен:

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

*Утверждения*, с другой стороны, используются аналогично фактам, но могут зависеть от состояния целевого компьютера. Соответственно, они определяются как операции, тогда как факты определяются как функции (как показано выше).
Чтобы понять различие, рассмотрим следующее применение факта в утверждении:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Здесь мы используем операцию, <xref:microsoft.quantum.environment.getqubitsavailabletouse> чтобы вернуть количество Кубитс, доступных для использования.
Так как это очевидно зависит от глобального состояния программы и среды выполнения, наше определение `AssertQubitsAreAvailable` должно также быть операцией.
Однако можно использовать это глобальное состояние, чтобы получить простое значение в `Bool` качестве входных данных для `Fact` функции.

Основываясь на этих идеях, [версионного](xref:microsoft.quantum.libraries.standard.prelude) предлагает два особо полезных утверждения, <xref:microsoft.quantum.intrinsic.assert> которые <xref:microsoft.quantum.intrinsic.assertprob> моделируются как операции `()` . Каждый из этих утверждений принимает Оператор Паули, описывающий определенное измерение интересов, тактовый регистр, на котором выполняется измерение, и гипотетический результат.
На целевых компьютерах, работающих по моделированию, мы не привязаны [к Теорема без клонирования](https://en.wikipedia.org/wiki/No-cloning_theorem)и могут выполнять такие измерения без нарушения регистра, передаваемого в такие утверждения.
Симулятор может, как и приведенная `PositivityFact` выше функция, прерывать вычисления, если гипотетический результат не наблюдается на практике:

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

На оборудовании физического такта, где Теорема без клонирования предотвращает исследование состояния такта, `Assert` операции и `AssertProb` просто возвращают без какого- `()` либо другого действия.

<xref:microsoft.quantum.diagnostics>Пространство имен предоставляет несколько дополнительных функций `Assert` семейства, которые позволяют проверить более сложные условия. 

## <a name="dump-functions"></a>Функции дампа

Для облегчения устранения неполадок в тактовых программах <xref:microsoft.quantum.diagnostics> пространство имен предлагает две функции, которые могут выводить дамп в файл текущее состояние целевого компьютера: <xref:microsoft.quantum.diagnostics.dumpmachine> и <xref:microsoft.quantum.diagnostics.dumpregister> . Созданные выходные данные каждого из них зависят от целевого компьютера.

### <a name="dumpmachine"></a>DumpMachine

Симулятор такта с полным состоянием, распространяемый в составе пакета разработки тактов, записывает в файл [функцию Wave](https://en.wikipedia.org/wiki/Wave_function) всей тактовой системы, в виде одномерного массива комплексных чисел, в котором каждый элемент представляет амплитуду вероятности измерения вычислительного состояния $ \кет{н} $, где $ \кет{н} = \кет{B_ {n-1}... b_1b_0} $ для BITS $ \{ b_i \} $. Например, на компьютере, где только два выделенных Кубитс и в состоянии такта $ $ \бегин{алигн} \кет{\пси} = \фрак {1} {\скрт {2} } \кет {00} -\фрак{(1 + i)} {2} \кет {10} , \енд{алигн} $ $ вызов <xref:microsoft.quantum.diagnostics.dumpmachine> создает этот результат:

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

Первая строка содержит комментарий с идентификаторами соответствующего Кубитс в значительном порядке.
Остальные строки описывают амплитуду вероятности по измерению вектора состояния базы данных $ \кет{н} $ в декартовой и полярной форматах. Подробно для первой строки:

* **`∣0❭:`** Эта строка соответствует `0` состоянию вычислительного основания
* **`0.707107 +  0.000000 i`**: амплитуда вероятности в формате Декарт.
* **` == `**: `equal` знак разписывает оба эквивалентных представления.
* **`**********  `**: Графическое представление величины, количество `*` пропорционально вероятности измерения этого вектора состояния.
* **`[ 0.500000 ]`**: числовое значение величины.
* **`    ---`**: Графическое представление фазы амплитуды (см. ниже).
* **`[ 0.0000 rad ]`**: числовое значение этапа (в радианах).

Как величина, так и фаза отображаются с графическим представлением. Представление величины прямо вперед: в нем отображается полоска `*` , чем больше вероятность, чем увеличено на полосе. Для этапа показаны следующие символы, представляющие угол на основе диапазонов:

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

В следующих примерах показаны `DumpMachine` некоторые распространенные состояния.

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
  > Идентификатор кубит назначается во время выполнения и не обязательно соответствует порядку выделения кубит или его позиции в кубит регистре.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Чтобы определить идентификатор кубит в Visual Studio, поместите точку останова в код и проверьте значение переменной кубит, например:
  > 
  > ![показывать идентификатор кубит в Visual Studio](~/media/qubit_id.png)
  >
  > Кубит с индексом `0` с `register2` идентификатором ID = `3` , кубит с индексом `1` ID = `2` .

#### <a name="command-line--visual-studio-code"></a>[Командная строка и Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Вы можете определить идентификатор кубит с помощью <xref:microsoft.quantum.intrinsic.message> функции и передать переменную кубит в сообщении, например:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > которые могут формировать этот результат:
  >```
  > 0=q:3; 1=q:2
  >```
  > Это означает, что кубит с индексом с `0` `register2` идентификатором ID = `3` , кубит с индексом `1` ID = `2` .


***

<xref:microsoft.quantum.diagnostics.dumpmachine>является частью <xref:microsoft.quantum.diagnostics> пространства имен, поэтому для его использования необходимо добавить `open` оператор:

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

<xref:microsoft.quantum.diagnostics.dumpregister>работает <xref:microsoft.quantum.diagnostics.dumpmachine> , как, за исключением того, что он также принимает массив Кубитс, чтобы ограничить объем информации, относящейся только к соответствующему Кубитс.

Как и в <xref:microsoft.quantum.diagnostics.dumpmachine> случае, сведения, созданные в, <xref:microsoft.quantum.diagnostics.dumpregister> зависят от целевого компьютера. Для имитатора с полным состоянием он записывает в файл функцию Wave вплоть до глобального этапа подсистемы такта, созданной предоставленным Кубитс в том же формате, что и <xref:microsoft.quantum.diagnostics.dumpmachine> .  Например, повторите попытку на компьютере с двумя выделенными Кубитс и в состоянии такта $ $ \бегин{алигн} \кет{\пси} = \фрак {1} {\скрт {2} } \кет {00} -\фрак{(1 + i)} {2} \кет {10} =-e ^ {-i \ PI/4} ((\фрак {1} {\скрт {2} } \кет {0} -\фрак{(1 + i)} {2} \кет {1} ) \otimes \frac{-(1 + i)} {\sqrt {2} } \ket {0} ). \end{align} $ $ вызов метода <xref:microsoft.quantum.diagnostics.dumpregister> для `qubit[0]` создает следующий результат:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

и вызов метода <xref:microsoft.quantum.diagnostics.dumpregister> для `qubit[1]` создает следующие выходные данные:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Как правило, состояние регистра, запутанными с другим регистром, находится в смешанном состоянии, а не в чистом состоянии. В этом случае <xref:microsoft.quantum.diagnostics.dumpregister> выводит следующее сообщение:

```
Qubits provided (0;) are entangled with some other qubit.
```

В следующем примере показано, как можно использовать <xref:microsoft.quantum.diagnostics.dumpregister> и <xref:microsoft.quantum.diagnostics.dumpmachine> в коде Q #:

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

Поверх `Assert` функций и `Dump` операций, Q # поддерживает подмножество стандартных возможностей отладки Visual Studio: [Установка точек останова в строке](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [пошаговое выполнение кода с помощью клавиши F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) и [Проверка значений классических переменных](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) во время выполнения кода в симуляторе.

Отладка в Visual Studio Code использует возможности отладки, предоставляемые C# для Visual Studio Code расширения на базе OmniSharp и требует установки [последней версии](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp). 