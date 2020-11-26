---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Функция Трансформедконтинуаусдистрибутион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226270"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="ce72e-102">Функция Трансформедконтинуаусдистрибутион</span><span class="sxs-lookup"><span data-stu-id="ce72e-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="ce72e-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="ce72e-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="ce72e-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ce72e-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ce72e-105">При наличии непрерывного распределения возвращает новое распределение, которое преобразует оригинал с помощью заданной функции.</span><span class="sxs-lookup"><span data-stu-id="ce72e-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="ce72e-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ce72e-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="ce72e-107">Преобразование: [Двойное](xref:microsoft.quantum.lang-ref.double) -> [Двойное](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ce72e-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ce72e-108">Функция, которая преобразует вариатес исходного распределения в преобразованное распределение.</span><span class="sxs-lookup"><span data-stu-id="ce72e-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="ce72e-109">распространение: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="ce72e-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="ce72e-110">Исходное распределение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="ce72e-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="ce72e-111">Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="ce72e-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="ce72e-112">Новое распределение, относящееся к `distribution` преобразованию, заданному параметром `transform` .</span><span class="sxs-lookup"><span data-stu-id="ce72e-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>