---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Операция Ассертмеасуремент
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 09024cd8cd6e713360dcf7f42f55941590f35883
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92713032"
---
# <a name="assertmeasurement-operation"></a>Операция Ассертмеасуремент

Пространство имен: [Microsoft. тактов. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Пакеты [](https://nuget.org/packages/)


Утверждения, которые измеряют данный Кубитс в заданной Паули базисе, всегда будут иметь заданный результат.

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit
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