---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Операция Апплиторестка
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: e64eeaae2151a28c289e3e71e47f897d6c378b36
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841246"
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