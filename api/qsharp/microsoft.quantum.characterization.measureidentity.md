---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Операция Меасуреидентити
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: f8cf5975ac9407e8c532ace08455a41d3c08d6f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851810"
---
# <a name="measureidentity-operation"></a>Операция Меасуреидентити

Пространство имен: [Microsoft. тактов. charactering](xref:Microsoft.Quantum.Characterization)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Измеряет оператор Identity в регистре Кубитс.

```qsharp
operation MeasureIdentity (register : Qubit[]) : Result
```


## <a name="input"></a>Входные данные

### <a name="register--qubit"></a>Register: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр для измерения.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

Результирующее значение `Zero` .

## <a name="remarks"></a>Remarks

Поскольку $ \болдоне $ имеет только еиженвалуе $1 $ и не имеет отрицательного еиженвалуе, эта операция всегда возвращает значение `Zero` , соответствующее еиженвалуе $ + 1 = (-1) ^ 0 $, и не приводит к свертыванию состояния `register` .

Сам по себе эта операция нецелесообразна, но она полезна в контексте процесса томографи, так как она предоставляет сведения о сохранении трассировки процесса обработки такта.
В частности, целевой компьютер с измерением потери данных должен заменить эту операцию фактическим измерением $ \болдоне $.