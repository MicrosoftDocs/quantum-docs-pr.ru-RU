---
title: Руководство пользователя Q#
description: Общие сведения о назначении и содержимом этого руководства пользователя
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: f535aaedbe6ce181375d48f7023409ad8212c702
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430617"
---
# <a name="the-q-user-guide"></a>Руководство пользователя Q#

Перед вами руководство пользователя по Q#. 

Здесь мы подробно рассмотрим основные понятия языка Q # и все, что вам потребуется для написания квантовых программ.

## <a name="user-guide-contents"></a>Содержимое руководства пользователя

- [Основы Q#](xref:microsoft.quantum.guide.basics). Вводные сведения о назначении и функциональных возможностях языка программирования Q#. 

### <a name="q-language"></a>Язык Q#

- [Типы в Q#](xref:microsoft.quantum.guide.types). Описание модели типов в Q# и синтаксиса для определения типов и работы с ними.

- [Выражения типов](xref:microsoft.quantum.guide.expressions). Сведения о том, как определять, использовать и объединять каждый из типов в Q#, а также работать с их значениями. 

### <a name="using-q"></a>Использование Q#

- [Структура файла Q#.](xref:microsoft.quantum.guide.filestructure) Описание структуры и синтаксиса файла `*.qs` Q#.

- [Операции и функции.](xref:microsoft.quantum.guide.operationsfunctions) Подробное описание двух вызываемых типов в языке Q#: *операции* для действий над кубитами и квантовыми системами и *функции* строго для работы с классическими данными. 
    Здесь также описано, как определять и вызывать эти типы, в том числе сопряженные и контролируемые версии квантовых операций.

- [Локальные переменные.](xref:microsoft.quantum.guide.variables) Описание роли переменных в программах на Q# и способа их эффективного использования. 
    В частности, вы найдете здесь сведения об областях привязки, узнаете разницу между неизменяемыми и изменяемыми переменными, а также научитесь назначать и переназначать их.

- [Работа с кубитами.](xref:microsoft.quantum.guide.qubits) Описание функций Q#, которые можно применять к отдельным кубитам и системам кубитов. 
    В частности, это влечет за собой их распределение, выполнение операций над ними и, в конечном счете, их измерение. 

- [Поток управления.](xref:microsoft.quantum.guide.controlflow) Подробные сведения о шаблонах программных потоков управления, доступных в Q#, включая множество стандартных методов (условное выполнение, циклы for и while и т. д.), а также специальном шаблоне квантовых вычислений "повторять до успешного выполнения".

- [Тестирование и отладка.](xref:microsoft.quantum.guide.testingdebugging) Подробное описание некоторых способов контроля правильности выполнения кода. 
    В связи с общей непрозрачностью квантовой информации, отладка квантовой программы может потребовать специальных методов. 
    К счастью, Q# поддерживает многие классические методы отладки, к которым привыкли программисты, а также квантово-специфические методы. К ним относятся создание и запуск модульных тестов в Q#, встраивание *операторов утверждений* к значениям и вероятностям в коде, а также функции `Dump`, которые выводят состояние целевого компьютера. 
    Второй способ можно использовать наряду с нашим полнофункциональным симулятором для отладки некоторых частей вычислений, обходя некоторые квантовые ограничения (такие как теорема о запрете клонирования).

### <a name="quantum-simulators-and-resource-estimators"></a>Квантовые симуляторы и средства оценки ресурсов

- [Квантовые симуляторы и основные приложения.](xref:microsoft.quantum.machines) Обзор доступных симуляторов и общей модели выполнения между основным приложением и целевыми компьютерами.

- [Симулятор полного состояния.](xref:microsoft.quantum.machines.full-state-simulator) Целевой компьютер, имитирующий полное квантовое состояние. Используется для выполнения или отладки программ небольшого размера (менее двух десятков кубитов).

- [Оценщик ресурсов.](xref:microsoft.quantum.machines.resources-estimator) Оценивает потребность в ресурсах для выполнения определенного экземпляра операции Q# на квантовом компьютере.

- [Симулятор трассировки.](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Выполняет квантовую программу без фактической имитации состояния квантового компьютера, позволяя выполнять квантовые программы с несколькими тысячами кубитов. Используется для отладки классического кода в квантовой программе, а также для оценки требуемых ресурсов.

- [Симулятор Тоффоли.](xref:microsoft.quantum.machines.toffoli-simulator) Специализированный программный симулятор квантового состояния, который умеет имитировать небольшой набор квантовых операций (X, CNOT и X с множественным управлением) для очень большого числа кубитов.

### <a name="quick-reference-pages"></a>Краткое справочное руководство

- [Магические команды IQ#](xref:microsoft.quantum.guide.quickref.iqsharp) Краткая справочная информация о магических командах IQ# в Jupyter Notebook для Q#.