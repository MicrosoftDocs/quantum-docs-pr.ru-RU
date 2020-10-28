---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: Операция Апплитопартитион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: c1f43e7936fc1c18fb665388e9892dc3b74cdd05
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717147"
---
# <a name="applytopartition-operation"></a>Операция Апплитопартитион

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет пару операций к заданному разделу регистра на две части.

```qsharp
operation ApplyToPartition (op : ((Qubit[], Qubit[]) => Unit), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [единица](xref:microsoft.quantum.lang-ref.unit)> 

Пара операций, применяемых к заданному разделу.


### <a name="numberofqubitstofirstargument--int"></a>Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс от целевого объекта, помещаемых в первую часть секции.
Остальные Кубитс составляют вторую часть секции.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр Кубитс, которые секционированы и управляются данной двумя операциями.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитопартитиона](xref:Microsoft.Quantum.Canon.ApplyToPartitionA)
- [Microsoft. тактов. Canon. Апплитопартитионк](xref:Microsoft.Quantum.Canon.ApplyToPartitionC)
- [Microsoft. тактов. Canon. Апплитопартитионка](xref:Microsoft.Quantum.Canon.ApplyToPartitionCA)