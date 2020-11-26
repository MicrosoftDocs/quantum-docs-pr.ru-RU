---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Операция Енкодеинтофивекубиткоде
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 70e52b7440dca1fa8761db13d6187cb6bf8c43c4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200991"
---
# <a name="encodeintofivequbitcode-operation"></a>Операция Енкодеинтофивекубиткоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Кодирует в код такта ⟦ 5, 1, 3 ⟧.

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Входные данные

### <a name="physregister--qubit"></a>Фисрегистер: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубит, представляющий незакодированное состояние. Длина этого массива равна `Qubit[]` 1.


### <a name="auxqubits--qubit"></a>Аукскубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр вспомогательных Кубитс, которые будут использоваться для представления закодированного состояния.



## <a name="output--logicalregister"></a>Выходные данные: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Массив физического Кубитс типа `LogicalRegister` , который хранит закодированное состояние.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)