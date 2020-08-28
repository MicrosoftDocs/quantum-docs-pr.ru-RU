---
title: Установка пакета средств разработки Microsoft Quantum (QDK)
description: Узнайте, как установить комплект SDK Microsoft Quantum (QDK) в разных средах.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3aafe78d5910027e2836f7dce72c064e75fc4436
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863714"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Установка пакета средств разработки Microsoft Quantum (QDK)

Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием. QDK состоит из следующих компонентов:

- Язык программирования Q#.
- Набор библиотек, абстрагирующих сложные функции в Q#.
- Интерфейсы API для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#.
- Средства для упрощения разработки

Программы Q# можно запускать как автономные приложения с помощью Visual Studio Code или Visual Studio, а также через записные книжки Jupyter Notebook с ядром Jupyter IQ#.
Их также можно объединять с основным приложением на языке .NET (чаще всего это C#) или Python, что позволяет вызывать квантовые операции из классической программы.

Рабочие процессы для каждой из таких конфигураций описаны и сравниваются в статье [Способы запуска программы Q#](xref:microsoft.quantum.guide.host-programs).

Чтобы продолжить установку QDK и создание проектов Q#, выберите предпочтительный вариант:

[Разработка с помощью приложений Q#.](xref:microsoft.quantum.install.standalone) Этот вариант позволяет работать с Q# из командной строки. Для этого не требуется драйвер или основная программа, включая приведенные ниже варианты.

[Разработка с помощью записных книжек Jupyter Notebook для Q#.](xref:microsoft.quantum.install.jupyter) В этой среде можно выполнять код Q# в ячейках с внедренным текстом или разрабатывать интерактивные руководства по квантовым вычислениям. 

[Разработка с помощью Q# и Python.](xref:microsoft.quantum.install.python) Этот вариант позволяет совместно использовать Q# и Python для создания ведущей программы Python, которая вызывает операции Q#.

[Разработка с помощью Q# и .NET.](xref:microsoft.quantum.install.cs) Этот вариант позволяет использовать Q# совместно с C#, F# или VB.NET для создания ведущей программы .NET, которая вызывает операции Q#.
