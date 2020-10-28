---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Операция Итератесраугхкартесианповер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716027"
---
# <a name="iteratethroughcartesianpower-operation"></a>Операция Итератесраугхкартесианповер

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


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