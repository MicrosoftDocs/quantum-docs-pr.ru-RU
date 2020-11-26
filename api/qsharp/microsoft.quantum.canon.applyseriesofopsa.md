---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Операция Апплисериесофопса
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: e5b3527507f79dcc77803ce01472856145df0e9f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217974"
---
# <a name="applyseriesofopsa-operation"></a>Операция Апплисериесофопса

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет список Ops и их целевых объектов последовательно в массиве. (Прилегающий)

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="listofops--t--unit--is-adj"></a>Листофопс: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является суммой []

Список операций, каждый из которых принимает массив «t» для применения. Они применяются последовательно, сначала по нижнему индексу.
Каждый должен иметь смежный функтор


### <a name="targets--int"></a>целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []

Вложенные массивы, описывающие целевые объекты Op. Каждый массив должен содержать список ints, описывающих индексы для использования.


### <a name="register--t"></a>Register: не []

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплйопрепеатедлйовер](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)