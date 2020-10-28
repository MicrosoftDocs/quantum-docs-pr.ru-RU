---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Операция Драврандомдаубле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 6c0558ded2bd018afad84c42c2d15fc029ac0d44
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733209"
---
# <a name="drawrandomdouble-operation"></a>Операция Драврандомдаубле

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


Рисует случайное вещественное число в заданном инклюзивном интервале.

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a>Входные данные

### <a name="min--double"></a>min: [Double](xref:microsoft.quantum.lang-ref.double)

Наименьшее вещественное число для рисования.


### <a name="max--double"></a>Max: [Double](xref:microsoft.quantum.lang-ref.double)

Максимальное вещественное число для рисования.



## <a name="output--double"></a>Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)

Случайное вещественное число в инклюзивном интервале от `min` до `max` с равномерным вероятностью.

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Континуаусуниформдистрибутион](xref:Microsoft.Quantum.ContinuousUniformDistribution)