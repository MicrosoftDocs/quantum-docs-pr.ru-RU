---
uid: Microsoft.Quantum.ErrorCorrection.BitFlipRecoveryFn
title: Функция Битфлипрековерифн
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: BitFlipRecoveryFn
qsharp.summary: Function for recovery Pauli operations for given syndrome measurement by table lookup for the ⟦3, 1, 1⟧ bit flip code.
ms.openlocfilehash: 1cf2bd944b4dcaadeeca96fa0f576250590962e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827594"
---
# <a name="bitfliprecoveryfn-function"></a>Функция Битфлипрековерифн

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Функция для операций восстановления Паули для заданного измерения синдром путем уточняющего запроса таблицы для ⟦ 3, 1, 1 ⟧ разрядного кода отражения.

```qsharp
function BitFlipRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Выходные данные: [рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Функция типа `RecoveryFn` , которая принимает синдром измерение `Result[]` и возвращает `Pauli[]` операции, которые исправляет обнаруженную ошибку.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)