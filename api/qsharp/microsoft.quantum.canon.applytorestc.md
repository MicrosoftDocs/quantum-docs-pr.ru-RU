---
uid: Microsoft.Quantum.Canon.ApplyToRestC
title: Операция Апплиторестк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestC
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 55e534b7b7673f300b607a8213418c45c8c7c92c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717092"
---
# <a name="applytorestc-operation"></a>Операция Апплиторестк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию ко всему элементу массива, кроме первого элемента.

```qsharp
operation ApplyToRestC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl"></a>Op: 'T [] => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL

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
- [Microsoft. тактов. Canon. Апплиторестка](xref:Microsoft.Quantum.Canon.ApplyToRestCA)