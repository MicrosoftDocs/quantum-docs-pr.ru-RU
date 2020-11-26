---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Операция Меасуревисскратч
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: c42316a811e0e4a81c7f244c093a2be88fe5c733
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227069"
---
# <a name="measurewithscratch-operation"></a>Операция Меасуревисскратч

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Измеряет заданный оператор Паули, используя явное значение "кубит" для выполнения измерения.

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a>Входные данные

### <a name="pauli--pauli"></a>Паули: [Паули](xref:microsoft.quantum.lang-ref.pauli)[]

Оператор Multi-кубит Паули, указанный в качестве массива операторов с одним кубит Паули.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистр кубит для измерения.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__

Результат измерения данного оператора Паули в `target` регистре.