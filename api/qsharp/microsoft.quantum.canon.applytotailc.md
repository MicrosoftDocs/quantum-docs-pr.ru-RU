---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Операция Апплитотаилк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 631e08666002d8077c6f8b78525b06b104dd4c7c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716966"
---
# <a name="applytotailc-operation"></a>Операция Апплитотаилк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет операцию к последнему элементу массива.

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl"></a>Op: 'T => [единицы](xref:microsoft.quantum.lang-ref.unit) CTL

Операция, которую необходимо применить.


### <a name="targets--t"></a>targets: 'T []

Массив целевых объектов, к которым будет применен последний объект `op` .



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Тип входных данных операции, которая должна быть применена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитотаил](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [Microsoft. тактов. Canon. Апплитотаила](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [Microsoft. тактов. Canon. Апплитотаилка](xref:Microsoft.Quantum.Canon.ApplyToTailCA)