---
uid: Microsoft.Quantum.Canon.DelayA
title: Отложенная операция
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c7385cfcdf782347feb8d95311205a9311f4c929
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840667"
---
# <a name="delaya-operation"></a>Отложенная операция

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет заданную операцию с задержкой.

```qsharp
operation DelayA<'T> (op : ('T => Unit is Adj), arg : 'T, aux : Unit) : Unit is Adj
```


## <a name="description"></a>Описание

При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.
В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.
Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .

## <a name="input"></a>Входные данные

### <a name="op--t--unit--is-adj"></a>Op: t =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  является просуммой

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