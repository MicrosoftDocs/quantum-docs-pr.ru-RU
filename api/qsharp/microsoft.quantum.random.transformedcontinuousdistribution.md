---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Функция Трансформедконтинуаусдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 353442a4245a9e20bb1e4c46d2e8a84d4c9534b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857772"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="ecf62-102">Функция Трансформедконтинуаусдистрибутион</span><span class="sxs-lookup"><span data-stu-id="ecf62-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="ecf62-103">Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="ecf62-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="ecf62-104">Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ecf62-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ecf62-105">При наличии непрерывного распределения возвращает новое распределение, которое преобразует оригинал с помощью заданной функции.</span><span class="sxs-lookup"><span data-stu-id="ecf62-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="ecf62-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ecf62-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="ecf62-107">Преобразование: [Двойное](xref:microsoft.quantum.lang-ref.double) -> [Двойное](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ecf62-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ecf62-108">Функция, которая преобразует вариатес исходного распределения в преобразованное распределение.</span><span class="sxs-lookup"><span data-stu-id="ecf62-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="ecf62-109">распространение: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="ecf62-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="ecf62-110">Исходное распределение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="ecf62-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="ecf62-111">Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="ecf62-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="ecf62-112">Новое распределение, относящееся к `distribution` преобразованию, заданному параметром `transform` .</span><span class="sxs-lookup"><span data-stu-id="ecf62-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>

## <a name="example"></a><span data-ttu-id="ecf62-113">Пример</span><span class="sxs-lookup"><span data-stu-id="ecf62-113">Example</span></span>

<span data-ttu-id="ecf62-114">Следующие два распределения идентичны:</span><span class="sxs-lookup"><span data-stu-id="ecf62-114">The following two distributions are identical:</span></span>

```qsharp
let dist1 = ContinuousUniformDistribution(1.0, 2.0);
let dist2 = TransformedContinuousDistribution(
    PlusD(1.0, _),
    ContinuousUniformDistribution(0.0, 1.0)
);
```