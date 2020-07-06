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
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="da95d-103">Установка пакета средств разработки Microsoft Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="da95d-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="da95d-104">Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="da95d-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="da95d-105">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="da95d-105">The QDK consists of:</span></span>

- <span data-ttu-id="da95d-106">Язык программирования Q#</span><span class="sxs-lookup"><span data-stu-id="da95d-106">The Q# programming language</span></span>
- <span data-ttu-id="da95d-107">Набор библиотек, абстрагирующих сложные функции в Q#</span><span class="sxs-lookup"><span data-stu-id="da95d-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="da95d-108">API-интерфейсы для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#</span><span class="sxs-lookup"><span data-stu-id="da95d-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="da95d-109">Средства для упрощения разработки</span><span class="sxs-lookup"><span data-stu-id="da95d-109">Tools to facilitate your development</span></span>

<span data-ttu-id="da95d-110">Программы Q# можно запускать как автономные приложения с помощью Visual Studio Code или Visual Studio, а также через Jupyter Notebook с ядром Jupyter IQ#.</span><span class="sxs-lookup"><span data-stu-id="da95d-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, or through Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>
<span data-ttu-id="da95d-111">Их также можно объединять с основным приложением на языке .NET (чаще всего это C#) или Python, что позволяет вызывать квантовые операции из классической программы.</span><span class="sxs-lookup"><span data-stu-id="da95d-111">They can also be paired with a host program written in a .NET language (typically C#) or Python, enabling you to call quantum operations from inside a classical program.</span></span>

<span data-ttu-id="da95d-112">Рабочие процессы для каждой из таких конфигураций описаны и сравниваются в статье [Способы запуска программы Q#](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="da95d-112">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

<span data-ttu-id="da95d-113">Чтобы продолжить установку QDK и создание проектов Q#, выберите предпочтительный вариант:</span><span class="sxs-lookup"><span data-stu-id="da95d-113">To proceed with installing the QDK and creating Q# projects, select your preferred setup:</span></span>

<span data-ttu-id="da95d-114">[Разработка с помощью приложений командной строки Q#.](xref:microsoft.quantum.install.standalone) Этот вариант позволяет работать с Q# из командной строки.</span><span class="sxs-lookup"><span data-stu-id="da95d-114">[Develop with Q# command line applications](xref:microsoft.quantum.install.standalone) - Choose this approach to work with Q# from the command line.</span></span> <span data-ttu-id="da95d-115">Для этого не требуется драйвер или основная программа, включая приведенные ниже варианты.</span><span class="sxs-lookup"><span data-stu-id="da95d-115">This does not require a driver or a host program like the below options.</span></span>

<span data-ttu-id="da95d-116">[Разработка с помощью Jupyter Notebook для Q#.](xref:microsoft.quantum.install.jupyter) В этой среде можно выполнять код Q# в ячейках с внедренным текстом или разрабатывать интерактивные руководства по созданию квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="da95d-116">[Develop with Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter) - Select this environment to run Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 

<span data-ttu-id="da95d-117">[Разработка с помощью Q# и Python.](xref:microsoft.quantum.install.python) Этот вариант позволяет совместно использовать Q# и Python для создания основной программы Python, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="da95d-117">[Develop with Q# and Python](xref:microsoft.quantum.install.python) - Enables you to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>

<span data-ttu-id="da95d-118">[Разработка с помощью Q# и .NET.](xref:microsoft.quantum.install.cs) Этот вариант позволяет совместно использовать Q# и C#, F# или VB.NET для создания основной программы .NET, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="da95d-118">[Develop with Q# and .NET](xref:microsoft.quantum.install.cs) - Combine C#, F#, or VB.NET with Q# to create a .NET host program that calls Q# operations.</span></span>
