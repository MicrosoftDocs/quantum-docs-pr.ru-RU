---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverA
title: Операция Апплйопрепеатедлйовера
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 30e91d8a0292c7389ad83f14e1b7d4a8248cbb96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841623"
---
# <a name="applyoprepeatedlyovera-operation"></a>Операция Апплйопрепеатедлйовера

Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Применяет одну и ту же Op к кубит регистру несколько раз.

```qsharp
operation ApplyOpRepeatedlyOverA (op : (Qubit[] => Unit is Adj), targets : Int[][], register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Входные данные

### <a name="op--qubit--unit--is-adj"></a>Op: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit) >

Операция, которая должна быть применена несколько раз к регистру кубит


### <a name="targets--int"></a>целевые объекты: [int](xref:microsoft.quantum.lang-ref.int)[] []

Вложенные массивы, описывающие целевые объекты Op. Каждый массив должен содержать список ints, описывающих используемый Кубитс.


### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр кубит, по которому будет выполняться операция.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Canon. Апплисериесофопс](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)