---
title: 'Математические символы в библиотеках Q # Standard'
description: 'Сведения о классических математических функциях в библиотеках Q # Standard, которые используются со встроенными типами данных.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: bec866472abc0d4327cdc570306341375395f492
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275660"
---
# <a name="classical-mathematical-functions"></a>Классические математические функции #

Эти функции в основном используются для работы с встроенными типами данных Q # `Int` , `Double` и `Range` .

<xref:microsoft.quantum.intrinsic.random>Операция имеет подпись `(Double[] => Int)` .
Он принимает массив значений типа Double в качестве входных данных и возвращает в массиве индекс в виде случайного выбора `Int` .
Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе. n элементов массива, равных нулю, пропускаются, и их индексы никогда не возвращаются.
Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.
