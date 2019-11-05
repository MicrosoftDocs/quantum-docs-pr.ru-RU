---
title: Введение в Quantum Katas
description: Сведения о тренировочных упражнениях (ката), которые входят в пакет Microsoft Quantum Development Kit
author: natke
ms.author: nakersha
ms.date: 10/17/2019
ms.topic: overview
uid: microsoft.quantum.overview.katas
ms.openlocfilehash: 7fb8dba2a10f9a983ebee52e394260bbdc0d2f9c
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "73444146"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a>Изучение квантовых вычислений с помощью Quantum Katas

[Quantum Katas](https://github.com/Microsoft/QuantumKatas/) — это коллекция учебных курсов с открытым кодом и уроков программирования, предназначенная для изучения квантовых вычислений и программирования на Q# в произвольном темпе.

## <a name="learning-by-doing"></a>Обучение путем выполнения

Руководства и ката, собранные в этом проекте, реализуют идею обучения путем выполнения. Вам предлагаются задачи по программированию на определенные темы с разным уровнем сложности. В каждой задаче вам нужно добавить определенный код. Для первой задачи в серии нужна всего одна строка, а для последней — более крупный фрагмент.

Что важнее всего, в ката включены платформы для тестирования, которые подготавливают и запускают ваши решения, а также проверяют результаты. Это позволяет немедленно оценить ваше решение, чтобы вы могли поменять неправильный подход.

Вы можете работать и учиться с ката в любой удобной среде:

* Jupyter Notebook в Интернете со средой Binder;
* Jupyter Notebook на локальном компьютере;
* Visual Studio
* Visual Studio Code

## <a name="what-can-i-learn-with-the-quantum-katas"></a>Что я могу изучить с помощью Quantum Katas?

Ниже приведен краткий список основных тем, которые рассматриваются в Quantum Katas. Мы рекомендуем соблюдать эту последовательность в начале обучения, чтобы хорошо разобраться в фундаментальных концепциях квантовых вычислений. Разумеется, вы всегда можете пропустить уже знакомые вам темы, например сложные арифметические действия, и изучать алгоритмы в произвольном порядке.

### <a name="introduction-to-quantum-computing-concepts"></a>Сведения о концепциях квантовых вычислений

* [Сложные арифметические действия](https://github.com/microsoft/QuantumKatas/blob/master/tutorials/ComplexArithmetic)
* [Линейная алгебра](https://github.com/microsoft/QuantumKatas/blob/master/tutorials/LinearAlgebra)
* [Концепция кубита](https://github.com/microsoft/QuantumKatas/blob/master/tutorials/Qubit)
* [Квантовые вентили с одним кубитом](https://github.com/microsoft/QuantumKatas/blob/master/tutorials/SingleQubitGates)

### <a name="quantum-computing-fundamentals"></a>Основы квантовых вычислений

* [Определение квантовых вентилей](https://github.com/microsoft/QuantumKatas/tree/master/BasicGates)
* [Создание квантовой суперпозиции](https://github.com/microsoft/QuantumKatas/tree/master/Superposition)
* [Дифференциация квантовых состояний путем измерений](https://github.com/microsoft/QuantumKatas/tree/master/Measurements)
* [Связанные измерения](https://github.com/microsoft/QuantumKatas/tree/master/JointMeasurements)

### <a name="algorithms"></a>Алгоритмы

* [Квантовая телепортация](https://github.com/microsoft/QuantumKatas/tree/master/Teleportation)
* [Сверхплотное кодирование](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)
* [Алгоритм Дойча — Йожи](https://github.com/microsoft/QuantumKatas/blob/master/tutorials/DeutschJozsaAlgorithm)
* [Реализация алгоритма поиска Гровера](https://github.com/microsoft/QuantumKatas/tree/master/GroversAlgorithm)
* [Изучение высокоуровневых свойств алгоритма поиска Гровера](https://github.com/microsoft/QuantumKatas/blob/master/tutorials/ExploringGroversAlgorithm)
* Решение реальных задач с помощью алгоритма Гровера: [Задача выполнимости булевых формул](https://github.com/microsoft/QuantumKatas/blob/master/SolveSATWithGrover) и [задача цветовой раскраски графа](https://github.com/microsoft/QuantumKatas/blob/master/GraphColoring)

### <a name="protocols-and-libraries"></a>Протоколы и библиотеки

* [Протокол BB84 для распространения квантовых ключей](https://github.com/microsoft/QuantumKatas/tree/master/KeyDistribution_BB84)
* Квантовая коррекция ошибок: [код коррекции ошибок при инверсии битов](https://github.com/microsoft/QuantumKatas/tree/master/QEC_BitFlipCode)
* [Оценка квантовых фаз](https://github.com/microsoft/QuantumKatas/blob/master/PhaseEstimation)
* Квантовая арифметика: [создание сумматоров со сквозным переносом](https://github.com/microsoft/QuantumKatas/blob/master/RippleCarryAdder)

### <a name="entanglement-games"></a>Игры с запутанностью

* [Игра CHSH](https://github.com/microsoft/QuantumKatas/blob/master/CHSHGame)
* [Игра GHZ](https://github.com/microsoft/QuantumKatas/blob/master/GHZGame)
* [Игра "Волшебный квадрат" Мермина — Переса](https://github.com/microsoft/QuantumKatas/tree/master/MagicSquareGame)

## <a name="resources"></a>Ресурсы

* Полный набор [Quantum Katas](https://github.com/microsoft/QuantumKatas)
* [Выполнение ката в Интернете](https://aka.ms/try-quantum-katas)
