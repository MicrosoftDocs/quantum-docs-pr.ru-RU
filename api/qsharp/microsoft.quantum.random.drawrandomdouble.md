---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Операция Драврандомдаубле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: d62416f4a222716edb9393fe4f43731d0e8aa9d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192950"
---
# <a name="drawrandomdouble-operation"></a>Операция Драврандомдаубле

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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

## <a name="remarks"></a>Комментарии

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Континуаусуниформдистрибутион](xref:Microsoft.Quantum.ContinuousUniformDistribution)