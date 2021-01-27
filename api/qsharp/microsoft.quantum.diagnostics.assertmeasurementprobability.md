---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Операция Ассертмеасурементпробабилити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830823"
---
# <a name="assertmeasurementprobability-operation"></a>Операция Ассертмеасурементпробабилити

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Утверждения, измеряющие заданный Кубитс в данной Паулиной базе, будут иметь заданный результат с заданной вероятностью в пределах некоторой допустимости.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="bases--pauli"></a>базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Результат измерения для утверждения вероятности, выраженный как кубит оператор Паули.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр, для которого необходимо выполнить утверждение.


### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Ожидаемый результат `Measure(bases, qubits)` .


### <a name="prob--double"></a>prob: [Double](xref:microsoft.quantum.lang-ref.double)

Вероятность, с которой ожидается данный результат.


### <a name="msg--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Сообщение, которое необходимо сообщить, если утверждение не выполняется.


### <a name="tol--double"></a>принудительно применяли стойкое: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Пример

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a>Remarks

Обратите внимание, что смежная и контролируемая версии этой операции не будут проверять условие.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. Ассертмеасуремент](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)