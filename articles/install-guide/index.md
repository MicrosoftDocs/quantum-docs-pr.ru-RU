---
title: Установка пакета средств разработки Microsoft Quantum (QDK)
description: Узнайте, как установить комплект SDK Microsoft Quantum (QDK) в разных средах.
author: natke
ms.author: nakersha
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: a5230f506bce02c331d22d6a428b3bd92052bbd4
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327579"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="40a00-103">Установка пакета средств разработки Microsoft Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="40a00-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="40a00-104">Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="40a00-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="40a00-105">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="40a00-105">The QDK consists of:</span></span>

- <span data-ttu-id="40a00-106">Язык программирования Q#</span><span class="sxs-lookup"><span data-stu-id="40a00-106">The Q# programming language</span></span>
- <span data-ttu-id="40a00-107">Набор библиотек, абстрагирующих сложные функции в Q#</span><span class="sxs-lookup"><span data-stu-id="40a00-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="40a00-108">API-интерфейсы для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#</span><span class="sxs-lookup"><span data-stu-id="40a00-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="40a00-109">Средства для упрощения разработки</span><span class="sxs-lookup"><span data-stu-id="40a00-109">Tools to facilitate your development</span></span>

<span data-ttu-id="40a00-110">Программы Q# можно запускать как автономные приложения с помощью Visual Studio Code или Visual Studio, а также через Jupyter Notebook с ядром Jupyter IQ#.</span><span class="sxs-lookup"><span data-stu-id="40a00-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, or through Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="40a00-111">Их также можно объединять с основным приложением на языке .NET (чаще всего это C#) или Python, что позволяет вызывать квантовые операции из классической программы.</span><span class="sxs-lookup"><span data-stu-id="40a00-111">They can also be paired with a host program written in a .NET language (typically C#) or Python, enabling you to call quantum operations from inside a classical program.</span></span>

<span data-ttu-id="40a00-112">QDK доступен для нескольких сред разработки.</span><span class="sxs-lookup"><span data-stu-id="40a00-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="40a00-113">Вы можете выбрать любой из следующих вариантов.</span><span class="sxs-lookup"><span data-stu-id="40a00-113">Select your preferred setup from:</span></span>

<span data-ttu-id="40a00-114">[Разработка с помощью приложений командной строки Q#.](xref:microsoft.quantum.install.standalone) Этот вариант позволяет работать с Q# из командной строки.</span><span class="sxs-lookup"><span data-stu-id="40a00-114">[Develop with Q# command line applications](xref:microsoft.quantum.install.standalone) - Choose this approach to work with Q# from the command line.</span></span> <span data-ttu-id="40a00-115">Для этого не требуется драйвер или основная программа, включая приведенные ниже варианты.</span><span class="sxs-lookup"><span data-stu-id="40a00-115">This does not require a driver or a host program like the below options.</span></span>

<span data-ttu-id="40a00-116">[Разработка с помощью Jupyter Notebook для Q#.](xref:microsoft.quantum.install.jupyter) В этой среде можно выполнять код Q# в ячейках с внедренным текстом или разрабатывать интерактивные руководства по созданию квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="40a00-116">[Develop with Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter) - Select this environment to run Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 

<span data-ttu-id="40a00-117">[Разработка с помощью Q# и Python.](xref:microsoft.quantum.install.python) Этот вариант позволяет совместно использовать Q# и Python для создания основной программы Python, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="40a00-117">[Develop with Q# and Python](xref:microsoft.quantum.install.python) - Enables you to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>

<span data-ttu-id="40a00-118">[Разработка с помощью Q# и .NET.](xref:microsoft.quantum.install.cs) Этот вариант позволяет совместно использовать Q# и C#, F# или VB.NET для создания основной программы .NET, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="40a00-118">[Develop with Q# and .NET](xref:microsoft.quantum.install.cs) - Combine C#, F#, or VB.NET with Q# to create a .NET host program that calls Q# operations.</span></span>
