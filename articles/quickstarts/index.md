---
title: Настройка пакета средств разработки Microsoft Quantum (QDK)
description: Узнайте, как настроить пакет средств разработки Microsoft Quantum для разных сред.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: quickstart
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15067f1762f4468345beee38c98e1b943081fc1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859031"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="b92ab-103">Настройка пакета средств разработки Microsoft Quantum (QDK)</span><span class="sxs-lookup"><span data-stu-id="b92ab-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="b92ab-104">Узнайте, как настроить пакет средств разработки Microsoft Quantum (QDK) для своей среды, чтобы приступить к работе с квантовым программированием.</span><span class="sxs-lookup"><span data-stu-id="b92ab-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="b92ab-105">QDK состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="b92ab-105">The QDK consists of:</span></span>

- <span data-ttu-id="b92ab-106">Язык программирования Q#.</span><span class="sxs-lookup"><span data-stu-id="b92ab-106">The Q# programming language</span></span>
- <span data-ttu-id="b92ab-107">Набор библиотек, абстрагирующих сложные функции в Q#.</span><span class="sxs-lookup"><span data-stu-id="b92ab-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="b92ab-108">Интерфейсы API для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#.</span><span class="sxs-lookup"><span data-stu-id="b92ab-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="b92ab-109">Средства для упрощения разработки</span><span class="sxs-lookup"><span data-stu-id="b92ab-109">Tools to facilitate your development</span></span>

<span data-ttu-id="b92ab-110">Программы на Q# можно запускать как автономные приложения с помощью Visual Studio Code, Visual Studio или Jupyter Notebook с ядром Jupyter IQ# либо как приложения, связанные с основной программой на языке Python или .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="b92ab-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="b92ab-111">Кроме того, программы на Q# можно запускать по сети с помощью [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) или [Docker](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="b92ab-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="b92ab-112">Параметры для настройки QDK</span><span class="sxs-lookup"><span data-stu-id="b92ab-112">Options for setting up the QDK</span></span>

<span data-ttu-id="b92ab-113">QDK можно использовать тремя способами:</span><span class="sxs-lookup"><span data-stu-id="b92ab-113">You can use the QDK in three ways:</span></span>

- <span data-ttu-id="b92ab-114">[установить QDK локально](#install-the-qdk-locally);</span><span class="sxs-lookup"><span data-stu-id="b92ab-114">[Install the QDK locally](#install-the-qdk-locally)</span></span>
- <span data-ttu-id="b92ab-115">[использовать QDK по сети](#use-the-qdk-online);</span><span class="sxs-lookup"><span data-stu-id="b92ab-115">[Use the QDK online](#use-the-qdk-online)</span></span>
- <span data-ttu-id="b92ab-116">[использовать образ Docker для QDK](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="b92ab-116">[Use a QDK Docker image](#use-the-qdk-with-docker)</span></span>

## <a name="install-the-qdk-locally"></a><span data-ttu-id="b92ab-117">Локальная установка QDK</span><span class="sxs-lookup"><span data-stu-id="b92ab-117">Install the QDK locally</span></span>

<span data-ttu-id="b92ab-118">Вы можете создавать код Q# в большинстве популярных интегрированных сред разработки, а также интегрировать Q# с другими языками, например Python и .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="b92ab-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><span data-ttu-id="b92ab-119"><b>VS Code</span><span class="sxs-lookup"><span data-stu-id="b92ab-119"><b>VS Code</span></span><br><span data-ttu-id="b92ab-120">(2019 и более поздней версии)</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-120">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><span data-ttu-id="b92ab-121"><b>Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b92ab-121"><b>Visual Studio</span></span><br><span data-ttu-id="b92ab-122">(2019 и более поздней версии)</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-122">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><span data-ttu-id="b92ab-123"><b>Jupyter Notebook</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-123"><b>Jupyter Notebooks</b></span></span></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><span data-ttu-id="b92ab-124"><b>Командная строка</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-124"><b>Command line</b></span></span></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><span data-ttu-id="b92ab-125"><b>Поддержка ОС:</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-125"><b>OS support:</b></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="b92ab-126">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="b92ab-127">Только в Windows</span><span class="sxs-lookup"><span data-stu-id="b92ab-127">Windows only</span></span></td>
        <td align="center"><span data-ttu-id="b92ab-128">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="b92ab-128">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="b92ab-129">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="b92ab-129">Windows, macOS, Linux</span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><span data-ttu-id="b92ab-130"><b>Q# (изолированный)</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-130"><b>Q# standalone</b></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-131"><a href="xref:microsoft.quantum.install.standalone">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-131"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-132"><a href="xref:microsoft.quantum.install.standalone">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-132"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-133"><a href="xref:microsoft.quantum.install.jupyter">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-133"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-134"><a href="xref:microsoft.quantum.install.standalone">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-134"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><span data-ttu-id="b92ab-135"><b>Q# и Python</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-135"><b>Q# and Python</b></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-136"><a href="xref:microsoft.quantum.install.python">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-136"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-137"><a href="xref:microsoft.quantum.install.python">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-137"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-138"><a href="xref:microsoft.quantum.install.python">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-138"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-139"><a href="xref:microsoft.quantum.install.python">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-139"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><span data-ttu-id="b92ab-140"><b>Q# и .NET (C#, F#)</b></span><span class="sxs-lookup"><span data-stu-id="b92ab-140"><b>Q# and .NET (C#, F#)</b></span></span></td> 
        <td align="center"><span data-ttu-id="b92ab-141"><a href="xref:microsoft.quantum.install.cs">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-141"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-142"><a href="xref:microsoft.quantum.install.cs">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-142"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="b92ab-143">&#10006;</span><span class="sxs-lookup"><span data-stu-id="b92ab-143">&#10006;</span></span></td>
        <td align="center"><span data-ttu-id="b92ab-144"><a href="xref:microsoft.quantum.install.cs">Установка</a></span><span class="sxs-lookup"><span data-stu-id="b92ab-144"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
   </tr>
</table>

## <a name="use-the-qdk-online"></a><span data-ttu-id="b92ab-145">Использование QDK по сети</span><span class="sxs-lookup"><span data-stu-id="b92ab-145">Use the QDK Online</span></span>

<span data-ttu-id="b92ab-146">Вы также можете создавать код Q# без локальной установки компонентов, используя такие варианты:</span><span class="sxs-lookup"><span data-stu-id="b92ab-146">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="b92ab-147">Ресурс</span><span class="sxs-lookup"><span data-stu-id="b92ab-147">Resource</span></span>|<span data-ttu-id="b92ab-148">Преимущества</span><span class="sxs-lookup"><span data-stu-id="b92ab-148">Advantages</span></span>|<span data-ttu-id="b92ab-149">Ограничения</span><span class="sxs-lookup"><span data-stu-id="b92ab-149">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="b92ab-150">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="b92ab-150">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="b92ab-151">Многофункциональная подключенная среда разработки</span><span class="sxs-lookup"><span data-stu-id="b92ab-151">A rich online development environment</span></span>  |<span data-ttu-id="b92ab-152">Требуется подписка и план Azure</span><span class="sxs-lookup"><span data-stu-id="b92ab-152">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="b92ab-153">**Binder**</span><span class="sxs-lookup"><span data-stu-id="b92ab-153">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="b92ab-154">Бесплатная работа с записными книжками по сети</span><span class="sxs-lookup"><span data-stu-id="b92ab-154">Free online notebook experience</span></span> |<span data-ttu-id="b92ab-155">Без сохранения данных</span><span class="sxs-lookup"><span data-stu-id="b92ab-155">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="b92ab-156">Использование QDK с Docker</span><span class="sxs-lookup"><span data-stu-id="b92ab-156">Use the QDK with Docker</span></span>

<span data-ttu-id="b92ab-157">Вы можете использовать наш образ Docker для QDK в своей локальной установке Docker или облаке, запустив его через любую службу, которая поддерживает образы Docker, например ACI.</span><span class="sxs-lookup"><span data-stu-id="b92ab-157">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="b92ab-158">Вы можете скачать образ Docker IQ# здесь: https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span><span class="sxs-lookup"><span data-stu-id="b92ab-158">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="b92ab-159">Вы также можете использовать Docker с контейнером удаленной разработки Visual Studio Code для быстрого определения сред разработки.</span><span class="sxs-lookup"><span data-stu-id="b92ab-159">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="b92ab-160">Дополнительные сведения о контейнерах разработки VS Code см. здесь: https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span><span class="sxs-lookup"><span data-stu-id="b92ab-160">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b92ab-161">Следующие шаги</span><span class="sxs-lookup"><span data-stu-id="b92ab-161">Next steps</span></span>

<span data-ttu-id="b92ab-162">Рабочие процессы для каждой из таких конфигураций описаны и сравниваются в статье [Способы запуска программы Q#](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="b92ab-162">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
