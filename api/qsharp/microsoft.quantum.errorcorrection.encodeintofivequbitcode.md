---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Операция Енкодеинтофивекубиткоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 1bccf46453ad34199dcebc5bcff693359fe2254c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826322"
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