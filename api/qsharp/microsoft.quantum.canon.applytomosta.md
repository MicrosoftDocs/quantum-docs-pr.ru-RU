---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Операция Апплитомоста
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 994cada2952809dc84a70b76dc4ede8286c89855
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717204"
---
# <a name="applytomosta-operation"></a>Операция Апплитомоста

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию ко всему элементу массива, кроме последнего.

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Most(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit-adj"></a>Op: 'T [] [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будут применены все, кроме последнего `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитомост](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [Microsoft. тактов. Canon. Апплитомостк](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [Microsoft. тактов. Canon. Апплитомостка](xref:Microsoft.Quantum.Canon.ApplyToMostCA)