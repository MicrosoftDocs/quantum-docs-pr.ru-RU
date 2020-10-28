---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Операция восстановления
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: a659399f51794a4edc1d2ff43da84e46797103fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712206"
---
# <a name="recover-operation"></a>Операция восстановления

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


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