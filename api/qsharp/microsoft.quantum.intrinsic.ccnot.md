---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Операция ККНОТ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711534"
---
# <a name="ccnot-operation"></a>Операция ККНОТ

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакеты [](https://nuget.org/packages/)


Применяет шлюз удвоенной управляемости — не (ККНОТ) к трем Кубитс.

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="control1--qubit"></a>Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первый элемент управления кубит для шлюза ККНОТ.


### <a name="control2--qubit"></a>control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй элемент управления кубит для шлюза ККНОТ.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой кубит для шлюза ККНОТ.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Эквивалентно:

```qsharp
Controlled X([control1, control2], target);
```