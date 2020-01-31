---
title: Сведения об установке пакета средств разработки Microsoft Quantum (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: b209f0b600d973c3870c66060e1b484ec519322f
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820714"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="941d3-102">Установка пакета средств разработки Microsoft Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="941d3-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="941d3-103">Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="941d3-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="941d3-104">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="941d3-104">The QDK consists of:</span></span>

- <span data-ttu-id="941d3-105">язык программирования Q#;</span><span class="sxs-lookup"><span data-stu-id="941d3-105">the Q# programming language</span></span>
- <span data-ttu-id="941d3-106">набор библиотек, абстрагирующих сложные функции в Q#;</span><span class="sxs-lookup"><span data-stu-id="941d3-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="941d3-107">API для языков Python и .NET (например: C#, F#и VB.NET) для запуска квантовых программ, написанных в Q#</span><span class="sxs-lookup"><span data-stu-id="941d3-107">APIs for Python and .NET languages (i.e.: C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="941d3-108">средства для упрощения разработки.</span><span class="sxs-lookup"><span data-stu-id="941d3-108">tools to facilitate your development</span></span>

<span data-ttu-id="941d3-109">Программы Q# часто связаны с основной программой, написанной на языке .NET (обычно C#) или Python.</span><span class="sxs-lookup"><span data-stu-id="941d3-109">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="941d3-110">Это позволяет вызывать квантовые операции из классической программы.</span><span class="sxs-lookup"><span data-stu-id="941d3-110">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="941d3-111">Кроме того, QDK предоставляет поддержку Q# для Jupyter Notebook с ядром IQ# Jupyter.</span><span class="sxs-lookup"><span data-stu-id="941d3-111">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="941d3-112">QDK доступен для нескольких сред разработки.</span><span class="sxs-lookup"><span data-stu-id="941d3-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="941d3-113">Выберите предпочитаемую настройку из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="941d3-113">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="941d3-114">[Установка Q# для C#:](xref:microsoft.quantum.install.cs) выберите эту среду, если вы хотите объединить C# и Q# для создания основной программы на C#, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="941d3-114">[Install Q# for C#:](xref:microsoft.quantum.install.cs) choose this environment if you want to combine C# and Q# to create a C# host program that calls Q# operations.</span></span>
- <span data-ttu-id="941d3-115">[Установка Q# для Python:](xref:microsoft.quantum.install.python) выберите эту среду, если хотите объединить Python и Q# для создания основной программы Python, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="941d3-115">[Install Q# for Python:](xref:microsoft.quantum.install.python) choose this environment if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="941d3-116">[Установка Q# для Jupyter Notebook:](xref:microsoft.quantum.install.jupyter) выберите эту среду для выполнения кода Q# в ячейках с внедренным текстом или создайте интерактивные учебники по созданию квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="941d3-116">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> <span data-ttu-id="941d3-117">Не выбирайте эту среду, если хотите объединить Q# с внешней классической основной программой.</span><span class="sxs-lookup"><span data-stu-id="941d3-117">Do not choose this environment if you want to combine Q# with an external classical host program.</span></span>
