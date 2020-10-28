---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Операция Енкодеинтобитфлипкоде
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 694d3f7a412b64b0ad533b4478a9274384d05c61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712402"
---
# <a name="encodeintobitflipcode-operation"></a>Операция Енкодеинтобитфлипкоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакеты [](https://nuget.org/packages/)


Кодирует в код [3, 1, 3]/⟦ 3, 1, 1 ⟧ bit-переворот.

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Входные данные

### <a name="physregister--qubit"></a>Фисрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр физических Кубитс, представляющих защищаемые данные.


### <a name="auxqubits--qubit"></a>Аукскубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация вспомогательных Кубитс изначально в состоянии $ \кет {00} $, которая используется для кодирования защищаемых данных.



## <a name="output--logicalregister"></a>Выходные данные: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Физические и вспомогательные Кубитс, используемые в кодировке, представленные в виде логического регистра.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)