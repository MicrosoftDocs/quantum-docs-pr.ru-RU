---
title: 'Математические вычисления в Q# стандартных библиотеках'
description: 'Сведения о классических математических функциях в Q# стандартных библиотеках, которые используются со встроенными типами данных.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: article
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 6de1574341d67c569cd2f040ec533e263fdd386e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92692063"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="765d6-103">Классические математические функции</span><span class="sxs-lookup"><span data-stu-id="765d6-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="765d6-104">Эти функции в основном используются для работы со Q# встроенными типами данных `Int` , `Double` и `Range` .</span><span class="sxs-lookup"><span data-stu-id="765d6-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="765d6-105"><xref:Microsoft.Quantum.Intrinsic.Random>Операция имеет подпись `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="765d6-105">The <xref:Microsoft.Quantum.Intrinsic.Random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="765d6-106">Он принимает массив значений типа Double в качестве входных данных и возвращает в массиве индекс в виде случайного выбора `Int` .</span><span class="sxs-lookup"><span data-stu-id="765d6-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="765d6-107">Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="765d6-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="765d6-108">n элементов массива, равных нулю, пропускаются, и их индексы никогда не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="765d6-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="765d6-109">Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="765d6-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
