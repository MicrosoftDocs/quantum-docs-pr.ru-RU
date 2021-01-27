---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Операция Апплитохеадк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3a65ad52e0b2f8b3a921fc549c35311f24d0e189
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850630"
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