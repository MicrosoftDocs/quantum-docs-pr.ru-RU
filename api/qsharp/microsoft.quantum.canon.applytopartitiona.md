---
uid: Microsoft.Quantum.Canon.ApplyToPartitionA
title: Операция Апплитопартитиона
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 6ff3bf8b5a4344ee5a7a054c6285a5492260068d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717133"
---
# <a name="applytopartitiona-operation"></a>Операция Апплитопартитиона

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет пару операций к заданному разделу регистра на две части.
Модификатор `A` указывает, что операция является аджоинтабле.

```qsharp
operation ApplyToPartitionA (op : ((Qubit[], Qubit[]) => Unit is Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit-adj"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) [=>ная](xref:microsoft.quantum.lang-ref.unit) прогода

Пара операций, применяемых к заданному разделу.


### <a name="numberofqubitstofirstargument--int"></a>Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс от целевого объекта, помещаемых в первую часть секции.
Остальные Кубитс составляют вторую часть секции.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр Кубитс, которые секционированы и управляются данной двумя операциями.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитопартитион](xref:Microsoft.Quantum.Canon.ApplyToPartition)