---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Функция Дискретеуниформдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: f909e7def5439ec0feef4ca4dc0cf8ed12374dfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853718"
---
# <a name="discreteuniformdistribution-function"></a>Функция Дискретеуниформдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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

## <a name="example"></a>Пример

Следующий фрагмент Q # случайным образом выполняет откат шести костей:

```qsharp
let dieDistribution = DiscreteUniformDistribution(1, 6);
let dieRoll = dieDistribution::Sample();
```

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Драврандомдаубле](xref:Microsoft.Quantum.DrawRandomDouble)