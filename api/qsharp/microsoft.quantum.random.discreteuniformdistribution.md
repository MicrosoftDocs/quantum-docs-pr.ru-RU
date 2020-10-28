---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Функция Дискретеуниформдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730968"
---
# <a name="discreteuniformdistribution-function"></a>Функция Дискретеуниформдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


Возвращает равномерное распределение по заданному инклюзивному диапазону.

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Входные данные

### <a name="min--int"></a>min: [int](xref:microsoft.quantum.lang-ref.int)

Наименьшее целое число для рисования.


### <a name="max--int"></a>Max: [int](xref:microsoft.quantum.lang-ref.int)

Максимальное отображаемое целое число.



## <a name="output--discretedistribution"></a>Выходные данные: [дискретедистрибутион](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Распределение, случайные вариатес которых являются целыми числами в диапазоне от `min` до `max` с равномерным значением вероятности.

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Драврандомдаубле](xref:Microsoft.Quantum.DrawRandomDouble)