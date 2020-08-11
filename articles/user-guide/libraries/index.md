---
title: Библиотека пакета средств разработки Quantum
description: Общие сведения о стандартной библиотеке, а также о библиотеках химии и числовых значений в составе Microsoft Quantum Development Kit.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries
no-loc:
- Q#
- $$v
ms.openlocfilehash: d61fe459362fdb5f3550768a26b34656a8a538a7
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869109"
---
# <a name="overview-of-no-locq-libraries"></a><span data-ttu-id="1fdc8-103">Обзор библиотек Q#</span><span class="sxs-lookup"><span data-stu-id="1fdc8-103">Overview of Q# Libraries</span></span>
<span data-ttu-id="1fdc8-104">Quantum Development Kit включает несколько библиотек, которые упрощают разработку квантовых приложений на языке Q#.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-104">The Quantum Development Kit is provided with several libraries to make it easier to develop quantum applications in Q#.</span></span>
<span data-ttu-id="1fdc8-105">В этом разделе документации описываются эти библиотеки и способы их использования в программах.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-105">In this section of the documentation, we describe these libraries and how to use them in your programs.</span></span>

- <span data-ttu-id="1fdc8-106">[**Стандартные библиотеки.** ](xref:microsoft.quantum.libraries.standard.intro) В этом разделе собрана информация о вводной части, которая определяет интерфейс между программами Q# и целевыми компьютерами, и библиотеке Q# canon, которая предоставляет операции и функции общего назначения для использования при написании программ Q#.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-106">[**Standard libraries**](xref:microsoft.quantum.libraries.standard.intro): This section describes the prelude, which defines the interface between Q# programs and target machines, and the canon, a Q# library that provides general-purpose operations and functions for use in writing Q# programs.</span></span>
- <span data-ttu-id="1fdc8-107">[**Библиотека Quantum Chemistry.** ](xref:microsoft.quantum.chemistry.concepts.intro) В этом разделе описывается библиотека для квантовой химии, которая содержит модель данных для загрузки гамильтоновых представлений фермионов, а также операции и функции квантового моделирования для работы с этими представлениями.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-107">[**Quantum chemistry library**](xref:microsoft.quantum.chemistry.concepts.intro): This section describes the quantum chemistry library, which provides a data model for loading representations of fermionic Hamiltonians and quantum simulation operations and functions which act on these representations.</span></span>
- <span data-ttu-id="1fdc8-108">[**Квантовая библиотека числовых значений.** ](xref:microsoft.quantum.numerics.intro) В этом разделе описывается квантовая библиотека числовых значений, которая предоставляет реализации большого набора математических функций.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-108">[**Quantum numerics library**](xref:microsoft.quantum.numerics.intro): This section describes the quantum numerics library, which provides implementations for a host of mathematical functions.</span></span> <span data-ttu-id="1fdc8-109">Она поддерживает целочисленные значения (со знаком и без знака) и представления с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-109">It supports integer (signed & unsigned) and fixed-point representations.</span></span>
- <span data-ttu-id="1fdc8-110">[**Библиотека квантового машинного обучения.** ](xref:microsoft.quantum.machine-learning.concepts.intro) В этом разделе описывается библиотека квантового машинного обучения. Она предоставляет реализацию последовательных классификаторов, которые используют возможности квантовых вычислений для анализа данных.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-110">[**Quantum machine learning library**](xref:microsoft.quantum.machine-learning.concepts.intro): This section describes the quantum machine learning library, which provides an implementation of the sequential classifiers that take advantage of quantum computing to understand data.</span></span>

<span data-ttu-id="1fdc8-111">Исходный код этих библиотек и примеры использования можно получить на GitHub.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-111">Sources of the libraries as well as code samples can be obtained from GitHub.</span></span>
<span data-ttu-id="1fdc8-112">См. сведения в разделе [Лицензирование](xref:microsoft.quantum.libraries.licensing).</span><span class="sxs-lookup"><span data-stu-id="1fdc8-112">See [Licensing](xref:microsoft.quantum.libraries.licensing) for further information.</span></span> <span data-ttu-id="1fdc8-113">Учтите, что для библиотек можно использовать ссылки на пакеты (двоичные файлы). Это альтернативный способ включать библиотеки в проекты.</span><span class="sxs-lookup"><span data-stu-id="1fdc8-113">Note that package references ("binaries") are available also for the libraries and offer another way of including the libraries in projects.</span></span>
<span data-ttu-id="1fdc8-114">Например, их очень удобно получать с помощью [NuGet](https://nuget.org).</span><span class="sxs-lookup"><span data-stu-id="1fdc8-114">A convenient way of obtaining them is via [NuGet](https://nuget.org).</span></span>
