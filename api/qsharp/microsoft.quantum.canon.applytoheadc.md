---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Операция Апплитохеадк
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 2b7321a6c385e2d98a0e91a8f58091ea8dc43ff4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208607"
---
# <a name="applytoheadc-operation"></a>Операция Апплитохеадк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к первому элементу массива.

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Head(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-ctl"></a>Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будет применен первый из них `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитохеад](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [Microsoft. тактов. Canon. Апплитохеада](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [Microsoft. тактов. Canon. Апплитохеадка](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)