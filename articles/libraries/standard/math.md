---
title: 'Математические символы в библиотеках Q # Standard'
description: 'Сведения о классических математических функциях в библиотеках Q # Standard, которые используются со встроенными типами данных.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: bec866472abc0d4327cdc570306341375395f492
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906157"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="8091d-103">Классические математические функции</span><span class="sxs-lookup"><span data-stu-id="8091d-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="8091d-104">Эти функции в основном используются для работы с встроенными типами данных Q # `Int`, `Double`и `Range`.</span><span class="sxs-lookup"><span data-stu-id="8091d-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="8091d-105"><xref:microsoft.quantum.intrinsic.random>ная операция имеет `(Double[] => Int)`сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="8091d-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="8091d-106">Он принимает массив значений типа Double в качестве входных данных и возвращает в массиве в качестве `Int`индекс случайного выбора.</span><span class="sxs-lookup"><span data-stu-id="8091d-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="8091d-107">Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="8091d-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="8091d-108">n элементов массива, равных нулю, пропускаются, и их индексы никогда не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="8091d-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="8091d-109">Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8091d-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
