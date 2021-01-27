---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Функция Категорикалдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 754ada71078bd5446f78885ace31d92dce6bf1a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842350"
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

## <a name="example"></a>Пример

В следующем коде Q # отображается 0 с вероятностью 30% и 1 с вероятностью 70%:

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```