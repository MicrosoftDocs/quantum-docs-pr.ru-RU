---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Операция Декодефромфивекубиткоде
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 9b4580cb88f03a16e3c9c55511d0ec5968cc636f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853157"
---
# <a name="decodefromfivequbitcode-operation"></a>Операция Декодефромфивекубиткоде

Пространство имен: [Microsoft. тактов. ерроркорректион](xref:Microsoft.Quantum.ErrorCorrection)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Декодирует код такта ⟦ 5, 1, 3 ⟧.

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Входные данные

### <a name="logicalregister--logicalregister"></a>Логикалрегистер: [логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Массив Кубитс, представляющий закодированное 5-кубит логическое состояние кода.



## <a name="output--qubitqubit"></a>Выходные данные: ([кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[])

Массив кубит с длиной 1, представляющий незакодированное состояние в первом параметре вместе с вспомогательным Кубитс во втором параметре.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Ерроркорректион. Фивекубиткодинкодер](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [Microsoft. тактов. Ерроркорректион. Логикалрегистер](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)