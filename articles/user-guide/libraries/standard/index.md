---
title: Знакомство со стандартными библиотеками Microsoft Q#
description: Сведения о стандартных библиотеках Microsoft Q#, которые определяют операции, функции и типы данных, используемые в квантовых программах.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4db227fcf159331f9f8456c474ce6d64111c21df
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868480"
---
# <a name="introduction-to-the-no-locq-standard-libraries"></a>Введение в стандартные библиотеки Q#

В дополнение к Q# предоставляется широкий набор полезных операций, функций и пользовательских типов, которые собраны в *стандартные библиотеки* Q#.
[Пакет NuGet `Microsoft.Quantum.Development.Kit`](https://www.nuget.org/packages/microsoft.quantum.development.kit), который устанавливается в процессе [установки и проверки](xref:microsoft.quantum.install), содержит компилятор Q# и элементы стандартной библиотеки, которые реализованы на целевых компьютерах.
[Пакет `Microsoft.Quantum.Standard`](https://www.nuget.org/packages/microsoft.quantum.standard) содержит другую часть стандартных библиотек Q#, переносимых между целевыми компьютерами.

Символы, определенные в стандартных библиотеках Q#, более подробно описаны в [документации по API](xref:microsoft.quantum.standardlibsintro).

В следующих разделах мы рассмотрим наиболее важные функции из каждой части стандартных библиотек и вкратце опишем контекст, в котором можно применять на практике каждую из этих функций.
