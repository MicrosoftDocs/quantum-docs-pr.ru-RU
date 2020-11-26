---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Определяемый пользователем тип Синдромемеасоп
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 65e47d82546b1df0beec2c00f435d3e7a28e6ae6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200260"
---
# <a name="syndromemeasop-user-defined-type"></a>Определяемый пользователем тип Синдромемеасоп

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет операцию, используемую для измерения синдром блока кода исправления ошибок.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>Комментарии

Подпись `(LogicalRegister => Syndrome)` представляет операцию, которая взаимодействует с Кубитс в `LogicalRegister` и некоторыми дополнительными Кубитс, за которыми следуют измерения вспомогательного Кубитс для извлечения `Syndrome` значения, представляющего `Result[]` эти измерения.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. тактов. Ерроркорректион. синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)