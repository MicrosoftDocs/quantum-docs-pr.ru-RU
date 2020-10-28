---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Функция Категорикалдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 756e9e95cac5554ab8f885dab7c47ac1b174c0f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732544"
---
# <a name="categoricaldistribution-function"></a>Функция Категорикалдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


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