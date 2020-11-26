---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Операция Дравкатегорикал
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a5826aa5f658fea766db0ca5ccbb9c0d7d056d4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193001"
---
# <a name="drawcategorical-operation"></a>Операция Дравкатегорикал

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Рисует случайную выборку из распределения по категориям, заданному списком пробаблитиес.

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a>Описание

Вероятность выбора определенного индекса пропорциональна значению элемента массива в этом индексе.
Элементы массива, равные нулю, игнорируются, и их индексы никогда не возвращаются. Если какой-либо элемент массива меньше нуля или если ни один элемент массива больше нуля, операция завершается ошибкой.

## <a name="input"></a>Входные данные

### <a name="probs--double"></a>пробс: [Double](xref:microsoft.quantum.lang-ref.double)[]

Массив чисел с плавающей запятой пропорционально вероятности выбора каждого индекса.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целое число $i $ с вероятностью $ \Пр (i) = p_i/\ sum_i p_i $, где $p _i $ — это $i $ TH элемент `probs` .

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Random. Категорикалдистрибутион](xref:Microsoft.Quantum.Random.CategoricalDistribution)