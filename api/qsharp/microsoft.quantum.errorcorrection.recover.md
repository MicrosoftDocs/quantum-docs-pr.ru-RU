---
uid: Microsoft.Quantum.ErrorCorrection.Recover
title: Операция восстановления
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: Recover
qsharp.summary: Performs a single round of error correction by a quantum code described by a `QECC` type.
ms.openlocfilehash: 3e2ce404ae3a6b4097897b859388fea3f915232c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98825519"
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