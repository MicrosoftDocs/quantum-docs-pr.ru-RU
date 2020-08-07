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
# <a name="classical-mathematical-functions"></a><span data-ttu-id="944df-103">Классические математические функции</span><span class="sxs-lookup"><span data-stu-id="944df-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="944df-104">Эти функции в основном используются для работы со Q# встроенными типами данных `Int` , `Double` и `Range` .</span><span class="sxs-lookup"><span data-stu-id="944df-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="944df-105"><xref:microsoft.quantum.intrinsic.random>Операция имеет подпись `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="944df-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="944df-106">Он принимает массив значений типа Double в качестве входных данных и возвращает в массиве индекс в виде случайного выбора `Int` .</span><span class="sxs-lookup"><span data-stu-id="944df-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="944df-107">Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="944df-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="944df-108">n элементов массива, равных нулю, пропускаются, и их индексы никогда не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="944df-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="944df-109">Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="944df-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
