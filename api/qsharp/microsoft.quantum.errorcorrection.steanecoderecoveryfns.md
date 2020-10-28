---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Функция Стеанекодерековерифнс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: b1dd1c2e9a71e58bd8a86d1759a8b6af13a49614
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712136"
---
# <a name="steanecoderecoveryfns-function"></a>Функция Стеанекодерековерифнс

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Декодер для Объединенных X-и Z-частей стабилизер группы ⟦ 7, 1, 3 ⟧ Стеане.

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a>Выходные данные: ([рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))

Кортеж функций типа `RecoveryFn` , принимающий измерение синдром `Result[]` и возвращающий `Pauli[]` операции, которые исправляет обнаруженную ошибку.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. тактов. Ерроркорректион. Стеанекодерековериз](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)