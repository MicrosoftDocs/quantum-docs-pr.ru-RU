---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Функция Категорикалдистрибутион
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210256"
---
# <a name="categoricaldistribution-function"></a>Функция Категорикалдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает дискретное распределение по категориям, в котором явно задана вероятность для каждого конечного списка заданных результатов.

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Входные данные

### <a name="probs--double"></a>пробс: [Double](xref:microsoft.quantum.lang-ref.double)[]

Вероятности для каждого результата из распределения по категориям.
Эти вероятности не могут быть нормализованы, но должны быть не отрицательными.



## <a name="output--discretedistribution"></a>Выходные данные: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Индекс `i` с вероятностью `probs[i] / sum` , где `sum` — Сумма, `probs` заданная параметром `Fold(PlusD, 0.0, probs)` .