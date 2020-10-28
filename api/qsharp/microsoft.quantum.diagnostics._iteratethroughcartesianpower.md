---
uid: Microsoft.Quantum.Diagnostics._iterateThroughCartesianPower
title: _iterateThroughCartesianPower операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _iterateThroughCartesianPower
qsharp.summary: Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product
ms.openlocfilehash: 36666238b40d036e3f6a8949b22f5806216d71f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713143"
---
# <a name="_iteratethroughcartesianpower-operation"></a>_iterateThroughCartesianPower операция

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Просматривает переменную через декартово произведение [0, Bounds [0]-1] × [0, Bounds [1]-1] × [0, Bounds [length (Bounds)-1]-1] и вызывает op (ARR) для каждого элемента декартово продукта.

```qsharp
operation _iterateThroughCartesianPower (length : Int, value : Int, op : (Int[] => Unit)) : Unit
```


## <a name="input"></a>Входные данные

### <a name="length--int"></a>Длина: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="value--int"></a>значение: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="op--int--unit"></a>Op: [int](xref:microsoft.quantum.lang-ref.int)[] = [единица](xref:microsoft.quantum.lang-ref.unit)> 





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)

