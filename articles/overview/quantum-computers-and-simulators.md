---
title: Квантовые компьютеры и квантовые симуляторы
description: Узнайте о квантовом оборудовании, симуляторах и принципах квантовых операций.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.simulators
ms.openlocfilehash: 04f90e9f88cf17259f96532617ef6f092b56b859
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430753"
---
# <a name="quantum-computers-and-quantum-simulators"></a>Квантовые компьютеры и квантовые симуляторы

Квантовые компьютеры все еще находятся на начальном этапе своего создания. Оборудование и его обслуживание требуют больших затрат, а большинство систем находятся в университетах и исследовательских лабораториях. Но технология совершенствуется, и к некоторым системам предоставляется ограниченный открытый доступ.

Квантовые симуляторы — это компьютерные программы, выполняющиеся на традиционных компьютерах. Они позволяют запускать и тестировать квантовые программы в среде, которая прогнозирует поведение кубитов в ответ на разные операции.

## <a name="quantum-hardware"></a>Квантовое оборудование

Квантовый компьютер состоит из трех основных частей: области, которая содержит кубиты, механизма передачи сигналов кубитам и обычного компьютера для запуска программы и отправки инструкций.

- Кубиты изготавливаются из хрупкого квантового материала, крайне чувствительного к воздействию окружающей среды. Некоторые способы организации хранилища кубитов предусматривают поддержание в нем температуры чуть выше абсолютного нуля для обеспечения максимальной когерентности кубитов. В других случаях хранилище представляет собой вакуумную камеру, что позволяет минимизировать вибрации и стабилизировать кубиты.  
- Для передачи кубитам сигналов применяются различные способы, в том числе с использованием микроволн, лазерного импульса и внешних потенциалов.

Чтобы обеспечить правильную работу квантовых компьютеров, нужно решить множество задач. Исправление ошибок на квантовых компьютерах является серьезной проблемой, а увеличение числа кубитов ведет к росту числа ошибок. Из-за этих ограничений домашний квантовый компьютер остается далекой перспективой. Более реалистичной представляется возможность доступа к коммерческим разработкам квантового компьютера на базе лаборатории.

## <a name="quantum-simulators"></a>Квантовые симуляторы

Квантовые симуляторы, работающие на обычных компьютерах, позволяют имитировать выполнение квантовых алгоритмов в квантовой системе.  Пакет средств разработки Quantum (QDK) содержит симулятор векторов всех состояний и другие специализированные квантовые симуляторы.

## <a name="topological-qubit"></a>Топологический кубит

Корпорация Майкрософт разрабатывает квантовый компьютер на основе топологических кубитов. Топологические кубиты менее всего подвержены влиянию среды, что сокращает потребность во внешних системах корректировки ошибок.

Топологические кубиты повышают стабильность системы и устойчивость к внешним шумам, а значит такая система лучше масштабируется и дольше остается надежной.

## <a name="microsoft-and-quantum-hardware-partnerships"></a>Партнерство с корпорацией Майкрософт в сфере создания оборудования для квантовых вычислений

Корпорация Майкрософт сотрудничает с такими производителями оборудования для квантовых вычислений, как IonQ, Honeywell и QCI, чтобы в будущем сделать квантовые компьютеры доступными для разработчиков. С помощью платформы Azure Quantum, пакета средств разработки Quantum (QDK) и языка Q# разработчики смогут создавать квантовые программы и выполнять их удаленно.

## <a name="quantum-computations"></a>Квантовые вычисления

Выполнение вычислений на квантовом компьютере или симуляторе включает следующие основные этапы:

- доступ к кубитам;
- инициализация кубитов в нужном состоянии;
- выполнение операций для изменения состояний кубитов;
- измерение новых состояний кубитов;

Инициализация и изменение состояний кубит выполняется с помощью **квантовых операций** (иногда именуемых квантовыми вентилями). Квантовые операции похожи на логические операции в обычных вычислениях, такие как AND, OR, NOT и XOR. Операция может быть как простой (например, смена состояния кубита с 1 на 0 или запутывание двух кубит), так и состоящей из серии операций для изменения вероятности коллапса кубитов, находящихся в суперпозиции, к тому или иному состоянию.

> [!NOTE] 
> [Библиотеки Q#](xref:microsoft.quantum.libraries) предоставляют встроенные операции, определяющие сложные сочетания низкоуровневых квантовых операций. Операции из библиотек можно использовать для преобразования кубитов и создания более сложных пользовательских операций.  

Измерение результата вычисления позволяет получить некий ответ, но для некоторых квантовых алгоритмов он не всегда будет правильным. Так как результат некоторых квантовых алгоритмов основан на вероятности, определенной квантовыми операциями, эти вычисления выполняются несколько раз для получения распределения вероятностей и повышения точности результатов.  Процесс определения того, что в результате операции получен правильный ответ, называется квантовой проверкой. Это серьезная задача в квантовых вычислениях.

## <a name="summary"></a>Сводка

Квантовые и традиционные вычисления имеют много общего, но у первых есть свои особенности. Вот некоторые из них:

- Квантовое оборудование является дорогостоящим и нестабильным, поэтому для написания и тестирования программ используются квантовые симуляторы.
- Как в традиционных, так и в квантовых вычислениях используются логические операции (или вентили).
- Квантовые вычисления возвращают вероятности.

Квантовое оборудование и технологии совершенствуются, что способствует динамичному развитию этой сферы. [Здесь](https://phys.org/search/?search=quantum+computer&s=0) вы можете узнать о некоторых текущих разработках.

## <a name="next-steps"></a>Дальнейшие действия

> [!div class="nextstepaction"]
> [Общие сведения о языке программирования Q# и пакете QDK](xref:microsoft.quantum.overview.q-sharp)