---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Определяемый пользователем тип Синдромемеасоп
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 36336f9e47e5f360cf5e19ffb6e15b4af88b2580
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850057"
---
# <a name="syndromemeasop-user-defined-type"></a>Определяемый пользователем тип Синдромемеасоп

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет операцию, используемую для измерения синдром блока кода исправления ошибок.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="example"></a>Пример

Мера синдромес для кода побитового отражения $S = \лангле ЗЗИ, ИЗЗ \рангле $ с помощью вспомогательного Кубитс, не являющегося отказоустойчивым способом:

```qsharp
    let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
            [PauliZ, PauliZ, PauliI],
            [PauliI, PauliZ, PauliZ]
        ], _, MeasureWithScratch));
```

## <a name="remarks"></a>Remarks

Подпись `(LogicalRegister => Syndrome)` представляет операцию, которая взаимодействует с Кубитс в `LogicalRegister` и некоторыми дополнительными Кубитс, за которыми следуют измерения вспомогательного Кубитс для извлечения `Syndrome` значения, представляющего `Result[]` эти измерения.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. тактов. Ерроркорректион. синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)