---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Операция Апплиторестка
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 3123c7f7b5e5c7f5cb17a34eedc81b3912109883
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208165"
---
# <a name="applytorestca-operation"></a>Операция Апплиторестка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию ко всему элементу массива, кроме первого элемента.

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-adj--ctl"></a>Op: 'T [] =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будут применяться все, кроме первого `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплиторест](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [Microsoft. тактов. Canon. Апплитореста](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [Microsoft. тактов. Canon. Апплиторестк](xref:Microsoft.Quantum.Canon.ApplyToRestC)