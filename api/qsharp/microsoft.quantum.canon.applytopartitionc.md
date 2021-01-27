---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Операция Апплитопартитионк
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 43cf43fa2bf9c00a4096b39555b8f6080dd506d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850524"
---
# <a name="applytopartitionc-operation"></a>Операция Апплитопартитионк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет пару операций к заданному разделу регистра на две части.
Модификатор `C` указывает, что операция является управляемой.

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Входные данные

### <a name="op--qubitqubit--unit--is-ctl"></a>Op: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) = [единица](xref:microsoft.quantum.lang-ref.unit) > является CTL

Пара операций, применяемых к заданному разделу.


### <a name="numberofqubitstofirstargument--int"></a>Нумберофкубитстофирстаргумент: [int](xref:microsoft.quantum.lang-ref.int)

Число Кубитс от целевого объекта, помещаемых в первую часть секции.
Остальные Кубитс составляют вторую часть секции.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр Кубитс, которые секционированы и управляются данной двумя операциями.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплитопартитион](xref:Microsoft.Quantum.Canon.ApplyToPartition)