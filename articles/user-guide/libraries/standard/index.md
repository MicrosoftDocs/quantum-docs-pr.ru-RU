---
title: Знакомство со стандартными библиотеками Microsoft Q#
description: Узнайте о стандартных библиотеках Microsoft Q#, которые определяют операции, функции и типы данных, используемые в квантовых программах.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
ms.openlocfilehash: ab069c496d89a57f979732da6ccdfbe673b79726
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870589"
---
# <a name="introduction-to-the-q-standard-libraries"></a>Введение в стандартные библиотеки Q#

В дополнение к Q# предоставляется широкий набор полезных операций, функций и пользовательских типов, которые собраны в *стандартные библиотеки* Q#.
[Пакет NuGet `Microsoft.Quantum.Development.Kit`](https://www.nuget.org/packages/microsoft.quantum.development.kit), который устанавливается в процессе [установки и проверки](xref:microsoft.quantum.install), содержит компилятор Q# и элементы стандартной библиотеки, которые реализованы на целевых компьютерах.
[Пакет `Microsoft.Quantum.Standard`](https://www.nuget.org/packages/microsoft.quantum.standard) содержит другую часть стандартных библиотек Q#, переносимую между целевыми компьютерами.

Символы, определенные в стандартных библиотеках Q#, более подробно описаны в [документации по API](xref:microsoft.quantum.standardlibsintro).

В следующих разделах мы рассмотрим наиболее важные функции из каждой части стандартных библиотек и вкратце опишем контекст, в котором можно применять на практике каждую из этих функций.
