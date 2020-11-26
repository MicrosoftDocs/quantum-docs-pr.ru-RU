---
uid: Microsoft.Quantum.Canon.Delay
title: Операция задержки
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4f45527faa49f79fccff3892e928fed09f9f0bc8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216512"
---
# <a name="delay-operation"></a>Операция задержки

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет заданную операцию с задержкой.

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a>Описание

При наличии операции и входных данных для этой операции применяет операцию, когда предоставляется дополнительный ввод.
В частности, выражение `Delay(op, arg, _)` является операцией, которая применяется `op` к `arg` при вызове.
Выражение `Delay(op,arg,_)` позволяет отложить применение `op` .

## <a name="input"></a>Входные данные

### <a name="op--t--u"></a>Op: 'T => ' U 

Операция, которую необходимо применить.


### <a name="arg--t"></a>ARG: 'T

Входные данные, к которым применяется операция.


### <a name="aux--unit"></a>AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)

Аргумент, используемый для задержки применения операции с помощью частичного приложения.



## <a name="output--u"></a>Выходные данные: ' U



## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

Входной тип операции, которая должна быть отложена.
### <a name="u"></a>' U

Возвращаемый тип операции, которая должна быть отложена.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Делайк](xref:Microsoft.Quantum.Canon.DelayC)
- [Microsoft. тактов. Canon. Delay](xref:Microsoft.Quantum.Canon.DelayA)
- [Microsoft. тактов. Canon. Делайка](xref:Microsoft.Quantum.Canon.DelayCA)
- [Microsoft. тактов. Canon. DELAYED](xref:Microsoft.Quantum.Canon.Delayed)