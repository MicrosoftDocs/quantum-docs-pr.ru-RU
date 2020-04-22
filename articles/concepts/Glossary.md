---
title: Квантовые вычисления глоссарий
description: Глоссарий общих терминов, действий и объектов, используемых в квантовых вычислениях.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: ee78515a0f47730b7d3df10da0853c5b8a7f6624
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "81482237"
---
# <a name="quantum-computing-glossary"></a>Квантовые вычисления глоссарий

## <a name="adjoint"></a>Адытковые

Комплекс сопряжения переноса [операции.](xref:microsoft.quantum.glossary#operation) Для операций, осуществляемых [унитарным](xref:microsoft.quantum.glossary#unitary-operator) оператором, присоединение является обратным для операции и указывается символом кинжала. Например, если `U` операция представляет унитарного `Adjoint U` оператора $U$, то представляет собой $U .dagger$. Для получения дополнительной информации, [см Adjoint](xref:microsoft.quantum.language.file-structure#adjoint).

## <a name="ancilla"></a>Ансилла

[Кубит,](xref:microsoft.quantum.glossary#qubit) который служит временной памятью для квантового компьютера и выделяется и высвобождается по мере необходимости.  Для получения дополнительной [информации см.](xref:microsoft.quantum.concepts.multiple-qubits)

## <a name="bell-state"></a>Состояние колокола

Один из четырех конкретных максимально [запутанных](xref:microsoft.quantum.glossary#entanglement) [квантовых состояний](xref:microsoft.quantum.glossary#quantum-state) двух кубитов. Четыре состояния определяются как «beta_ »зий» («математика» («время Хийз»{00} («Кет» и{11}«кет») /{2}«sqrt ».» Состояние Bell также известно как [пара EPR.](xref:microsoft.quantum.glossary#epr-pair)

## <a name="bloch-sphere"></a>Сфера Блох

Графическое представление[однокубитового](xref:microsoft.quantum.glossary#qubit) [квантового состояния](xref:microsoft.quantum.glossary#quantum-state) как точки в трехмерной единой сфере. Для получения дополнительной информации [см. Визуализация Кубитс и Преобразований с помощью сферы Блох](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).

## <a name="callable"></a>Вызываемые

[Операция](xref:microsoft.quantum.glossary#operation) или [функция](xref:microsoft.quantum.glossary#function) на языке q. Для получения дополнительной информации [см.](xref:microsoft.quantum.language.type-model#operation-and-function-types)

## <a name="clifford-group"></a>Группа Клиффорд

Набор операций, которые занимают октаны [сферы Блох](xref:microsoft.quantum.glossary#bloch-sphere) и эффект перестановки [операторов Паули](xref:microsoft.quantum.glossary#pauli-operators). К ним относятся операции [$X $](xref:microsoft.quantum.intrinsic.x), [$Y $](xref:microsoft.quantum.intrinsic.y), [$Z $](xref:microsoft.quantum.intrinsic.z), [$H$](xref:microsoft.quantum.intrinsic.h) и [$S $](xref:microsoft.quantum.intrinsic.s).

## <a name="controlled"></a>Контролируемых

Квантовая [операция,](xref:microsoft.quantum.glossary#operation) которая занимает один или несколько [кубитов](xref:microsoft.quantum.glossary#qubit) в качестве вспомогательного фактора для целевой операции. Для получения дополнительной информации [см.](xref:microsoft.quantum.language.type-model#controlled)

## <a name="dirac-notation"></a>Нотация Дирака

Символическое сокращение, которое упрощает представление [квантовых состояний,](xref:microsoft.quantum.glossary#quantum-state)также называемое *обозначением бюстгальтер-кет.*  Часть *бюстгальтера* представляет собой вектор строки, например, «бра»А» » » » » » » » » » » » » » » & A »2 » (конец» bmatrix) $ и *кет-часть* представляет собой вектор столбца, $ »кет»B» » » » » » B1» \\ \\ B » Для получения дополнительной информации [см.](xref:microsoft.quantum.concepts.dirac)

## <a name="eigenvalue"></a>Эйгенвале

Фактор, с помощью которого величина [эйгенвевеста](xref:microsoft.quantum.glossary#eigenvector) данной трансформации изменяется при применении преобразования.  Учитывая квадратную матрицу $M$ и eigenvector $v$, затем $Mv cv$, где $c $ является eigenvalue и может быть сложным числом любого аргумента. Для получения дополнительной [информации см.](xref:microsoft.quantum.concepts.matrix-advanced)

## <a name="eigenvector"></a>Эйгенвектор

Вектор, направление которого не меняется в результате данной трансформации и величина которого изменяется коэффициентом, соответствующим [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue)этого вектора. Учитывая квадратную матрицу $M$, а также eigenvalue $c$, то $Mv cv$, где $v$ является eigenvector матрицы и может быть сложным числом любого аргумента. Для получения дополнительной [информации см.](xref:microsoft.quantum.concepts.matrix-advanced)

## <a name="entanglement"></a>Запутанности

Квантовые частицы, такие как [кубиты,](xref:microsoft.quantum.glossary#qubit)могут быть соединены или *запутаны* таким образом, что они не могут быть описаны независимо друг от друга. Их результаты измерения коррелируют даже тогда, когда они разделены бесконечно далеко. Запутывание имеет важное значение для [измерения](xref:microsoft.quantum.glossary#measurement) [состояния](xref:microsoft.quantum.glossary#quantum-state) кубита.  Для получения дополнительной [информации см.](xref:microsoft.quantum.concepts.matrix-advanced)

## <a name="epr-pair"></a>Пара EPR

Один из четырех конкретных максимально запутанных [квантовых состояний](xref:microsoft.quantum.glossary#quantum-state) двух [кубитов.](xref:microsoft.quantum.glossary#qubit) Четыре состояния определяются как «beta_ »ij» («математика»{1} («олеты Хизёй»{00} (кет){11}/ «кверт» (кврт.) / «кврт» (кврт.).{2} Пара EPR также известна как [состояние Bell](xref:microsoft.quantum.glossary#bell-state)

## <a name="evolution"></a>Эволюции

Как [квантовое состояние](xref:microsoft.quantum.glossary#quantum-state) изменяется с течением времени. Для получения дополнительной информации, см [Матрица экспоненциально .](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials)

## <a name="function"></a>Функция
Тип подпрограммы на языке, который является чисто классическим (неквантовым). Хотя функции используются в квантовых алгоритмах, они не могут действовать на [кубитоты](xref:microsoft.quantum.glossary#qubit) или [операции](xref:microsoft.quantum.glossary#operation)вызова. Для получения дополнительной информации [см.](xref:microsoft.quantum.language.type-model#operation-and-function-types)

## <a name="gate"></a>Ворота

Наследие термин для квантовой [операции](xref:microsoft.quantum.glossary#operation), основанный на концепции классической логики ворот. [Квантовая цепь](xref:microsoft.quantum.glossary#quantum-circuit-diagram) представляет собой сеть ворот (или операций), основанную на аналогичной концепции классических логических схем.

## <a name="global-phase"></a>Глобальная фаза

Когда два [состояния](xref:microsoft.quantum.glossary#quantum-state) идентичны кратному сложному числу $e «зи»-фи»,, они, как говорят, отличаются до глобальной фазы. В отличие от локальных фаз, глобальные фазы не могут наблюдаться через любое [измерение.](xref:microsoft.quantum.glossary#measurement) Для получения дополнительной информации, [см.](xref:microsoft.quantum.concepts.qubit)

## <a name="hadamard"></a>Hadamard

Операция Хадамард (также именуемый воротами Хадамард или преобразование) действует на одном [кубите](xref:microsoft.quantum.glossary#qubit) и{1}помещает его в ровную [суперпозицию](xref:microsoft.quantum.glossary#superposition) в размере ${0}или $ кет $ , если кубит изначально находится в состоянии{0}$ $ . В q, эта операция применяется заранее определенной [`H`](xref:microsoft.quantum.intrinsic.h) операцией.

## <a name="immutable"></a>Постоянное

Переменная, значение которой не может быть изменено. Неизменяемая переменная в q `let` создается с помощью ключевого слова. Чтобы объявить переменные, которые *могут* быть изменены, `set` используйте [изменяемое](xref:microsoft.quantum.glossary#immutable) ключевое слово для декларировать и ключевое слово для изменения значения. 

## <a name="measurement"></a>Измерения

Манипуляция [кубитом](xref:microsoft.quantum.glossary#qubit) (или набором кубитов), который дает результат наблюдения, фактически получая классический бит. Для получения дополнительной информации, [см.](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit)

## <a name="mutable"></a>Изменяемый

Переменная, значение которой может быть изменено после его создания. Изменяемая переменная в q `mutable` объявляется с помощью ключевого слова и модифицируется с помощью ключевого `set` слова. Переменные, созданные с помощью ключевого `let` слова, [неизменяемы,](xref:microsoft.quantum.glossary#immutable) и их значение не может быть изменено.

## <a name="namespace"></a>Пространство имен

Метка для коллекции связанных имен (т.е. [операций,](xref:microsoft.quantum.glossary#operation) [функций](xref:microsoft.quantum.glossary#function)и [типов, определяемых пользователем).](xref:microsoft.quantum.glossary#user-defined-type) Например, пространство имен [Microsoft.Quantum.Preparation](xref:microsoft.quantum.preparation) маркирует все символы, определенные в стандартной библиотеке, которые помогают при подготовке исходных состояний.

## <a name="operation"></a>Операция

Основная единица квантового исполнения в кю. Это примерно эквивалентно функции в C, C или Python, или статического метода в C или Java. Для получения дополнительной информации [см.](xref:microsoft.quantum.language.type-model#operation-and-function-types)

## <a name="operator-application"></a>Приложение оператора

Выполнение квантовой операции. Это обычно применяет унитарную матрицу к текущему вектору состояния квантового состояния.

## <a name="oracle"></a>Oracle;

Подпрограммы, которая предоставляет зависимую от данных информацию квантовому алгоритму во время выполнения. Как правило, цель состоит в том, чтобы обеспечить [суперпозицию](xref:microsoft.quantum.glossary#superposition) выходов, соответствующих входным данным, которые находятся в суперпозиции. Для получения дополнительной [информации см.](xref:microsoft.quantum.libraries.data-structures#oracles)

## <a name="partial-application"></a>Частичное применение

Вызов [функции](xref:microsoft.quantum.glossary#function) или [операции](xref:microsoft.quantum.glossary#operation) без всех необходимых входов. Это возвращает новый [callable,](xref:microsoft.quantum.glossary#callable) что только необходимо недостающие параметры (указано подчеркнуть), которые будут поставлены во время будущего приложения. Например, с `MyFunc(x : int, y : int) : int {return x + y;}` учетом функции можно частично применить `let NewFunc = MyFunc(_, 3)`ее к новой функции. Затем можно позвонить в новую функцию `NewFunc(2)` позже с отсутствующим параметром, который возвращает значение *5.*  Для получения дополнительной информации [см.](xref:microsoft.quantum.language.expressions#partial-application)

## <a name="pauli-operators"></a>Операторы Паули

Набор из трех 2 х 2 унитарных `Y` `Z` матриц, известных как `X`, и квантовых операций. Матрица идентификации, $I$, часто входит в набор также.  $I »начать »bmatrix» 1 \\ \\ & 0 0 & 1 «конец»bmatrix»$, $X \\ \\ »начать »bmatrix» 0 & 1 1 & 0 »конец \\ \\ »bmatrix» $, $Y »начало »bmatrix» 0 &-i i & 0 »конец »bmatrix» $, $Z »начать »bmatrix» 1 & 0 \\ \\ 0 & .1 »конец»bmatrix»   Для получения дополнительной информации [см.](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)

## <a name="quantum-circuit-diagram"></a>Схема квантовой цепи

Метод для графического представления последовательности [операций](xref:microsoft.quantum.glossary#operation) (или [ворот)](xref:microsoft.quantum.glossary#gate) ![для простых](~/media/qpe.png)квантовых программ, например диаграммы схемы образца. Для получения дополнительной информации, см [Квантовая схемы](xref:microsoft.quantum.concepts.circuits).

## <a name="quantum-libraries"></a>Квантовые библиотеки

Коллекции [операций,](xref:microsoft.quantum.glossary#operation) [функций](xref:microsoft.quantum.glossary#function) и [типов, определяемых пользователями,](xref:microsoft.quantum.glossary#user-defined-type) для создания программ. [Стандартная библиотека](xref:microsoft.quantum.libraries.standard.intro) устанавливается по умолчанию. Другие библиотеки доступны [библиотека химии,](xref:microsoft.quantum.chemistry.concepts.intro) [библиотека Numerics](xref:microsoft.quantum.numerics.intro) и [библиотека машинного обучения](xref:microsoft.quantum.machine-learning.concepts.intro).

## <a name="quantum-state"></a>Квантовое состояние

Точное состояние изолированной квантовой системы, из которой можно извлечь [вероятности](xref:microsoft.quantum.glossary#measurement) измерений. В квантовых вычислениях квантовый симулятор использует эту информацию для имитации реагирования кубитов на операции. Для получения дополнительной информации, [см.](xref:microsoft.quantum.concepts.qubit)

## <a name="qubit"></a>Зубит

Основная единица квантовой информации, аналогичная *немного* в классических вычислениях. Для получения дополнительной информации, [см.](xref:microsoft.quantum.concepts.qubit)

## <a name="repeat-until-success"></a>Повторите-до-успех

Квантовый алгоритм, который, вероятно, преуспевает. После сбоя, рутина будет повторить попытку до тех пор, пока успешно (или предел был достигнут). Для получения дополнительной информации [см.](xref:microsoft.quantum.techniques.qubits#measurements)

## <a name="standard-libraries"></a>Стандартные библиотеки

[Операции,](xref:microsoft.quantum.glossary#operation) [функции](xref:microsoft.quantum.glossary#function) и типы, определяемые [пользователем,](xref:microsoft.quantum.glossary#user-defined-type) которые устанавливаются вместе с компилятором во время установки. Стандартная реализация библиотеки агностична по отношению к целевым машинам. Для получения дополнительной информации [см.](xref:microsoft.quantum.libraries.standard.intro)

## <a name="superposition"></a>Суперпозиции

Концепция в квантовых вычислениях, что [кубит](xref:microsoft.quantum.glossary#qubit) представляет собой линейное сочетание двух состояний, $ кет-0 »$и $ 1 $, до тех пор, пока он [измеряется](xref:microsoft.quantum.glossary#measurement).  Для получения дополнительной информации, см [Что такое квантовые вычисления](xref:microsoft.quantum.overview.what).

## <a name="target-machine"></a>Целевая машина

Цель компиляции, которая понижает абстрактную квантовую программу к аппаратному или симуляции. Это обычно включает перезаписи для многих целей, включая замену ворот, кодирование для коррекции ошибок, геометрический макет и другие. Для получения дополнительной информации смотрите [квантовые симуляторы и принимающие приложения.](xref:microsoft.quantum.machines)

## <a name="teleportation"></a>Телепортация

Метод регенерации данных, или [квантовое состояние,](xref:microsoft.quantum.glossary#quantum-state)одного [кубита](xref:microsoft.quantum.glossary#qubit) из одного места в другое без физического перемещения кубита, используя [запутанность](xref:microsoft.quantum.glossary#entanglement) и [измерение.](xref:microsoft.quantum.glossary#measurement)  Для получения дополнительной информации, см [Квантовая схемы](xref:microsoft.quantum.concepts.circuits) и [положить все это вместе](xref:microsoft.quantum.techniques.puttingittogether).

## <a name="tuple"></a>Кортеж

Коллекция значений, разделенных запятой, которая действует как единое значение. *Тип* тупл определяется типами значений, которые он содержит. В кью, tuples являются [неизменяемыми](xref:microsoft.quantum.glossary#immutable) и могут быть вложены, содержат массивы, или использоваться в массиве. Для получения дополнительной [Tuple types](xref:microsoft.quantum.language.type-model#tuple-types)информации см.

## <a name="unitary-operator"></a>Унитарный оператор

Оператор, обратная сторона которого равна его [аддукции,](xref:microsoft.quantum.glossary#adjoint)т.е. $UU «кинжал» и «ид»..

## <a name="user-defined-type"></a>Определяемый пользователем тип

Коллекция встроенных или ранее определенных типов, которые могут быть отнесены к единой единице. Для получения дополнительной [User-defined types](xref:microsoft.quantum.language.type-model#user-defined-types)информации см.