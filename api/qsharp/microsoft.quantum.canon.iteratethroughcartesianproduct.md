---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Операция Итератесраугхкартесианпродукт
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: e4fc71f6f707639f6f89eece8546ec2fb434a15a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716041"
---
# <a name="iteratethroughcartesianproduct-operation"></a>Операция Итератесраугхкартесианпродукт

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


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