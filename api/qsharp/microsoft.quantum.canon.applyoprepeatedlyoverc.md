---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverC
title: Операция Апплйопрепеатедлйоверк
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverC
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: effd61e6c012dcf81a83383c3fd43cf745d18117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92717833"
---
# <a name="applyoprepeatedlyoverc-operation"></a>Операция Апплйопрепеатедлйоверк

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакеты [](https://nuget.org/packages/)


Применяет одну и ту же Op к кубит регистру несколько раз.

```qsharp
operation ApplyOpRepeatedlyOverC (op : (Qubit[] => Unit is Ctl), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit-ctl"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = Ctl [единицы](xref:microsoft.quantum.lang-ref.unit)>

Операция, которая должна быть применена несколько раз к регистру кубит


### <a name="targets--int"></a>целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []

Вложенные массивы, описывающие целевые объекты Op. Каждый массив должен содержать список ints, описывающих используемый Кубитс.


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплисериесофопс](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)