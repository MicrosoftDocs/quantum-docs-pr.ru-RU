---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Операция Апплитореста
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 99a18e835115491cc3451a4e3b44a6ff70e9dc6c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717078"
---
# <a name="applytoresta-operation"></a>Операция Апплитореста

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию ко всему элементу массива, кроме первого элемента.

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Rest(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit-adj"></a>Op: 'T [] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будут применяться все, кроме первого `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплиторест](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [Microsoft. тактов. Canon. Апплиторестк](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [Microsoft. тактов. Canon. Апплиторестка](xref:Microsoft.Quantum.Canon.ApplyToRestCA)