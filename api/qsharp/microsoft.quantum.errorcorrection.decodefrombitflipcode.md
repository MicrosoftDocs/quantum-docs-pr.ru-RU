---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Операция Декодефромбитфлипкоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: b16e84340053b6c1eab7b91ed8db0461b9eac98e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827566"
---
# <a name="decodefrombitflipcode-operation"></a>Операция Декодефромбитфлипкоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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