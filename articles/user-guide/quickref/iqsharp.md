---
title: Магические команды IQ#
description: 'Краткая справочная страница для команд IQ # Magic с записными книжками Q # Jupyter'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 2fb542df8723fa437c82b4a1dfada77e22c1d6e4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870551"
---
# <a name="iq-magic-commands"></a>Магические команды IQ#

### <a name="general"></a>Общие сведения

- [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): Разрешает задавать параметры конфигурации или выполнять запросы к ним.
- [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): Выполняет заданную функцию или операцию на целевом компьютере Ресаурцесестиматор.
- [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic)— Возвращает список всех доступных в настоящее время команд Magic.
- [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package)— Предоставляет возможность загрузки пакета NuGet.
- [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance): Сообщает текущие метрики производительности для этого ядра.
- [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): Выполняет заданную функцию или операцию на целевом компьютере Куантумсимулатор.
- [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): Выполняет заданную функцию или операцию на целевом компьютере Тоффолисимулатор.
- [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Список операций Q #, доступных в текущем сеансе.
- [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): Предоставляет действия, связанные с текущей рабочей областью.

### <a name="azure-quantum-integration"></a>Интеграция тактовой задержки Azure

- [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Подключается к рабочей области такта Azure или отображает текущее состояние соединения.
- [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Выполняет задание в рабочей области такта Azure.
- [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): Отображает список заданий в текущей рабочей области такта Azure.
- [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): Отображение результатов для задания в текущей рабочей области такта Azure.
- [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): Отображает состояние задания в текущей рабочей области такта Azure.
- [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit)— Отправляет задание в рабочую область такта Azure.
- [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Задает или отображает активный целевой объект выполнения для отправки задания Q # в рабочей области такта Azure.

### <a name="chemistry-from-microsoftquantumchemistry-package"></a>Химия (из пакета Microsoft. тактов. химия)

- [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): Загружает и возвращает представление проблем с электронной структурой Брумбридже из заданного YAML-файла.
- [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Кодирует фермион Хамилтониан в формат, который можно использовать в Q #.
- [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Добавляет термины в фермион Хамилтониан.
- [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): Загружает Хамилтониан фермион для проблемы с электронной структурой. Проблема загружается из файла или передается в качестве аргумента.
- [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Загружает ошибку электронной структуры Брумбридже и возвращает выбранное состояние входа.

### <a name="katas-from-microsoftquantumkatas-package"></a>Катас (из пакета Microsoft. тактов. Катас)

- [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): Выполняет один тест и сообщает, успешно ли пройден тест.
- [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): Проверяет эталонную реализацию для теста одного Ката.
    В частности, он заменяет эталонную реализацию для отдельной задачи на ячейку и сообщает, успешно ли прошел тест.
