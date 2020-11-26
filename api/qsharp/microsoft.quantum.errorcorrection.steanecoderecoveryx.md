---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Функция Стеанекодерековерикс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 5fac832ef5b7d7be2d85675a32f45e66312f66c8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200376"
---
# <a name="steanecoderecoveryx-function"></a>Функция Стеанекодерековерикс

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Декодер для X-части группы стабилизер ⟦ 7, 1, 3 ⟧ Стеане.

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a>Входные данные

### <a name="syndrome--syndrome"></a>синдром: [синдром](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Массив синдром, полученный из измерения X-части стабилизер.



## <a name="output--pauli"></a>Выходные данные: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Массив операций Паули, которые при применении к закодированной тактовой системе исправляет ошибку, соответствующую `syndrome` .

## <a name="remarks"></a>Комментарии

Выбранный декодер использует свойство кода CSS ⟦ 7, 1, 3 ⟧ Стеане Code, т. е. оно корректирует X Errors и Z Errors отдельно. Свойство кода заключается в том, что положение X, соответственно, с коррекцией Z, которое должно применяться, — это 3-разрядная кодировка X, соответственно, Z синдром, когда считается целым числом.

## <a name="references"></a>Ссылки

- Г. Готтесман, «Стабилизер коды и исправление ошибок такта», «степень Ph.d. гипотеза», Калтеч, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. тактов. Ерроркорректион. Стеанекодерековерифнс](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)