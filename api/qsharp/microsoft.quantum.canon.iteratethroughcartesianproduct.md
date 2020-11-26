---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Операция Итератесраугхкартесианпродукт
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: 6340c7a972253e6f583a3856df93a7066ced3139
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206448"
---
# <a name="iteratethroughcartesianproduct-operation"></a>Операция Итератесраугхкартесианпродукт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию для каждого индекса в декартово произведение нескольких диапазонов.

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Описание

Итеративно применяет операцию для каждого элемента декартово произведения `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,..., `0..(bounds[Length(bounds) - 1] - 1)`

## <a name="input"></a>Входные данные

### <a name="bounds--int"></a>границы: [int](xref:microsoft.quantum.lang-ref.int)[]

Массив, указывающий диапазоны для итерации, при этом каждый диапазон задается как целочисленная длина.


### <a name="op--int--unit"></a>Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Операция, вызываемая для каждого элемента данного декартово произведение.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Итератесраугхкартесианповер](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)