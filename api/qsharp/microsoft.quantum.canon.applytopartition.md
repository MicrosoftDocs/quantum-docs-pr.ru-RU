---
uid: Microsoft.Quantum.Canon.ApplyToPartition
title: Операция Апплитопартитион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartition
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts.
ms.openlocfilehash: a0dc3453e7501816132569869e858418d5f3f4e5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850538"
---
# <a name="applytopartition-operation"></a>Операция Апплитопартитион

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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