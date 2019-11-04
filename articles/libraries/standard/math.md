---
title: 'Q # Стандартные библиотеки — математика | Документация Майкрософт'
description: 'Q # Стандартные библиотеки — математика'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 7ac9d321f59f7cc95ad8939a4cf7c36e0c5e0491
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184463"
---
# <a name="classical-mathematical-functions"></a>Классические математические функции #

Эти функции в основном используются для работы с встроенными типами данных Q # `Int`, `Double`и `Range`.

<xref:microsoft.quantum.intrinsic.random>ная операция имеет `(Double[] => Int)`сигнатуры.
Он принимает массив значений типа Double в качестве входных данных и возвращает в массиве в качестве `Int`индекс случайного выбора.
Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе. n элементов массива, равных нулю, пропускаются, и их индексы никогда не возвращаются.
Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.