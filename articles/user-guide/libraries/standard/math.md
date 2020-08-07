---
title: Математические вычисления в Q# стандартных библиотеках
description: Сведения о классических математических функциях в Q# стандартных библиотеках, которые используются со встроенными типами данных.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4a3747eaa2c91e482ded3af1279a0e40d922bfb3
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868429"
---
# <a name="classical-mathematical-functions"></a>Классические математические функции #

Эти функции в основном используются для работы со Q# встроенными типами данных `Int` , `Double` и `Range` .

<xref:microsoft.quantum.intrinsic.random>Операция имеет подпись `(Double[] => Int)` .
Он принимает массив значений типа Double в качестве входных данных и возвращает в массиве индекс в виде случайного выбора `Int` .
Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе. n элементов массива, равных нулю, пропускаются, и их индексы никогда не возвращаются.
Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.
