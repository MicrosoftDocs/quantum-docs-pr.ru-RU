---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Операция Енкодеинтостеанекоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 2f65423a17dafadd1f9f10a07335150dfc8bf886
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826209"
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