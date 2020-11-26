---
uid: Microsoft.Quantum.Characterization.MeasureIdentity
title: Операция Меасуреидентити
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: MeasureIdentity
qsharp.summary: Measures the identity operator on a register of qubits.
ms.openlocfilehash: 4a169355d0669c67f0eb14c80e8554b2f24b035a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216121"
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

## <a name="remarks"></a>Комментарии

Поскольку $ \болдоне $ имеет только еиженвалуе $1 $ и не имеет отрицательного еиженвалуе, эта операция всегда возвращает значение `Zero` , соответствующее еиженвалуе $ + 1 = (-1) ^ 0 $, и не приводит к свертыванию состояния `register` .

Сам по себе эта операция нецелесообразна, но она полезна в контексте процесса томографи, так как она предоставляет сведения о сохранении трассировки процесса обработки такта.
В частности, целевой компьютер с измерением потери данных должен заменить эту операцию фактическим измерением $ \болдоне $.