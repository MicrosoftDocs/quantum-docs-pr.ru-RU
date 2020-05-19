---
title: Установка пакета средств разработки Microsoft Quantum (QDK)
description: Узнайте, как установить комплект SDK Microsoft Quantum (QDK) в разных средах.
author: natke
ms.author: nakersha
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2041b90ba021b7640615d73c35841cc21f025ac0
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426470"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Установка пакета средств разработки Microsoft Quantum (QDK)

Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием. QDK состоит из следующих компонентов:

- Язык программирования Q#
- Набор библиотек, абстрагирующих сложные функции в Q#
- API-интерфейсы для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#
- Средства для упрощения разработки

Программы Q# можно запускать как автономные приложения с помощью Visual Studio Code или Visual Studio, а также через Jupyter Notebook с ядром Jupyter IQ#.

Их также можно объединять с основным приложением на языке .NET (чаще всего это C#) или Python, что позволяет вызывать квантовые операции из классической программы.

QDK доступен для нескольких сред разработки. Вы можете выбрать любой из следующих вариантов.

[**Разработка с помощью приложений командной строки Q#.** ](xref:microsoft.quantum.install.standalone) Этот вариант позволяет работать с Q# из командной строки. Для этого не требуется драйвер или основная программа, включая приведенные ниже варианты.

[**Разработка с помощью Jupyter Notebook для Q#.** ](xref:microsoft.quantum.install.jupyter) В этой среде можно выполнять код Q# в ячейках с внедренным текстом или создать интерактивные руководства по созданию квантовых вычислений. 

[**Разработка с помощью Q# и Python.** ](xref:microsoft.quantum.install.python) Этот вариант позволяет совместно использовать Q# и Python для создания основной программы Python, которая вызывает операции Q#.

[**Разработка с помощью Q# и .NET.** ](xref:microsoft.quantum.install.cs) Этот вариант позволяет совместно использовать Q# и C#, F# или VB.NET для создания основной программы .NET, которая вызывает операции Q#.
