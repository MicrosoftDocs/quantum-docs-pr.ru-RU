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
ms.openlocfilehash: c6e128ea8b3845336fb692d2bceefda998b935d9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228854"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a>Настройка пакета средств разработки Microsoft Quantum (QDK)

Узнайте, как настроить пакет средств разработки Microsoft Quantum (QDK) для своей среды, чтобы приступить к работе с квантовым программированием. QDK состоит из следующих компонентов:

- Язык программирования Q#.
- Набор библиотек, абстрагирующих сложные функции в Q#.
- Интерфейсы API для Python и языков .NET (C#, F# и VB.NET) для запуска квантовых программ, написанных на Q#.
- Средства для упрощения разработки

Программы на Q# можно запускать как автономные приложения с помощью Visual Studio Code, Visual Studio или Jupyter Notebook с ядром Jupyter IQ# либо как приложения, связанные с основной программой на языке Python или .NET (C#, F#). Кроме того, программы на Q# можно запускать по сети с помощью [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) или [Docker](#use-the-qdk-with-docker). 

## <a name="options-for-setting-up-the-qdk"></a>Параметры для настройки QDK

QDK можно использовать тремя способами:

- [установить QDK локально](#install-the-qdk-locally);
- [использовать QDK по сети](#use-the-qdk-online);
- [использовать образ Docker для QDK](#use-the-qdk-with-docker).

## <a name="install-the-qdk-locally"></a>Локальная установка QDK

Вы можете создавать код Q# в большинстве популярных интегрированных сред разработки, а также интегрировать Q# с другими языками, например Python и .NET (C#, F#).

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><b>VS Code<br>(2019 и более поздней версии)</b></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><b>Visual Studio<br>(2019 и более поздней версии)</b></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><b>Jupyter Notebook</b></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><b>Командная строка</b></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><b>Поддержка ОС:</b></td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Только в Windows</td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Windows, macOS, Linux</td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><b>Q# (изолированный)</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Установка</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Установка</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.jupyter">Установка</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Установка</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><b>Q# и Python</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Установка</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Установка</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Установка</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Установка</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><b>Q# и .NET (C#, F#)</b></td> 
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Установка</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Установка</a></td>
        <td align="center">&#10006;</td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Установка</a></td>
   </tr>
</table>

## <a name="use-the-qdk-online"></a>Использование QDK по сети

Вы также можете создавать код Q# без локальной установки компонентов, используя такие варианты:

|Ресурс|Преимущества|Ограничения|
|---|---|---|
|[**Visual Studio Codespaces**](xref:microsoft.quantum.install.standalone)|Многофункциональная подключенная среда разработки  |Требуется подписка и план Azure |
|[**Binder**](xref:microsoft.quantum.install.binder) | Бесплатная работа с записными книжками по сети |Без сохранения данных |

## <a name="use-the-qdk-with-docker"></a>Использование QDK с Docker

Вы можете использовать наш образ Docker для QDK в своей локальной установке Docker или облаке, запустив его через любую службу, которая поддерживает образы Docker, например ACI.

Вы можете скачать образ Docker IQ# здесь: https://github.com/microsoft/iqsharp/#using-iq-as-a-container. 

Вы также можете использовать Docker с контейнером удаленной разработки Visual Studio Code для быстрого определения сред разработки. Дополнительные сведения о контейнерах разработки VS Code см. здесь: https://github.com/microsoft/Quantum/tree/master/.devcontainer.

## <a name="next-steps"></a>Следующие шаги

Рабочие процессы для каждой из таких конфигураций описаны и сравниваются в статье [Способы запуска программы Q#](xref:microsoft.quantum.guide.host-programs).
