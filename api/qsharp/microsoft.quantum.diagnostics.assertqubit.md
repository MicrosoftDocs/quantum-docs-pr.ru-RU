---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Операция Ассерткубит
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: 8fcdd8de9250348e1dd1173052b53be978f2a0c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853454"
---
# <a name="assertqubit-operation"></a>Операция Ассерткубит

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Утверждает, что кубит `q` находится в ожидаемом еиженстате оператора Паули Z.

```qsharp
operation AssertQubit (expected : Result, q : Qubit) : Unit
```


## <a name="input"></a>Входные данные

### <a name="expected--__invalidresult__"></a>ожидалось __: <Result> недопустимо__

Состояние, в котором ожидается кубит: `Zero` или `One` .


### <a name="q--qubit"></a>вопрос. [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, состояние которого утверждено.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> позволяет утверждать произвольные состояния кубит, а не только $Z $ еиженстатес.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. Ассерткубитисинстатевисинтолеранце](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)