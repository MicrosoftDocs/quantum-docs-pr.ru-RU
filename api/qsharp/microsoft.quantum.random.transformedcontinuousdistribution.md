---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Функция Трансформедконтинуаусдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 6a6e0c26bd650fd4c05208197ff23f951d1c3b5c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710945"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="d78d3-102">Функция Трансформедконтинуаусдистрибутион</span><span class="sxs-lookup"><span data-stu-id="d78d3-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="d78d3-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d78d3-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d78d3-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d78d3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d78d3-105">При наличии непрерывного распределения возвращает новое распределение, которое преобразует оригинал с помощью заданной функции.</span><span class="sxs-lookup"><span data-stu-id="d78d3-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="d78d3-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d78d3-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="d78d3-107">Преобразование: [Двойное](xref:microsoft.quantum.lang-ref.double) -> [Двойное](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d78d3-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d78d3-108">Функция, которая преобразует вариатес исходного распределения в преобразованное распределение.</span><span class="sxs-lookup"><span data-stu-id="d78d3-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="d78d3-109">распространение: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="d78d3-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="d78d3-110">Исходное распределение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="d78d3-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="d78d3-111">Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="d78d3-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="d78d3-112">Новое распределение, относящееся к `distribution` преобразованию, заданному параметром `transform` .</span><span class="sxs-lookup"><span data-stu-id="d78d3-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>