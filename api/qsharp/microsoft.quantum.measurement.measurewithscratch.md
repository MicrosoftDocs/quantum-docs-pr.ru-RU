---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Операция Меасуревисскратч
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 4173aa9daac08a3febdfcbf12dc236f797685436
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854665"
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