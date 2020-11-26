---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Операция Драврандоминт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192916"
---
# <a name="drawrandomint-operation"></a>Операция Драврандоминт

Пространство имен: [Microsoft. тактов. Random](xref:Microsoft.Quantum.Random)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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

## <a name="remarks"></a>Комментарии

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Дискретеуниформдистрибутион](xref:Microsoft.Quantum.DiscreteUniformDistribution)