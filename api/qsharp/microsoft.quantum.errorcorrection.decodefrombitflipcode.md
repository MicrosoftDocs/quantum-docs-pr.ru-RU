---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Операция Декодефромбитфлипкоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: be6ad5fce9eeb3eea031ff301b78dbb3680b66f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712485"
---
# <a name="decodefrombitflipcode-operation"></a>Операция Декодефромбитфлипкоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Декодирования из кода [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-переворот Code.

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Входные данные

### <a name="logicalregister--logicalregister"></a>Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Блок кода побитового отражения.



## <a name="output--qubitqubit"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[])

Кортеж данных, закодированных в логическую регистрацию, и вспомогательный Кубитс, используемый для представления синдром.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. тактов. Ерроркорректион. Енкодеинтобитфлипкоде](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)