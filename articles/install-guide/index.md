---
title: Сведения об установке пакета средств разработки Microsoft Quantum (QDK)
description: Как установить Microsoft Quantum Development Kit для сред C#, Python и Jupyter Notebook
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 5fafb736f34d27f9233370a0a8a66c0613606048
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2020
ms.locfileid: "77904780"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Установка пакета средств разработки Microsoft Quantum (QDK)

Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием. QDK состоит из следующих компонентов:

- язык программирования Q#;
- набор библиотек, абстрагирующих сложные функции в Q#;
- API-интерфейсы для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#
- средства для упрощения разработки.

Программы Q# часто связаны с основной программой, написанной на языке .NET (обычно C#) или Python. Это позволяет вызывать квантовые операции из классической программы.
Кроме того, QDK предоставляет поддержку Q# для Jupyter Notebook с ядром IQ# Jupyter.

QDK доступен для нескольких сред разработки. Выберите предпочитаемую настройку из следующих разделов:

- [Установка Q# для C#:](xref:microsoft.quantum.install.cs) выберите эту среду, если вы хотите объединить C# и Q# для создания основной программы на C#, которая вызывает операции Q#.
- [Установка Q# для Python:](xref:microsoft.quantum.install.python) выберите эту среду, если хотите объединить Python и Q# для создания основной программы Python, которая вызывает операции Q#.
- [Установка Q# для Jupyter Notebook:](xref:microsoft.quantum.install.jupyter) выберите эту среду для выполнения кода Q# в ячейках с внедренным текстом или создайте интерактивные учебники по созданию квантовых вычислений. Не выбирайте эту среду, если хотите объединить Q# с внешней классической основной программой.
