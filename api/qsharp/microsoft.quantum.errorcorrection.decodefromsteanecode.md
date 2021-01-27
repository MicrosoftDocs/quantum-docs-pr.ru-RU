---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Операция Декодефромстеанекоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 54e47b65ed7a89c8ff9026126a9542d3d7ba15cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827389"
---
# <a name="decodefromsteanecode-operation"></a>Операция Декодефромстеанекоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Операция обратной кодировки, которая сопоставляет незакодированный регистр такта с закодированным регистром такта в коде такта ⟦ 7, 1, 3 ⟧ Стеане.

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Входные данные

### <a name="logicalregister--logicalregister"></a>Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Массив Кубитс, представляющий закодированное 5-кубит логическое состояние кода.



## <a name="output--qubitqubit"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[])

Массив кубит с длиной 1, представляющий незакодированное состояние в первом параметре вместе с вспомогательным Кубитс во втором параметре.

## <a name="remarks"></a>Remarks

Выбранный декодер использует свойство кода CSS ⟦ 7, 1, 3 ⟧ Стеане Code, т. е. оно корректирует X Errors и Z Errors отдельно. Свойство кода заключается в том, что положение X, соответственно, с коррекцией Z, которое должно применяться, — это 3-разрядная кодировка X, соответственно, Z синдром, когда считается целым числом.

## <a name="references"></a>Ссылки

- Г. Готтесман, «Стабилизер коды и исправление ошибок такта», «степень Ph.d. гипотеза», Калтеч, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Стеанекодинкодер](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [Microsoft. тактов. Ерроркорректион. Стеанекодедекодер](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)