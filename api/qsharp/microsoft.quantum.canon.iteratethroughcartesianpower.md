---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Операция Итератесраугхкартесианповер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840302"
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



## <a name="example"></a>Пример

При наличии операции `op` следующие два фрагмента эквивалентны:

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Итератесраугхкартесианпродукт](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)