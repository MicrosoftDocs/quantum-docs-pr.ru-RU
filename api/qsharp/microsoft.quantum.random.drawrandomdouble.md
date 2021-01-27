---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Операция Драврандомдаубле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 792e9c714b761b48618aec2091e167a359c2b522
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847621"
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

## <a name="example"></a>Пример

Следующий фрагмент Q # случайным образом рисует угол между $0 $ и $2 \пи $:

```qsharp
let angle = DrawRandomDouble(0.0, 2.0 * PI());
```

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Континуаусуниформдистрибутион](xref:Microsoft.Quantum.ContinuousUniformDistribution)