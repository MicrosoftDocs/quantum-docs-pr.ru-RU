---
title: Имитация Хамилтониан Dynamics
description: Узнайте, как использовать формулы Троттер-Сузуки и кубитизатион для работы с имитацией Хамилтониан.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.simulationalgorithms
ms.openlocfilehash: 5dad4e4a77eea99e72eb2efac52eec61ebbdb21c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275930"
---
# <a name="simulating-hamiltonian-dynamics"></a>Имитация Хамилтониан Dynamics

После того как Хамилтониан выражается в виде суммы элементарных операторов, Dynamics может быть скомпилирована в фундаментальные операции с использованием узла хорошо известных методов.
Вот три эффективных подхода: Троттер – Сузуки формулы, линейные сочетания унитариес и кубитизатион.
Мы объясним эти три подхода ниже и предведем конкретные примеры в Q #, как реализовать эти методы с помощью библиотеки моделирования Хамилтониан.


## <a name="trottersuzuki-formulas"></a>Троттер — формулы Сузуки
Идея Троттер – Сузуки формул проста: Express Хамилтониан в качестве суммы простых для имитации Хамилтонианс, а затем приблизительного суммарного развития в виде последовательности этих упрощенных эволюций.
В частности, Let $H = \ sum_ {j = 1} ^ m H_j $ быть Хамилтониан.
Затем $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \ prod_ {j = 1} ^ m e ^ {-iH_j t} + O (m ^ 2 t ^ 2), $ $ скажем, если $t \лл $1, то ошибка в этой аппроксимации становится незначительной.
Обратите внимание, что если $e ^ {-i H} $ является обычной экспонентой, то ошибка в этой аппроксимации не будет $O (m ^ 2 t ^ 2) $: это будет ноль.
Эта ошибка возникает из-за того, что $e ^ {-ИХТ} $ является экспонентой и, как следствие, при использовании этой формулы возникает ошибка, вызванная тем фактом, что $H _j $ термы не ведут себя (т *. е.*$H _j H_k \не H_k H_j $ в целом).

Если $t $ имеет большой размер, формулы Троттер – Сузуки можно использовать для точной имитации Dynamics, разбивая ее на последовательность коротких временных шагов.
Позвольте $r $ быть числом шагов, предпринятых в ходе эволюции, так что каждый раз, когда шаг выполняется в течение времени $t/r $. Затем у нас есть $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \лефт (\ prod_ {j = 1} ^ m e ^ {-iH_j t/r} \ right) ^ r + O (m ^ 2 t ^ 2/r), $ $ означает, что если $r $ масштабируется как $m ^ 2 t ^ 2/\ Эпсилон $, то ошибку можно сделать не более чем на $ \епсилон $ для любого $ \епсилон>$0.

Более точные выражения приближения могут быть построены путем создания последовательности экспоненциальных элементов операторов таким, что условия ошибки отменяются.
Самая простая формула, вторая формула Троттер-Сузуки, принимает форму $ $ U_2 (t) = \лефт (\ prod_ {j = 1} ^ {m} e ^ {-iH_j t/2R} \ prod_ {j = m} ^ 1 e ^ {-iH_j t/2R} \ right) ^ r = e ^ {-ИХТ} + O (m ^ 3 t ^ 3/r ^ 2), $ $ ошибка, которую можно сделать меньше $ \епсилон $ для любого $ \епсилон>$0, выбрав $r $ для масштабирования $m ^ {3/2} t ^ {3/2}/\скрт {\ Эпсилон} $.

Даже более высокие формулы, в частности ($ 2000 $) TH-Order для $k>$0, можно формировать рекурсивно: $ $ U_ {2000} (t) = [U_ {2000-2} (s_k \~ t)] ^ 2 U_ {2000-2} ([1-4s_k] t) [U_ {2000 – 2} (s_k \~ t)] ^ 2 = e ^ {-ИХТ} + O ((m t) ^ {2000 + 1}/r ^ {2000}), $ $ where $s _k = (4-4 ^ {1/(2000-1)}) ^ {-1} $.

Самым простым является следующая четвертая формула ($k = $2), впервые представленная Сузуки: $ $ U_4 (t) = [U_2 (s_2 \~ t)] ^ 2 U_2 ([1-4s_2] t) [U_2 (S_2 \~ t)] ^ 2 = e ^ {-ИХТ} + O (m ^ 5T ^ 5/r ^ 4), $ $ Where $s _2 = (4-4 ^ {1/3}) ^ {-1} $.
Как правило, произвольные формулы высокого порядка могут быть сформированы аналогичным образом. Однако затраты, связанные с использованием более сложных интеграторов, часто перевешивают преимущества за пределы четвертого порядка для большинства практических проблем.

Чтобы обеспечить работу описанных выше стратегий, необходим метод для имитации широкого класса $e ^ {-iH_j t} $.
Простейшим семейством Хамилтонианс и, вероятно, наиболее полезным, что мы можем использовать здесь, — это операторы Паули.
Операторы Паули можно легко имитировать, так как они могут быть диагонали с помощью операций Клиффорд (которые являются стандартными шлюзами в тактовых вычислениях).
Кроме того, после диагонали их еиженвалуес можно найти, вычисляя четность Кубитс, на которой они работают.

Например, $ $ e ^ {-Икс\отимес X t} = (Х\отимес H) e ^ {-Из\отимес Z t} (Х\отимес H), $ $ где $ $ e ^ {-i Z \отимес Z t} = \бегин{бматрикс} e ^ {-IT} & 0 & 0 & 0\\\
        0 & e ^ {i t} & 0 & 0\\\
        0 & 0 & e ^ {IT} & 0\\\
        0 & 0 & 0 & e ^ {-IT} \енд{бматрикс}.
$ $ Здесь $e ^ {-ИХТ} \кет {00} = e ^ {IT} \кет {00} $ и $e ^ {-ИХТ} \кет {01} = e ^ {-IT} \кет {01} $, которая может быть показана непосредственно в результате того, что четность $0 $ равна $0 $, а четность битовой строки $1 $ — $1 $.

Экспоненциальные операторы Паули можно реализовать непосредственно в Q # с помощью <xref:microsoft.quantum.intrinsic.exp> операции:
```qsharp
    using(qubits = Qubit[2]){
        let pauliString = [PauliX, PauliX];
        let evolutionTime = 1.0;

        // This applies 𝑒^{- 𝑖 𝑋⊗𝑋 𝑡} to qubits 0 and 1.
        Exp(pauliString, - evolutionTime, qubits);
    }
```

Для Фермионик Хамилтонианс [декомпозиция "Иордания — Вигнер](xref:microsoft.quantum.chemistry.concepts.jordanwigner) " удобно сопоставляет хамилтониан с суммой операторов Паули.
Это означает, что описанный выше подход можно легко адаптировать для имитации химия.
Вместо того, чтобы выполнять циклическое переключение всех Паулиных терминов в представлении "Иордания-Вигнер", ниже приведен простой пример того, как будет выглядеть такая имитация в химия.
Наша начальная точка – это [Вигнер кодировка](xref:microsoft.quantum.chemistry.concepts.jordanwigner) фермионик хамилтониан, выраженная в коде как экземпляр `JordanWignerEncoding` класса.

```csharp
    // This example uses the following namespaces:
    // using Microsoft.Quantum.Chemistry.OrbitalIntegrals;
    // using Microsoft.Quantum.Chemistry.Fermion;
    // using Microsoft.Quantum.Chemistry.Pauli;
    // using Microsoft.Quantum.Chemistry.QSharpFormat;

    // We create an instance of the `FermionHamiltonian` objecclasst to store the terms.
    var hamiltonian = new OrbitalIntegralHamiltonian(new[] 
    {
        new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123),
        new OrbitalIntegral(new[] { 0, 1 }, 0.456)
    }).ToFermionHamiltonian(IndexConvention.UpDown);

    // We convert this fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = hamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);

    // We now convert this representation into a format consumable by Q#.
    var qSharpData = jordanWignerEncoding.ToQSharpFormat();
```

Этот формат представления "Иордания — Вигнер", который используется алгоритмами моделирования Q #, является определяемым пользователем типом `JordanWignerEncodingData` .
В Q # этот формат передается в удобную функцию `TrotterStepOracle` , которая возвращает оператор, приближенный к времени на развитие с помощью Троттер — Сузуки Integrator, в дополнение к другим параметрам, необходимым для его выполнения.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single time-step.
using(qubits = Qubit[nQubits]){

    // Apply single step of time-evolution
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

Важно, что эта реализация применяет некоторые оптимизации, обсуждаемые при [моделировании электронных структур Хамилтонианс с помощью тактовых компьютеров](https://arxiv.org/abs/1001.3855) , и [улучшая тактовые алгоритмы для химия тактов](https://arxiv.org/abs/1403.1539) , чтобы свести к минимальному числу требуемых поворотов с одним кубитом, а также сократить количество ошибок моделирования.

## <a name="qubitization"></a>кубитизатион

Кубитизатион — это альтернативный подход к моделированию, в котором для имитации тактовой корректировки используются идеи из примеров тактов.
Хотя для кубитизатион требуется больше Кубитс, чем Троттер формул, метод обещает оптимальное масштабирование с учетом времени развития и допустимости ошибок.
По этим причинам он стал предпочтительным методом для имитации Хамилтониан Dynamics в целом, а также для решения проблемы с электронной структурой в частности.

На высоком уровне кубитизатион выполняет эту задачу, выполнив следующие действия.
Сначала позвольте $H = \ sum_j h_j H_j $ для единых и Хермитиан $H _j $ и $h _j \же $0.
Выполняя пару отражений, кубитизатион реализует оператор, эквивалентный $ $W = e ^ {\пм i \кос ^ {-1} (H/| h | _1)}, $ $ где $ | H | _1 = \ sum_j | h_j | $.
Следующий шаг включает преобразование еиженвалуес оператора обхода из $e ^ {и\пм \кос ^ {-1} (E_k/| h | _1)} $, где $E _k $ являются еиженвалуес $H $ для $e ^ {-iE_k t} $.
Это можно сделать с помощью различных методов преобразования значений в единственном значении такта, включая [обработку тактовых сигналов](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).

Кроме того, если требуется только статическое количество (например, энергия состояния заземления Хамилтониан), то вполне достаточно применить [оценку этапа](xref:microsoft.quantum.libraries.characterization) непосредственно к $W $, чтобы оценить энергопотребление от результата, выполнив косинус результата.
Это важно, так как позволяет сделать преобразование Спектрал классическим, а не использовать метод преобразования значения в единственном значении в такте.

На более подробном уровне для реализации кубитизатион требуется две подпрограммы, предоставляющие интерфейсы для Хамилтониан.
В отличие от методов Троттер – Сузуки эти подпрограммы являются тактовыми, а их реализация требует использования пропорциональны логарифму больше Кубитс, чем потребуется для моделирования на основе Троттер.

Первая подпрограммы такта, используемая кубитизатион, называется $ \Операторнаме{Селект} $, и предполагается возвращать \бегин{екуатион} \Операторнаме{Селект} \кет{ж} \ket{\psi} = \ket{j} H_j \ket{\psi}, \end{Equation}, где каждый $H _j $ считается Hermitian и единой.
Хотя это может показаться неограниченным, помните, что операторы Паули являются Хермитиан и едиными, поэтому приложения, такие как имитация химия, естественным образом попадают в эту инфраструктуру.
Операция $ \Операторнаме{Селект} $, возможно, удивительно, является на самом деле операцией отражения.
Это видно из того факта, что $ \Операторнаме{Селект} ^ 2 \ Сисакет {j} \кет{\пси} = \кет{ж} \кет{\пси} $, так как каждый $H _j $ является единым и Хермитиан и, таким же, имеет еиженвалуес $ \пм $1.

Вторая подпрограммы называется $ \Операторнаме{ПРЕПАРЕ} $.
Хотя операция SELECT предоставляет средства для согласованного доступа к каждому из Хамилтониан условий $H _j $ подподпрограмма Prepare предоставляет метод для доступа к коэффициентам $h _j $, \бегин{екуатион} \Операторнаме{ПРЕПАРЕ}\кет {0} = \ sum_j \скрт{\фрак{h_j} {| H | _1}} \кет{ж}.
\енд{екуатион} затем, используя шлюз фаз с умножением, мы видим, что $ $ \Ламбда\кет {0} ^ {\отимес n} = \бегин{Касес} \- \кет{КС} & \текст{ИФ} x = 0\\\
        \кет{КС} & \текст{осервисе} \енд{Касес}.
$$

Операция $ \операторнаме{ПРЕПАРЕ} $ не используется непосредственно в кубитизатион, а используется для реализации отражения состояния, которое $ \операторнаме{ПРЕПАРЕ} $ создает $ $ \бегин{алигн} R &amp; = 1-2 \ операторнаме {Prepare} \ket {0} \bra {0} \operatorname{Prepare} ^ {-1} \\ \\ &amp; = \operatorname{Prepare} \Lambda \operatorname{Prepare} ^ {-1} .
\енд{алигн} $ $

Оператор обхода, $W $, может быть выражен в терминах $ \Операторнаме{Селект} $ и $R $ в виде $ $ W = \Операторнаме{Селект} R, $ $, который опять может быть представлен для реализации оператора, эквивалентного (до исометри), для $e ^ {\пм i \кос ^ {-1} (h/| H | _1)} $.

Эти подпрограммы легко настроить в Q #.
В качестве примера рассмотрим простой кубит с поворотом Исинг Хамилтониан, где $H = X_1 + X_2 + Z_1 Z_2 $.
В этом случае в параметре Q # Code, который будет реализовывать операцию $ \Операторнаме{Селект} $, вызывается <xref:microsoft.quantum.canon.multiplexoperations> , тогда как операция $ \операторнаме{ПРЕПАРЕ} $ может быть реализована с помощью <xref:microsoft.quantum.preparation.preparearbitrarystate> .
Пример, включающий моделирование модели Хуббард, можно найти в виде [образца Q #](https://github.com/microsoft/Quantum/tree/master/samples/simulation/hubbard).

Чтобы вручную указать эти шаги для произвольных проблем химия, потребуется много усилий, что позволит избежать использования библиотеки химия.
Аналогично алгоритму имитации Троттер – Сузуки, приведенному выше, `JordanWignerEncodingData` метод передается в удобную функцию `QubitizationOracle` , которая возвращает оператор обхода, а также другие параметры, необходимые для его выполнения.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/oneNorm`, where oneNorm is the sum of absolute values of all probabilities in state prepared by `Prepare`.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  QubitizationOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single step of the quantum walk.
using(qubits = Qubit[nQubits]){

    // Apply single step of quantum walk.
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

Важно, что реализация <xref:microsoft.quantum.chemistry.jordanwigner.qubitizationoracle> применима к произвольным хамилтонианс, указанным в виде линейного сочетания строк Паули.
Версия, оптимизированная для имитации химия, вызывается с помощью <xref:microsoft.quantum.chemistry.jordanwigner.optimizedqubitizationoracle> .
Эта версия оптимизирована для минимального числа T-шлюзов с помощью методик, описанных в разделе [кодирование электронных спектра в тактовых каналах с помощью линейной T-сложности](https://arxiv.org/abs/1805.03662).