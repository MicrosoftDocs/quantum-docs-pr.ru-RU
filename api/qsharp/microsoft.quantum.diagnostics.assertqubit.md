---
uid: Microsoft.Quantum.Diagnostics.AssertQubit
title: Операция Ассерткубит
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubit
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator.
ms.openlocfilehash: fa1f52da5a011cd914a0fda69b78cf5a4fd71e16
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712947"
---
# <a name="assertqubit-operation"></a>Операция Ассерткубит

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


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