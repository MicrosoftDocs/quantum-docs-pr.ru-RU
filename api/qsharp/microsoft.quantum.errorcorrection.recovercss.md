---
uid: Microsoft.Quantum.ErrorCorrection.RecoverCSS
title: Операция Рековерксс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: RecoverCSS
qsharp.summary: Performs a single round of error correction by a quantum code described by a `CSS` type.
ms.openlocfilehash: 48d3cd3d5f6aea265fac2f50b913ab855a31accf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712205"
---
# <a name="recovercss-operation"></a>Операция Рековерксс

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Выполняет единичное округление исправления ошибки с помощью кода такта, описанного `CSS` типом.

```qsharp
operation RecoverCSS (code : Microsoft.Quantum.ErrorCorrection.CSS, fnX : Microsoft.Quantum.ErrorCorrection.RecoveryFn, fnZ : Microsoft.Quantum.ErrorCorrection.RecoveryFn, logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : Unit
```


## <a name="input"></a>Входные данные

### <a name="code--css"></a>код: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)

В такте ошибки CSS, упакованной в виде типа, `CSS` описывается кодирование и декодирование данных тактов, а также способ измерения ошибки синдромес.


### <a name="fnx--recoveryfn"></a>ФНКС: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Объект `RecoveryFn` , сопоставляющий каждый $X $ Error синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.


### <a name="fnz--recoveryfn"></a>Фнз: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Объект `RecoveryFn` , сопоставляющий каждый $Z $ Error синдром с `Pauli[]` операциями, которые исправлять обнаруженную ошибку.


### <a name="logicalregister--logicalregister"></a>Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Массив Кубитс, в котором определен код стабилизер.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)
- [Microsoft. тактов. Ерроркорректион. Рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)
- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)