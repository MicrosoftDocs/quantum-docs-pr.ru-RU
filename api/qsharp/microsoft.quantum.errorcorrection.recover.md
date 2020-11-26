---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Операция восстановления
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: bdf09decc3705d3285f4eb605c176d7764a994d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200583"
---
# <a name="recover-operation"></a>Операция восстановления

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Выполняет единичное округление исправления ошибки с помощью кода такта, описанного `QECC` типом.

```qsharp
operation Recover (code : Microsoft.Quantum.ErrorCorrection.QECC, fn : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Входные данные

### <a name="code--qecc"></a>код: [кекк](xref:Microsoft.Quantum.ErrorCorrection.QECC)

Ошибка такта. Исправление кода, упакованного как `QECC` тип, описывает кодирование и декодирование данных тактов, а также способ измерения ошибки синдромес.


### <a name="fn--recoveryfn"></a>FN: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Объект `RecoveryFn` , сопоставляющий каждую ошибку, синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.


### <a name="logicalregister--logicalregister"></a>Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Массив Кубитс, в котором определен код стабилизер.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. КЕКК](xref:Microsoft.Quantum.ErrorCorrection.QECC)
- [Microsoft. тактов. Ерроркорректион. Рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)