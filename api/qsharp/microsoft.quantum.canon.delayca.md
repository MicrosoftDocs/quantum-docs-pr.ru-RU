---
uid: Microsoft.Quantum.Canon.DelayCA
title: Операция Делайка
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4b4be55436d6619511a12c6fb7fbd0f23989152a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92716266"
---
# <a name="delayca-operation"></a>Операция Делайка

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет заданную операцию с задержкой.

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a>Описание

При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.
В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.
Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit-ctl--adj"></a>Op: t => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + прилагательные

Операция, которую необходимо применить.


### <a name="arg--t"></a>ARG: 'T

Входные данные, к которым применяется операция.


### <a name="aux--unit"></a>AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)

Аргумент, используемый для задержки применения операции с помощью частичного приложения.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Входной тип операции, которая должна быть отложена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)
- [Microsoft. тактов. Canon. DELAYED](xref:Microsoft.Quantum.Canon.Delayed)