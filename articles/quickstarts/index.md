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

|&nbsp; | **VS Code<br>(2019 или более поздней версии)**| **Visual Studio<br>(2019 или более поздней версии)** | **Jupyter Notebook** | **Командная строка**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|**Операционная система** |Windows, macOS, Linux |Только в Windows |Windows, macOS, Linux |Windows, macOS, Linux |
|<br>**Q# (изолированный)** |<br>[Установка](xref:microsoft.quantum.install.standalone) |<br> [Установка](xref:microsoft.quantum.install.standalone)  |<br> [Установка](xref:microsoft.quantum.install.jupyter) |<br>[Установка](xref:microsoft.quantum.install.standalone)|
|**Q# и Python** |[Установка](xref:microsoft.quantum.install.python) |[Установка](xref:microsoft.quantum.install.python) |[Установка](xref:microsoft.quantum.install.jupyter) |[Установка](xref:microsoft.quantum.install.python) |
|**Q# и .NET (C#, F#)**|[Установка](xref:microsoft.quantum.install.cs) |[Установка](xref:microsoft.quantum.install.cs)|&#10006; |[Установка](xref:microsoft.quantum.install.cs) |

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
