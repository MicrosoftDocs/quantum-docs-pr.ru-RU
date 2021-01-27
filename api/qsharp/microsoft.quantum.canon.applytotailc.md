---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Операция Апплитотаилк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 8408dff24c5c57efbedb649ac182fac49e836a3e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850419"
---
# <a name="applytotailc-operation"></a>Операция Апплитотаилк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет операцию к последнему элементу массива.

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a>Описание

При наличии операции `op` и массива целевых объектов `targets` применяется `op(Tail(targets))` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-ctl"></a>Op: не>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — CTL

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