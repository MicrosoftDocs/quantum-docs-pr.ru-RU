---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Функция Континуаусуниформдистрибутион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709433"
---
# <a name="continuousuniformdistribution-function"></a>Функция Континуаусуниформдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Драврандомдаубле](xref:Microsoft.Quantum.DrawRandomDouble)