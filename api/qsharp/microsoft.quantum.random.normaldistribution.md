---
uid: Microsoft.Quantum.Random.NormalDistribution
title: Функция Нормалдистрибутион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814188"
---
# <a name="normaldistribution-function"></a>Функция Нормалдистрибутион

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Возвращает нормальное распределение с заданным средним и дисперсией.

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Входные данные

### <a name="mean--double"></a>среднее значение: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="variance--double"></a>дисперсия: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--continuousdistribution"></a>Выходные данные: [континуаусдистрибутион](xref:Microsoft.Quantum.Random.ContinuousDistribution)



## <a name="example"></a>Пример

В следующем примере выводятся 10 примеров из нормального распределения с средним значением 2 и стандартным отклонением 0,1:

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Random. Стандарднормалдистрибутион](xref:Microsoft.Quantum.Random.StandardNormalDistribution)