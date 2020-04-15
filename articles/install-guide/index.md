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
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="5b5a8-103">Установка пакета средств разработки Microsoft Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="5b5a8-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="5b5a8-104">Узнайте, как установить пакет средств разработки Microsoft Quantum (QDK), чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="5b5a8-105">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="5b5a8-105">The QDK consists of:</span></span>

- <span data-ttu-id="5b5a8-106">язык программирования Q#;</span><span class="sxs-lookup"><span data-stu-id="5b5a8-106">the Q# programming language</span></span>
- <span data-ttu-id="5b5a8-107">набор библиотек, абстрагирующих сложные функции в Q#;</span><span class="sxs-lookup"><span data-stu-id="5b5a8-107">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="5b5a8-108">API-интерфейсы для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#</span><span class="sxs-lookup"><span data-stu-id="5b5a8-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="5b5a8-109">средства для упрощения разработки.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-109">tools to facilitate your development</span></span>

<span data-ttu-id="5b5a8-110">Программы Q# часто связаны с основной программой, написанной на языке .NET (обычно C#) или Python.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-110">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="5b5a8-111">Это позволяет вызывать квантовые операции из классической программы.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-111">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="5b5a8-112">Кроме того, QDK предоставляет поддержку Q# для Jupyter Notebook с ядром IQ# Jupyter.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-112">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="5b5a8-113">QDK доступен для нескольких сред разработки.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-113">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="5b5a8-114">Выберите предпочитаемую настройку из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="5b5a8-114">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="5b5a8-115">[Установка Q# для C#:](xref:microsoft.quantum.install.cs) выберите эту среду, если вы хотите объединить C# и Q# для создания основной программы на C#, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-115">[Install Q# for C#:](xref:microsoft.quantum.install.cs) choose this environment if you want to combine C# and Q# to create a C# host program that calls Q# operations.</span></span>
- <span data-ttu-id="5b5a8-116">[Установка Q# для Python:](xref:microsoft.quantum.install.python) выберите эту среду, если хотите объединить Python и Q# для создания основной программы Python, которая вызывает операции Q#.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-116">[Install Q# for Python:](xref:microsoft.quantum.install.python) choose this environment if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="5b5a8-117">[Установка Q# для Jupyter Notebook:](xref:microsoft.quantum.install.jupyter) выберите эту среду для выполнения кода Q# в ячейках с внедренным текстом или создайте интерактивные учебники по созданию квантовых вычислений.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-117">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> <span data-ttu-id="5b5a8-118">Не выбирайте эту среду, если хотите объединить Q# с внешней классической основной программой.</span><span class="sxs-lookup"><span data-stu-id="5b5a8-118">Do not choose this environment if you want to combine Q# with an external classical host program.</span></span>
