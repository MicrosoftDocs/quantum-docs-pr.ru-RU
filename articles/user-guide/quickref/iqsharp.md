---
title: Я Q# волшебю команды
description: Краткий справочник по Q# командам automagic с помощью Q# записных книжек Jupyter
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: reference
uid: microsoft.quantum.guide.quickref.iqsharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: bb6517b782a82c1cb159951af41df9bfde51c0bb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858538"
---
# <a name="ino-locq-magic-commands"></a>Я Q# волшебю команды

### <a name="general"></a>Общие сведения

- [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): Разрешает задавать параметры конфигурации или выполнять запросы к ним.
- [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): Выполняет заданную функцию или операцию на целевом компьютере Ресаурцесестиматор.
- [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic)— Возвращает список всех доступных в настоящее время команд Magic.
- [`%lsopen`](xref:microsoft.quantum.iqsharp.magic-ref.lsopen): Список пространств имен, открытых в настоящее время, и их псевдонимов.
- [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package)— Предоставляет возможность загрузки пакета NuGet.
- [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance): Сообщает текущие метрики производительности для этого ядра.
- [`%project`](xref:microsoft.quantum.iqsharp.magic-ref.project): Предоставляет возможность просмотра или добавления Q# ссылок на проекты. 
- [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): Выполняет заданную функцию или операцию на целевом компьютере Куантумсимулатор.
- [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): Выполняет заданную функцию или операцию на целевом компьютере Тоффолисимулатор.
- [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Перечисляет Q# операции, доступные в текущем сеансе.
- [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): Предоставляет действия, связанные с текущей рабочей областью.

### <a name="azure-quantum-integration"></a>Интеграция тактовой задержки Azure

- [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Подключается к рабочей области такта Azure или отображает текущее состояние соединения.
- [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute)— Отправка задания в рабочую область такта Azure и ожидание завершения.
- [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): Отображает список заданий в текущей рабочей области такта Azure.
- [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): Отображение результатов для задания в текущей рабочей области такта Azure.
- [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): Отображает состояние задания в текущей рабочей области такта Azure.
- [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit)— Отправляет задание в рабочую область такта Azure.
- [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Задает или отображает активный целевой объект запуска для Q# отправки задания в рабочей области такта Azure.

### <a name="chemistry-from-microsoftquantumchemistry-package"></a>Химия (из пакета Microsoft. тактов. химия)

- [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): Загружает и возвращает представление проблем с электронной структурой Брумбридже из заданного YAML-файла.
- [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Кодирует фермион Хамилтониан в формат, используемый Q# .
- [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Добавляет термины в фермион Хамилтониан.
- [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): Загружает Хамилтониан фермион для проблемы с электронной структурой. Проблема загружается из файла или передается в качестве аргумента.
- [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Загружает ошибку электронной структуры Брумбридже и возвращает выбранное состояние входа.

### <a name="katas-from-microsoftquantumkatas-package"></a>Катас (из пакета Microsoft. тактов. Катас)

- [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): Выполняет один тест и сообщает, успешно ли пройден тест.
- [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): Проверяет эталонную реализацию для теста одного Ката.
    В частности, он заменяет эталонную реализацию для отдельной задачи на ячейку и сообщает, успешно ли прошел тест.
