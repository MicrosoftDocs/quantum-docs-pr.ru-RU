---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Операция Апплисериесофопска
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9dd1343b3ebcc75592441f150eee822cfe83f9a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217889"
---
# <a name="applyseriesofopsca-operation"></a>Операция Апплисериесофопска

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет список Ops и их целевых объектов последовательно в массиве. (Смежное + управление)

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="listofops--t--unit--is-adj--ctl"></a>Листофопс: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL []"

Список операций, каждый из которых принимает массив «t» для применения. Они применяются последовательно, сначала по нижнему индексу.
Каждый из них должен иметь одновременно соседний и контролируемый функтор.


### <a name="targets--int"></a>целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []

Вложенные массивы, описывающие целевые объекты Op. Каждый массив должен содержать список ints, описывающих индексы для использования.


### <a name="register--t"></a>Register: не []

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплйопрепеатедлйовер](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)