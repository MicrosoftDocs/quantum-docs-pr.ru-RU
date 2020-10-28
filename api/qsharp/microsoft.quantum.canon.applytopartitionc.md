---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Операция Апплитопартитионк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 840c93c653d71af1a82fb0dc51d9e056176ba88b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717119"
---
# <a name="applytopartitionc-operation"></a>Операция Апплитопартитионк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет пару операций к заданному разделу регистра на две части.
Модификатор `C` указывает, что операция является управляемой.

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit-ctl"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = CTL [единицы](xref:microsoft.quantum.lang-ref.unit)>

Пара операций, применяемых к заданному разделу.


### <a name="numberofqubitstofirstargument--int"></a>Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс от целевого объекта, помещаемых в первую часть секции.
Остальные Кубитс составляют вторую часть секции.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр Кубитс, которые секционированы и управляются данной двумя операциями.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитопартитион](xref:Microsoft.Quantum.Canon.ApplyToPartition)