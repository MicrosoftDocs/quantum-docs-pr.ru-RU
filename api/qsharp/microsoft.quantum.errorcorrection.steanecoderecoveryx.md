---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Функция Стеанекодерековерикс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: c90eac291ebe718d10377399184ad705bb51673e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824704"
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

## <a name="remarks"></a>Remarks

Выбранный декодер использует свойство кода CSS ⟦ 7, 1, 3 ⟧ Стеане Code, т. е. оно корректирует X Errors и Z Errors отдельно. Свойство кода заключается в том, что положение X, соответственно, с коррекцией Z, которое должно применяться, — это 3-разрядная кодировка X, соответственно, Z синдром, когда считается целым числом.

## <a name="references"></a>Ссылки

- Г. Готтесман, «Стабилизер коды и исправление ошибок такта», «степень Ph.d. гипотеза», Калтеч, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Стеанекодерековерикс](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. тактов. Ерроркорректион. Стеанекодерековерифнс](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)