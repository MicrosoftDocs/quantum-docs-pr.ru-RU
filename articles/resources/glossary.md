---
Title: описание для глоссария тактовых вычислений: Глоссарий общих терминов, действий и объектов, используемых в тактовых вычислениях.
Автор: брадбен MS. author: v-бенбра MS. Дата: 9/1/2020 MS. Topic: статья UID: Microsoft. тактов. Глоссарий No-Loc:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="quantum-computing-glossary"></a>Глоссарий по тактовым вычислениям

## <a name="adjoint"></a>Прилегающий

Комплексно сопряженное перестановка [операции](xref:microsoft.quantum.glossary#operation). Для операций, реализующих оператор с [единым](xref:microsoft.quantum.glossary#unitary-operator) , примыкающим является обратная операция и обозначается символом дагжер. Например, если операция `U` представляет собой оператор $ u $ , то `Adjoint U` представляет $ u ^ \dagger $ . Дополнительные сведения см. в разделе [прилегающие](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).

## <a name="ancilla"></a>анЦилла

[Кубит](xref:microsoft.quantum.glossary#qubit) , который служит временной памятью для тактового компьютера и выделяется и освобождается по мере необходимости.  Дополнительные сведения см. в разделе [несколько Кубитс](xref:microsoft.quantum.concepts.multiple-qubits).

## <a name="bell-state"></a>Состояние колокольчика

Одно из четырех конкретных [запутанными](xref:microsoft.quantum.glossary#entanglement) [состояний такта](xref:microsoft.quantum.glossary#quantum-state) двух Кубитс. Четыре состояния определяются $ \ket { \beta как _ { ИЖ } } = ( \mathbb { I } \otimes X ^ iz ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ . Состояние колокольчика также называется [парой EPR](xref:microsoft.quantum.glossary#epr-pair).

## <a name="bloch-sphere"></a>БЛОЧ шар

Графическое представление[однокубитного](xref:microsoft.quantum.glossary#qubit) [состояния такта](xref:microsoft.quantum.glossary#quantum-state) в виде точки трехмерной единичной сферы. Дополнительные сведения см.  [в разделе визуализация Кубитс и преобразований с помощью сферы БЛОЧ](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).

## <a name="callable"></a>Предназначен

[Операция](xref:microsoft.quantum.glossary#operation) или [функция](xref:microsoft.quantum.glossary#function) Q# языка. Дополнительные сведения см. в разделе [операции и функции](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="clifford-group"></a>Группа Клиффорд

Набор операций, которые занимают октантс [БЛОЧ Sphere](xref:microsoft.quantum.glossary#bloch-sphere) и влияют на перестановки [операторов Паули](xref:microsoft.quantum.glossary#pauli-operators). К ним относятся операции [ $ X $ ](xref:microsoft.quantum.intrinsic.x), [ $ Y $ ](xref:microsoft.quantum.intrinsic.y), [ $ Z $ ](xref:microsoft.quantum.intrinsic.z), [ $ H $ ](xref:microsoft.quantum.intrinsic.h) и [ $ S $ ](xref:microsoft.quantum.intrinsic.s).

## <a name="controlled"></a>Управляет

[Операция](xref:microsoft.quantum.glossary#operation) -такт, которая принимает один или несколько [Кубитс](xref:microsoft.quantum.glossary#qubit) как созидателями для целевой операции. Дополнительные сведения см. в разделе [контролируемые и смежные операции](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).

## <a name="dirac-notation"></a>Нотация Дирак

Символьная Краткая форма, упрощающая представление [состояний тактов](xref:microsoft.quantum.glossary#quantum-state), также называемая нотацией *неверное-Сисакет* .  *Неверное* часть представляет вектор строки, например a $ \bra { } = \begin{bmatrix} { _1 } & { _2 } \end{bmatrix} $ , а *Сисакет* представляет собой вектор столбца, $ \ket { b } = \begin{bmatrix} b { _1 } \\\\ b { _2 } \end{bmatrix} $ . Дополнительные сведения см. в разделе [Дирак Notation](xref:microsoft.quantum.concepts.dirac).

## <a name="eigenvalue"></a>еиженвалуе

Коэффициент, на который изменяется величина [еиженвектор](xref:microsoft.quantum.glossary#eigenvector) данного преобразования при преобразовании приложением преобразования.  При наличии квадратной матрицы $ M $ и еиженвектор $ v $ , затем $ MV = ОПС $ , где $ c $ — это еиженвалуе и может быть комплексным числом любого аргумента. Дополнительные сведения см. в разделе [Расширенные понятия матрицы](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="eigenvector"></a>еиженвектор

Вектор, направление которого не изменилось заданным преобразованием и величина которого изменяется коэффициентом, соответствующим [еиженвалуеу](xref:microsoft.quantum.glossary#eigenvalue)вектора. При наличии квадратной матрицы $ M $ и еиженвалуе $ c $ , затем $ MV = ОПС $ , где $ v $ является еиженвектор матрицы и может быть комплексным числом любого аргумента. Дополнительные сведения см. в разделе [Расширенные понятия матрицы](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="entanglement"></a>Запутанность

Частицы тактов, такие как [Кубитс](xref:microsoft.quantum.glossary#qubit), могут быть подключены или *запутанными* таким образом, что их нельзя описать независимо друг от друга. Результаты измерений сопоставлены, даже если они разделены бесконечно далеко. Замкнутые важно для [измерения](xref:microsoft.quantum.glossary#measurement) [состояния](xref:microsoft.quantum.glossary#quantum-state) кубит.  Дополнительные сведения см. в разделе [Расширенные понятия матрицы](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="epr-pair"></a>Пара EPR

Одно из четырех конкретных запутанными [состояний такта](xref:microsoft.quantum.glossary#quantum-state) двух [Кубитс](xref:microsoft.quantum.glossary#qubit). Четыре состояния определяются как $ \ket { \beta _ { ИЖ } } = ( \mathbb { 1 } \otimes X ^ iz ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ . Пара EPR называется также [состоянием колокольчика](xref:microsoft.quantum.glossary#bell-state)

## <a name="evolution"></a>Результатом

Изменение [состояния такта](xref:microsoft.quantum.glossary#quantum-state) со временем. Дополнительные сведения см. в разделе [экспонента матрицы](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).

## <a name="function"></a>Компонент
Тип подпрограммы на Q# языке, который является чисто классическим (не в такте). Хотя функции используются в алгоритмах такта, они не могут действовать в [операциях](xref:microsoft.quantum.glossary#operation) [Кубитс](xref:microsoft.quantum.glossary#qubit) или Call. Дополнительные сведения см. в разделе [операции и функции](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="gate"></a>Frame

Устаревший термин для [операции](xref:microsoft.quantum.glossary#operation)с тактом, основанный на концепции классических логик шлюзов. [Тактовая цепь](xref:microsoft.quantum.glossary#quantum-circuit-diagram) — это сеть шлюзов (или операций), основанная на аналогичной концепции классических логических цепей.

## <a name="global-phase"></a>Глобальный этап

Если два [состояния](xref:microsoft.quantum.glossary#quantum-state) идентичны кратному комплексному числу $ e ^ { i \phi } $ , то говорят, что они отличаются глобальным этапом. В отличие от локальных фаз, глобальные фазы не могут быть просмотрены через любые [меасурмент](xref:microsoft.quantum.glossary#measurement). Дополнительные сведения см. [в разделе кубит](xref:microsoft.quantum.concepts.qubit).

## <a name="hadamard"></a>Hadamard

Операция хадамард (также называемая хадамардным шлюзом или преобразованием) действует на одном [кубит](xref:microsoft.quantum.glossary#qubit) и помещает ее [в четное](xref:microsoft.quantum.glossary#superposition) значение $ \ket { 0 } $ или $ \ket { 1, } $ Если кубит изначально находится в $ \ket { } $ состоянии 0. В Q# Эта операция применяется в предварительно определенной [`H`](xref:microsoft.quantum.intrinsic.h) операции.

## <a name="immutable"></a>Неизменяемые

Переменная, значение которой нельзя изменить. Неизменяемая переменная в создается Q# с помощью `let` ключевого слова. Чтобы объявить переменные, которые *могут* быть изменены, используйте ключевое слово [mutable](xref:microsoft.quantum.glossary#immutable) для объявления и `set` ключевого слова для изменения значения. 

## <a name="measurement"></a>Измерения

Обработка [кубит](xref:microsoft.quantum.glossary#qubit) (или набора Кубитс), которая дает результат наблюдения, в результате получения классического бита. Дополнительные сведения см. [в разделе кубит](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).

## <a name="mutable"></a>Изменяемый

Переменная, значение которой можно изменить после ее создания. Изменяемая переменная в Q# объявляется с помощью `mutable` ключевого слова и изменяется с помощью `set` ключевого слова. Переменные, созданные с помощью `let` ключевого слова, являются [неизменяемыми](xref:microsoft.quantum.glossary#immutable) , и их значения нельзя изменить.

## <a name="namespace"></a>Пространство имен

Метка для коллекции связанных имен (т. е. [операций](xref:microsoft.quantum.glossary#operation), [функций](xref:microsoft.quantum.glossary#function)и [определяемых пользователем типов](xref:microsoft.quantum.glossary#user-defined-type)). Например, пространство имен [Microsoft. тактов. Подготовка](xref:microsoft.quantum.preparation) помечает все символы, определенные в стандартной библиотеке и помогающие при подготовке начальных состояний.

## <a name="operation"></a>Операция

Базовая единица вычислений тактов в Q# . Он примерно эквивалентен функции в C, C++ или Python или статическом методе в C# или Java. Дополнительные сведения см. в разделе [операции и функции](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="operator-application"></a>Приложение оператора

Выполнение операции над тактом. Обычно это применяет единую матрицу к текущему вектору состояния такта.

## <a name="oracle"></a>Oracle;

Подпрограммы, которая предоставляет зависящую от данных информацию в алгоритме такта во время выполнения. Как правило, целью является [предоставление части выходных](xref:microsoft.quantum.glossary#superposition) данных, соответствующих входным данным, находящимся в части. Дополнительные сведения см. в разделе [Oracle](xref:microsoft.quantum.libraries.data-structures#oracles).

## <a name="partial-application"></a>Частичное приложение

Вызов [функции](xref:microsoft.quantum.glossary#function) или [операции](xref:microsoft.quantum.glossary#operation) без всех необходимых входных данных. Он возвращает новый [вызываемый](xref:microsoft.quantum.glossary#callable) объект, которому требуются только отсутствующие параметры (обозначенные символом подчеркивания), которые должны быть предоставлены в будущем приложении. Например, при наличии функции `MyFunc(x : int, y : int) : int {return x + y;}` можно частично применить ее к новой функции `let NewFunc = MyFunc(_, 3)` . Затем можно вызвать новую функцию позднее с отсутствующим параметром, `NewFunc(2)` который возвращает значение *5*.  Дополнительные сведения см. в разделе [частичное применение](xref:microsoft.quantum.guide.operationsfunctions#partial-application).

## <a name="pauli-operators"></a>Операторы Паули

Набор из трех одноединых матриц 2 x 2, которые называются `X` `Y` и `Z` тактовыми операциями. Матрица идентификации, $ I $ , часто также включается в набор.  $1 0 0 = \begin{bmatrix} & \\\\ & 1 \end{bmatrix} $ , $ X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} $ , $ Y = \begin{bmatrix} 0 & -i 0 \\\\ & \end{bmatrix} $ , $ Z 1 0 = \begin{bmatrix} & \\\\ & -1 \end{bmatrix} $ .   Дополнительные сведения см. в статье [Single-кубит Operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).

## <a name="quantum-circuit-diagram"></a>Схема тактовой цепи

Метод для графического представления последовательности [операций](xref:microsoft.quantum.glossary#operation) (или [шлюзов](xref:microsoft.quantum.glossary#gate)) для простых тактовых программ, например 

![Образец схемы цепи](~/media/qpe.png). 

Дополнительные сведения см. в разделе [тактовые цепи](xref:microsoft.quantum.concepts.circuits).

## <a name="quantum-libraries"></a>Библиотеки тактов

Коллекции [операций](xref:microsoft.quantum.glossary#operation), [функций](xref:microsoft.quantum.glossary#function) и [определяемых пользователем типов](xref:microsoft.quantum.glossary#user-defined-type) для создания Q# программ. [Стандартная библиотека](xref:microsoft.quantum.libraries.standard.intro) устанавливается по умолчанию. Доступны другие библиотеки: [Библиотека химия](xref:microsoft.quantum.chemistry.concepts.intro), [Библиотека числовых чисел](xref:microsoft.quantum.numerics.intro) и [Библиотека машинного обучения](xref:microsoft.quantum.machine-learning.concepts.intro).

## <a name="quantum-state"></a>Состояние такта

Точное состояние изолированной тактовой системы, из которой можно извлечь вероятности [измерения](xref:microsoft.quantum.glossary#measurement) . В тактовых вычислениях имитатор тактовой частоты использует эти сведения для имитации реакции Кубитс на операции. Дополнительные сведения см. [в разделе кубит](xref:microsoft.quantum.concepts.qubit).

## <a name="qubit"></a>кубит

Базовая единица данных о такте, аналогичная *побиту* в классические вычисления. Дополнительные сведения см. [в разделе кубит](xref:microsoft.quantum.concepts.qubit).

## <a name="repeat-until-success"></a>Повторение до — успешное завершение

Алгоритм такта, probabilistically с ошибкой. При сбое подпрограммы повторит попытку до тех пор, пока не завершится успешно (или достигнут предел). Дополнительные сведения см. в разделе [повторение до успешного выполнения (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop) .

## <a name="standard-libraries"></a>Стандартные библиотеки

[Операции](xref:microsoft.quantum.glossary#operation), [функции](xref:microsoft.quantum.glossary#function) и [определяемые пользователем типы](xref:microsoft.quantum.glossary#user-defined-type) , которые устанавливаются вместе с Q# компилятором во время установки. Реализация стандартной библиотеки не зависит от целевых компьютеров. Дополнительные сведения см. в разделе [Стандартные библиотеки](xref:microsoft.quantum.libraries.standard.intro).

## <a name="superposition"></a>Суперпозиции

Концепция в тактовых вычислениях [кубит](xref:microsoft.quantum.glossary#qubit) представляет собой линейное сочетание двух состояний: $ \ket { 0 } $ и $ \ket { 1 } $ , пока оно не будет [измеряться](xref:microsoft.quantum.glossary#measurement).  Дополнительные сведения см. в разделе [Основные сведения о тактовых вычислениях](xref:microsoft.quantum.overview.understanding).

## <a name="target-machine"></a>Целевой компьютер

Цель компиляции, которая понижает абстрактную тактовую программу для оборудования или моделирования. Обычно это включает повторную запись для многих целей, включая замену шлюза, кодирование для коррекции ошибок, геометрическую структуру и другие. Дополнительные сведения см. в разделе [тактовые имитаторы и ведущие приложения](xref:microsoft.quantum.machines).

## <a name="teleportation"></a>Телепортация

Метод повторного создания данных или [состояния такта](xref:microsoft.quantum.glossary#quantum-state)одного [кубит](xref:microsoft.quantum.glossary#qubit) из одного места в другое без физического перемещения кубит с использованием [замкнутые](xref:microsoft.quantum.glossary#entanglement) и [измерения](xref:microsoft.quantum.glossary#measurement).  Дополнительные сведения см. в разделе [тактовые цепи](xref:microsoft.quantum.concepts.circuits) и соответствующие Ката в [такте Катас](xref:microsoft.quantum.overview.katas).

## <a name="tuple"></a>Кортеж

Коллекция значений с разделителями-запятыми, которая выступает в качестве одного значения. *Тип* кортежа определяется типами содержащихся в нем значений. В Q# кортежи являются [неизменяемыми](xref:microsoft.quantum.glossary#immutable) и могут быть вложенными, содержать массивы или использоваться в массиве. Дополнительные сведения см. в статье [Типы кортежей](xref:microsoft.quantum.guide.types#tuple-types).

## <a name="unitary-operator"></a>Оператор с единым

Оператор, инверсия которого равен его [соседнему](xref:microsoft.quantum.glossary#adjoint)объекту, т. е. $ УУ ^ { \dagger } = \id $ .

## <a name="user-defined-type"></a>Определяемый пользователем тип

Коллекция встроенных или ранее определенных типов, на которые можно ссылаться как на один блок. Дополнительные сведения см. в разделе [определяемые пользователем типы](xref:microsoft.quantum.guide.types#user-defined-types).