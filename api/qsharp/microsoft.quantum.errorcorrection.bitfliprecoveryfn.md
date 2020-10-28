---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: Функция Битфлипрековерифн
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: dad90475b2506187282825e143b11adc5120f453
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712499"
---
# <a name="bitfliprecoveryfn-function"></a>Функция Битфлипрековерифн

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Функция для операций восстановления Паули для заданного измерения синдром путем уточняющего запроса таблицы для ⟦ 3, 1, 1 ⟧ разрядного кода отражения.

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Функция типа `RecoveryFn` , которая принимает синдром измерение `Result[]` и возвращает `Pauli[]` операции, которые исправляет обнаруженную ошибку.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)