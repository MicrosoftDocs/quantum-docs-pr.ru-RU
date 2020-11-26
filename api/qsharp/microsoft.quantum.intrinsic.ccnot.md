---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Операция ККНОТ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: 715796ddd915d80036933e3f1ceefa97aa62cecf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212483"
---
# <a name="ccnot-operation"></a>Операция ККНОТ

Пространство имен: [Microsoft. такт. внутренний](xref:Microsoft.Quantum.Intrinsic)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Применяет шлюз удвоенной управляемости — не (ККНОТ) к трем Кубитс.

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="control1--qubit"></a>Control1: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Первый элемент управления кубит для шлюза ККНОТ.


### <a name="control2--qubit"></a>control2: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Второй элемент управления кубит для шлюза ККНОТ.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)

Целевой кубит для шлюза ККНОТ.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Комментарии

Эквивалентно:

```qsharp
Controlled X([control1, control2], target);
```