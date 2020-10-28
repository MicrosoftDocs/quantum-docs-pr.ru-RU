---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Операция Драврандоминт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733593"
---
# <a name="drawrandomint-operation"></a>Операция Драврандоминт

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакеты [](https://nuget.org/packages/)


Рисует случайное целое число в заданном инклюзивном диапазоне.

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a>Входные данные

### <a name="min--int"></a>min: [int](xref:microsoft.quantum.lang-ref.int)

Наименьшее целое число для рисования.


### <a name="max--int"></a>Max: [int](xref:microsoft.quantum.lang-ref.int)

Максимальное отображаемое целое число.



## <a name="output--int"></a>Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)

Целое число в инклюзивном диапазоне от `min` до `max` с равномерным значением вероятности.

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Дискретеуниформдистрибутион](xref:Microsoft.Quantum.DiscreteUniformDistribution)