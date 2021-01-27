---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Операция Драврандоминт
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851136"
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

## <a name="example"></a>Пример

Следующий фрагмент Q # случайным образом выполняет откат шести костей:

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a>Remarks

Завершается ошибкой `max <= min` , если.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Дискретеуниформдистрибутион](xref:Microsoft.Quantum.DiscreteUniformDistribution)