---
title: Сведения об установке пакета средств разработки Microsoft Quantum (QDK)
description: Как установить Microsoft Quantum Development Kit для сред C#, Python и Jupyter Notebook
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: bca700660094b91f1c0dfa03f9bce1336073ca51
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680194"
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

- [Приложение командной строки Q#.](xref:microsoft.quantum.install.standalone) Выберите этот вариант, чтобы работать с Q# из командной строки. Для этого не требуется драйвер или основная программа, включая приведенные ниже варианты.
- [Установка Q# для Jupyter Notebook:](xref:microsoft.quantum.install.jupyter) выберите эту среду для выполнения кода Q# в ячейках с внедренным текстом или создайте интерактивные учебники по созданию квантовых вычислений. 
- [Разработка с помощью Q# и Python.](xref:microsoft.quantum.install.python) Выберите этот вариант, чтобы совместно использовать Python и Q# для создания основной программы Python, которая вызывает операции Q#.
- [Разработка с помощью Q# и C# или F#.](xref:microsoft.quantum.install.cs) Выберите этот вариант, чтобы совместно использовать C# или F# и Q# для создания основной программы C#, которая вызывает операции Q#.
