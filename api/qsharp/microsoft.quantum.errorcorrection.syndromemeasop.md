---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Определяемый пользователем тип Синдромемеасоп
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 1314e16d26c7310bab21caa91cb398d4b6f09b29
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712121"
---
# <a name="syndromemeasop-user-defined-type"></a>Определяемый пользователем тип Синдромемеасоп

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Представляет операцию, используемую для измерения синдром блока кода исправления ошибок.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>Remarks

Подпись `(LogicalRegister => Syndrome)` представляет операцию, которая взаимодействует с Кубитс в `LogicalRegister` и некоторыми дополнительными Кубитс, за которыми следуют измерения вспомогательного Кубитс для извлечения `Syndrome` значения, представляющего `Result[]` эти измерения.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. тактов. Ерроркорректион. синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)