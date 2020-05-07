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
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="32d28-103">Установка пакета средств разработки Microsoft Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="32d28-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="32d28-104">Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="32d28-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="32d28-105">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="32d28-105">The QDK consists of:</span></span>

- <span data-ttu-id="32d28-106">язык программирования Q#;</span><span class="sxs-lookup"><span data-stu-id="32d28-106">the Q# programming language</span></span>
- <span data-ttu-id="32d28-107">набор библиотек, абстрагирующих сложные функции в Q#;</span><span class="sxs-lookup"><span data-stu-id="32d28-107">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="32d28-108">API-интерфейсы для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#</span><span class="sxs-lookup"><span data-stu-id="32d28-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="32d28-109">средства для упрощения разработки.</span><span class="sxs-lookup"><span data-stu-id="32d28-109">tools to facilitate your development</span></span>

<span data-ttu-id="32d28-110">Программы Q# часто связаны с основной программой, написанной на языке .NET (обычно C#) или Python.</span><span class="sxs-lookup"><span data-stu-id="32d28-110">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="32d28-111">Это позволяет вызывать квантовые операции из классической программы.</span><span class="sxs-lookup"><span data-stu-id="32d28-111">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="32d28-112">Кроме того, QDK предоставляет поддержку Q# для Jupyter Notebook с ядром IQ# Jupyter.</span><span class="sxs-lookup"><span data-stu-id="32d28-112">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="32d28-113">QDK доступен для нескольких сред разработки.</span><span class="sxs-lookup"><span data-stu-id="32d28-113">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="32d28-114">Выберите предпочитаемую настройку из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="32d28-114">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="32d28-115">[Приложение командной строки Q#.](xref:microsoft.quantum.install.standalone) Выберите этот вариант, чтобы работать с Q# из командной строки.</span><span class="sxs-lookup"><span data-stu-id="32d28-115">[Q# command line application:](xref:microsoft.quantum.install.standalone) choose this approach if you want to work with Q# from the command line.</span></span> <span data-ttu-id="32d28-116">Для этого не требуется драйвер или основная программа, включая приведенные ниже варианты.</span><span class="sxs-lookup"><span data-stu-id="32d28-116">This does not require a driver or a host program like the below options.</span></span>
- <span data-ttu-id="32d28-117">[Установка Q# для Jupyter Notebook:](xref:microsoft.quantum.install.jupyter) выберите эту среду для выполнения кода Q# в ячейках с внедренным текстом или создайте интерактивные учебники по созданию квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="32d28-117">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 
- <span data-ttu-id="32d28-118">[Разработка с помощью Q# и Python.](xref:microsoft.quantum.install.python) Выберите этот вариант, чтобы совместно использовать Python и Q# для создания основной программы Python, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="32d28-118">[Develop with Q# and Python:](xref:microsoft.quantum.install.python) if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="32d28-119">[Разработка с помощью Q# и C# или F#.](xref:microsoft.quantum.install.cs) Выберите этот вариант, чтобы совместно использовать C# или F# и Q# для создания основной программы C#, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="32d28-119">[Develop with Q# and C# or F#:](xref:microsoft.quantum.install.cs) if you want to combine C# or F# and Q# to create a .NET host program that calls Q# operations.</span></span>
