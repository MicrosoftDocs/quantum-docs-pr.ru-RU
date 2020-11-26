---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Операция Итератесраугхкартесианповер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 2883e7cb30633afe51d380befe806665207c5abd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206482"
---
# <a name="iteratethroughcartesianpower-operation"></a>Операция Итератесраугхкартесианповер

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к каждому индексу в блоке питания целого диапазона.

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Описание

Итеративно применяет операцию для каждого элемента декартовой мощности диапазона `0..(bound - 1)` .

## <a name="input"></a>Входные данные

### <a name="power--int"></a>степень: [int](xref:microsoft.quantum.lang-ref.int)

Постепенная декартка, на которую `0..(bound - 1)` должно быть вызвано значение диапазона.


### <a name="bound--int"></a>граница: [int](xref:microsoft.quantum.lang-ref.int)

Спецификация диапазона для итерации, заданная как длина диапазона.


### <a name="op--int--unit"></a>Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, вызываемая для каждого элемента заданной постепенной Декарт.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Итератесраугхкартесианпродукт](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)