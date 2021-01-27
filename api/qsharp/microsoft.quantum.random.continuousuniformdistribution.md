---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Функция Континуаусуниформдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: c81eb433f50277c677756ee70d916f4856260c6d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842322"
---
# <a name="continuousuniformdistribution-function"></a>Функция Континуаусуниформдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает равномерное распределение по заданному инклюзивному интервалу.

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Входные данные

### <a name="min--double"></a>min: [Double](xref:microsoft.quantum.lang-ref.double)

Наименьшее вещественное число для рисования.


### <a name="max--double"></a>Max: [Double](xref:microsoft.quantum.lang-ref.double)

Максимальное вещественное число для рисования.



## <a name="output--continuousdistribution"></a>Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Распределение, случайные вариатес которых являются реальными числами в инклюзивном интервале от `min` до `max` с равномерным значением вероятности.

## <a name="example"></a>Пример

Следующий фрагмент Q # случайным образом рисует угол между $0 $ и $2 \пи $:

```qsharp
let angleDistribution = ContinuousUniformDistribution(0.0, 2.0 * PI());
let angle = angleDistribution::Sample();
```

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Драврандомдаубле](xref:Microsoft.Quantum.DrawRandomDouble)