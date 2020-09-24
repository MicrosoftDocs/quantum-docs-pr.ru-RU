---
title: Настройка пакета средств разработки Microsoft Quantum (QDK)
description: Узнайте, как настроить пакет средств разработки Microsoft Quantum для разных сред.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834488"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="fcb94-103">Настройка пакета средств разработки Microsoft Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="fcb94-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="fcb94-104">Узнайте, как настроить пакет средств разработки Microsoft Quantum (QDK) для своей среды, чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="fcb94-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="fcb94-105">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="fcb94-105">The QDK consists of:</span></span>

- <span data-ttu-id="fcb94-106">Язык программирования Q#.</span><span class="sxs-lookup"><span data-stu-id="fcb94-106">The Q# programming language</span></span>
- <span data-ttu-id="fcb94-107">Набор библиотек, абстрагирующих сложные функции в Q#.</span><span class="sxs-lookup"><span data-stu-id="fcb94-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="fcb94-108">Интерфейсы API для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#.</span><span class="sxs-lookup"><span data-stu-id="fcb94-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="fcb94-109">Средства для упрощения разработки</span><span class="sxs-lookup"><span data-stu-id="fcb94-109">Tools to facilitate your development</span></span>

<span data-ttu-id="fcb94-110">Программы на Q# можно запускать как автономные приложения с помощью Visual Studio Code, Visual Studio или Jupyter Notebook с ядром Jupyter IQ# либо как приложения, связанные с основной программой на языке Python или .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="fcb94-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="fcb94-111">Кроме того, программы на Q# можно запускать по сети с помощью [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) или [Docker](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="fcb94-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="fcb94-112">Параметры для настройки QDK</span><span class="sxs-lookup"><span data-stu-id="fcb94-112">Options for setting up the QDK</span></span>

<span data-ttu-id="fcb94-113">QDK можно использовать тремя способами:</span><span class="sxs-lookup"><span data-stu-id="fcb94-113">You can use the QDK in three ways:</span></span>

- <span data-ttu-id="fcb94-114">[установить QDK локально](#install-the-qdk-locally);</span><span class="sxs-lookup"><span data-stu-id="fcb94-114">[Install the QDK locally](#install-the-qdk-locally)</span></span>
- <span data-ttu-id="fcb94-115">[использовать QDK по сети](#use-the-qdk-online);</span><span class="sxs-lookup"><span data-stu-id="fcb94-115">[Use the QDK online](#use-the-qdk-online)</span></span>
- <span data-ttu-id="fcb94-116">[использовать образ Docker для QDK](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="fcb94-116">[Use a QDK Docker image](#use-the-qdk-with-docker)</span></span>

## <a name="install-the-qdk-locally"></a><span data-ttu-id="fcb94-117">Локальная установка QDK</span><span class="sxs-lookup"><span data-stu-id="fcb94-117">Install the QDK locally</span></span>

<span data-ttu-id="fcb94-118">Вы можете создавать код Q# в большинстве популярных интегрированных сред разработки, а также интегрировать Q# с другими языками, например Python и .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="fcb94-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

|&nbsp; | <span data-ttu-id="fcb94-119">**VS Code<br>(2019 или более поздней версии)**</span><span class="sxs-lookup"><span data-stu-id="fcb94-119">**VS Code<br>(2019 or later)**</span></span>| <span data-ttu-id="fcb94-120">**Visual Studio<br>(2019 или более поздней версии)**</span><span class="sxs-lookup"><span data-stu-id="fcb94-120">**Visual Studio<br>(2019 or later)**</span></span> | <span data-ttu-id="fcb94-121">**Jupyter Notebook**</span><span class="sxs-lookup"><span data-stu-id="fcb94-121">**Jupyter Notebooks**</span></span> | <span data-ttu-id="fcb94-122">**Командная строка**</span><span class="sxs-lookup"><span data-stu-id="fcb94-122">**Command line**</span></span>|
|:-----|:-----:|:-----:|:-----:|:-----:|
|<span data-ttu-id="fcb94-123">**Операционная система**</span><span class="sxs-lookup"><span data-stu-id="fcb94-123">**OS**</span></span> |<span data-ttu-id="fcb94-124">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="fcb94-124">Windows, macOS, Linux</span></span> |<span data-ttu-id="fcb94-125">Только в Windows</span><span class="sxs-lookup"><span data-stu-id="fcb94-125">Windows only</span></span> |<span data-ttu-id="fcb94-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="fcb94-126">Windows, macOS, Linux</span></span> |<span data-ttu-id="fcb94-127">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="fcb94-127">Windows, macOS, Linux</span></span> |
|<br><span data-ttu-id="fcb94-128">**Q# (изолированный)**</span><span class="sxs-lookup"><span data-stu-id="fcb94-128">**Q# standalone**</span></span> |<br>[<span data-ttu-id="fcb94-129">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-129">Install</span></span>](xref:microsoft.quantum.install.standalone) |<br> [<span data-ttu-id="fcb94-130">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-130">Install</span></span>](xref:microsoft.quantum.install.standalone)  |<br> [<span data-ttu-id="fcb94-131">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-131">Install</span></span>](xref:microsoft.quantum.install.jupyter) |<br>[<span data-ttu-id="fcb94-132">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-132">Install</span></span>](xref:microsoft.quantum.install.standalone)|
|<span data-ttu-id="fcb94-133">**Q# и Python**</span><span class="sxs-lookup"><span data-stu-id="fcb94-133">**Q#  and Python**</span></span> |[<span data-ttu-id="fcb94-134">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-134">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="fcb94-135">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-135">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="fcb94-136">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-136">Install</span></span>](xref:microsoft.quantum.install.jupyter) |[<span data-ttu-id="fcb94-137">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-137">Install</span></span>](xref:microsoft.quantum.install.python) |
|<span data-ttu-id="fcb94-138">**Q# и .NET (C#, F#)**</span><span class="sxs-lookup"><span data-stu-id="fcb94-138">**Q# and .NET (C#, F#)**</span></span>|[<span data-ttu-id="fcb94-139">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-139">Install</span></span>](xref:microsoft.quantum.install.cs) |[<span data-ttu-id="fcb94-140">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-140">Install</span></span>](xref:microsoft.quantum.install.cs)|<span data-ttu-id="fcb94-141">&#10006;</span><span class="sxs-lookup"><span data-stu-id="fcb94-141">&#10006;</span></span> |[<span data-ttu-id="fcb94-142">Установка</span><span class="sxs-lookup"><span data-stu-id="fcb94-142">Install</span></span>](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a><span data-ttu-id="fcb94-143">Использование QDK по сети</span><span class="sxs-lookup"><span data-stu-id="fcb94-143">Use the QDK Online</span></span>

<span data-ttu-id="fcb94-144">Вы также можете создавать код Q# без локальной установки компонентов, используя такие варианты:</span><span class="sxs-lookup"><span data-stu-id="fcb94-144">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="fcb94-145">Ресурс</span><span class="sxs-lookup"><span data-stu-id="fcb94-145">Resource</span></span>|<span data-ttu-id="fcb94-146">Преимущества</span><span class="sxs-lookup"><span data-stu-id="fcb94-146">Advantages</span></span>|<span data-ttu-id="fcb94-147">Ограничения</span><span class="sxs-lookup"><span data-stu-id="fcb94-147">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="fcb94-148">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="fcb94-148">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="fcb94-149">Многофункциональная подключенная среда разработки</span><span class="sxs-lookup"><span data-stu-id="fcb94-149">A rich online development environment</span></span>  |<span data-ttu-id="fcb94-150">Требуется подписка и план Azure</span><span class="sxs-lookup"><span data-stu-id="fcb94-150">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="fcb94-151">**Binder**</span><span class="sxs-lookup"><span data-stu-id="fcb94-151">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="fcb94-152">Бесплатная работа с записными книжками по сети</span><span class="sxs-lookup"><span data-stu-id="fcb94-152">Free online notebook experience</span></span> |<span data-ttu-id="fcb94-153">Без сохранения данных</span><span class="sxs-lookup"><span data-stu-id="fcb94-153">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="fcb94-154">Использование QDK с Docker</span><span class="sxs-lookup"><span data-stu-id="fcb94-154">Use the QDK with Docker</span></span>

<span data-ttu-id="fcb94-155">Вы можете использовать наш образ Docker для QDK в своей локальной установке Docker или облаке, запустив его через любую службу, которая поддерживает образы Docker, например ACI.</span><span class="sxs-lookup"><span data-stu-id="fcb94-155">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="fcb94-156">Вы можете скачать образ Docker IQ# здесь: https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span><span class="sxs-lookup"><span data-stu-id="fcb94-156">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="fcb94-157">Вы также можете использовать Docker с контейнером удаленной разработки Visual Studio Code для быстрого определения сред разработки.</span><span class="sxs-lookup"><span data-stu-id="fcb94-157">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="fcb94-158">Дополнительные сведения о контейнерах разработки VS Code см. здесь: https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span><span class="sxs-lookup"><span data-stu-id="fcb94-158">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fcb94-159">Следующие шаги</span><span class="sxs-lookup"><span data-stu-id="fcb94-159">Next steps</span></span>

<span data-ttu-id="fcb94-160">Рабочие процессы для каждой из таких конфигураций описаны и сравниваются в статье [Способы запуска программы Q#](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="fcb94-160">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
