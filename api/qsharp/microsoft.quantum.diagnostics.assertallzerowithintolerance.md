---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Операция Ассерталлзеровисинтолеранце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 5e401904086323fabef7914d34463f50e4c38862
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713045"
---
# <a name="assertallzerowithintolerance-operation"></a>Операция Ассерталлзеровисинтолеранце

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Утверждение о том, что все заданные Кубитс находятся в состоянии $ \кет {0} $ вплоть до заданного допуска.

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit
```


## <a name="input"></a>Входные данные

### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Кубитс, которые подтверждаются в $ \кет {0} $ State.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Точность, с которой состояние должно находиться в $ \кет {0} $ State



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. Ассерткубитвисинтолеранце](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)