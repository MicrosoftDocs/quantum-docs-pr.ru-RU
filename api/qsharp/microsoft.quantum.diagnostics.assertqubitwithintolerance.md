---
uid: Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance
title: Операция Ассерткубитвисинтолеранце
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertQubitWithinTolerance
qsharp.summary: Asserts that the qubit `q` is in the expected eigenstate of the Pauli Z operator up to a given tolerance.
ms.openlocfilehash: 3fe4aa739c5e15199401aecb76ef551e52f6dcff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712878"
---
# <a name="assertqubitwithintolerance-operation"></a>Операция Ассерткубитвисинтолеранце

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Утверждает, что кубит `q` находится в ожидаемом еиженстате оператора Паули Z вплоть до заданного допуска.

```qsharp
operation AssertQubitWithinTolerance (expected : Result, q : Qubit, tolerance : Double) : Unit
```


## <a name="input"></a>Входные данные

### <a name="expected--__invalidresult__"></a>ожидалось __: <Result> недопустимо__

Состояние, в котором ожидается кубит: `Zero` или `One` .


### <a name="q--qubit"></a>вопрос. [кубит](xref:microsoft.quantum.lang-ref.qubit)

Кубит, состояние которого утверждено.


### <a name="tolerance--double"></a>Допуск: [Double](xref:microsoft.quantum.lang-ref.double)

Допуск на вероятность измерения кубит, возвращающего ожидаемый результат.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

<xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> позволяет утверждать произвольные состояния кубит, а не только $Z $ еиженстатес.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. Ассерткубитисинстатевисинтолеранце](xref:Microsoft.Quantum.Diagnostics.AssertQubitIsInStateWithinTolerance)