---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Операция Ассертмеасурементпробабилити
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: ff0419706d825442492f82e564f1cce86f1b112f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92712976"
---
# <a name="assertmeasurementprobability-operation"></a>Операция Ассертмеасурементпробабилити

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Утверждения, измеряющие заданный Кубитс в данной Паулиной базе, будут иметь заданный результат с заданной вероятностью в пределах некоторой допустимости.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit
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



## <a name="remarks"></a>Remarks

Обратите внимание, что смежная и контролируемая версии этой операции не будут проверять условие.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. Ассертмеасуремент](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)