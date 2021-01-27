---
uid: Microsoft.Quantum.Diagnostics._iterateThroughCartesianPower
title: _iterateThroughCartesianPower операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _iterateThroughCartesianPower
qsharp.summary: Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product
ms.openlocfilehash: a27302be75ee701b0629310700b56d222aaef7db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853564"
---
# <a name="_iteratethroughcartesianpower-operation"></a>_iterateThroughCartesianPower операция

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Просматривает переменную через декартово произведение [0, Bounds [0]-1] × [0, Bounds [1]-1] × [0, Bounds [length (Bounds)-1]-1] и вызывает op (ARR) для каждого элемента декартово продукта.

```qsharp
operation _iterateThroughCartesianPower (length : Int, value : Int, op : (Int[] => Unit)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="length--int"></a>Длина: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="op--int--unit"></a>Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

