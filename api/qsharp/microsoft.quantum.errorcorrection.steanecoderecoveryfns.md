---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns
title: Функция Стеанекодерековерифнс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryFns
qsharp.summary: Decoder for combined X- and Z-parts of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 7395996e75c5a1c0c5d13f76d9ec76acae5683c7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200413"
---
# <a name="steanecoderecoveryfns-function"></a>Функция Стеанекодерековерифнс

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Декодер для Объединенных X-и Z-частей стабилизер группы ⟦ 7, 1, 3 ⟧ Стеане.

```qsharp
function SteaneCodeRecoveryFns () : (Microsoft.Quantum.ErrorCorrection.RecoveryFn, Microsoft.Quantum.ErrorCorrection.RecoveryFn)
```


## <a name="output--recoveryfnrecoveryfn"></a>Выходные данные: ([рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn),[рековерифн](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn))

Кортеж функций типа `RecoveryFn` , принимающий измерение синдром `Result[]` и возвращающий `Pauli[]` операции, которые исправляет обнаруженную ошибку.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. тактов. Ерроркорректион. Стеанекодерековериз](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryZ)