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
# <a name="classical-mathematical-functions"></a><span data-ttu-id="ca991-103">Классические математические функции</span><span class="sxs-lookup"><span data-stu-id="ca991-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="ca991-104">Эти функции в основном используются для работы с встроенными типами данных Q # `Int` , `Double` и `Range` .</span><span class="sxs-lookup"><span data-stu-id="ca991-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="ca991-105"><xref:microsoft.quantum.intrinsic.random>Операция имеет подпись `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="ca991-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="ca991-106">Он принимает массив значений типа Double в качестве входных данных и возвращает в массиве индекс в виде случайного выбора `Int` .</span><span class="sxs-lookup"><span data-stu-id="ca991-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="ca991-107">Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе.</span><span class="sxs-lookup"><span data-stu-id="ca991-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="ca991-108">n элементов массива, равных нулю, пропускаются, и их индексы никогда не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="ca991-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="ca991-109">Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ca991-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
