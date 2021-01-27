---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Операция Ассертмеасуремент
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 8f5113f1d6b8e4f104af10ca330e244e95793418
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853502"
---
# <a name="assertmeasurement-operation"></a>Операция Ассертмеасуремент

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакет: [Microsoft. тактов. кшарп. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Утверждения, которые измеряют данный Кубитс в заданной Паули базисе, всегда будут иметь заданный результат.

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit is Adj + Ctl
```


## <a name="input"></a>Входные данные

### <a name="bases--pauli"></a>базовые базы: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Результат измерения для утверждения вероятности, выраженный как кубит оператор Паули.


### <a name="qubits--qubit"></a>Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр, для которого необходимо выполнить утверждение.


### <a name="result--__invalidresult__"></a>результат: __недопустимо <Result>__

Ожидаемый результат `Measure(bases, qubits)` .


### <a name="msg--string"></a>сообщение: [строка](xref:microsoft.quantum.lang-ref.string)

Сообщение, которое необходимо сообщить, если утверждение не выполняется.



## <a name="output--unit"></a>Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Remarks

Обратите внимание, что смежная и контролируемая версии этой операции не будут проверять условие.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Diagnostics. Ассертмеасурементпробабилити](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)