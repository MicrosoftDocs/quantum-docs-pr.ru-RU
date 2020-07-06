---
title: Установка пакета средств разработки Microsoft Quantum (QDK)
description: Узнайте, как установить комплект SDK Microsoft Quantum (QDK) в разных средах.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: ee8d210d67a20cfea3bdc36162efc47f021a6dc6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885470"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Установка пакета средств разработки Microsoft Quantum (QDK)

Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием. QDK состоит из следующих компонентов:

- Язык программирования Q#
- Набор библиотек, абстрагирующих сложные функции в Q#
- API-интерфейсы для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#
- Средства для упрощения разработки

Программы Q# можно запускать как автономные приложения с помощью Visual Studio Code или Visual Studio, а также через Jupyter Notebook с ядром Jupyter IQ#.
Их также можно объединять с основным приложением на языке .NET (чаще всего это C#) или Python, что позволяет вызывать квантовые операции из классической программы.

Рабочие процессы для каждой из таких конфигураций описаны и сравниваются в статье [Способы запуска программы Q#](xref:microsoft.quantum.guide.host-programs).

Чтобы продолжить установку QDK и создание проектов Q#, выберите предпочтительный вариант:

[Разработка с помощью приложений командной строки Q#.](xref:microsoft.quantum.install.standalone) Этот вариант позволяет работать с Q# из командной строки. Для этого не требуется драйвер или основная программа, включая приведенные ниже варианты.

[Разработка с помощью Jupyter Notebook для Q#.](xref:microsoft.quantum.install.jupyter) В этой среде можно выполнять код Q# в ячейках с внедренным текстом или разрабатывать интерактивные руководства по созданию квантовых вычислений. 

[Разработка с помощью Q# и Python.](xref:microsoft.quantum.install.python) Этот вариант позволяет совместно использовать Q# и Python для создания основной программы Python, которая вызывает операции Q#.

[Разработка с помощью Q# и .NET.](xref:microsoft.quantum.install.cs) Этот вариант позволяет совместно использовать Q# и C#, F# или VB.NET для создания основной программы .NET, которая вызывает операции Q#.
