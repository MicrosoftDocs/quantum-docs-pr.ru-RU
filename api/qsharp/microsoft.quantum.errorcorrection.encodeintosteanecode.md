---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Операция Енкодеинтостеанекоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e74c7fdc5acbb1a8c417bad3eb3630314e3f71bc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201025"
---
# <a name="encodeintosteanecode-operation"></a>Операция Енкодеинтостеанекоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Операция кодирования, которая сопоставляет незакодированный регистр такта с закодированным регистром такта в коде такта ⟦ 7, 1, 3 ⟧ Стеане.

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Входные данные

### <a name="physregister--qubit"></a>Фисрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр кубит, который содержит незакодированное состояние такта


### <a name="auxqubits--qubit"></a>Аукскубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр кубит, который изначально равен нулю и добавляется в тактовую систему, чтобы можно было выполнить операцию кодирования.



## <a name="output--logicalregister"></a>Выходные данные: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Регистр такта, удерживающий состояние после применения кодировщика Стеане

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. тактов. Ерроркорректион. Стеанекодедекодер](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)