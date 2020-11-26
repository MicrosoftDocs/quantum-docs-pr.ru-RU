---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Операция Меасурепаулис
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 4faaf78f24fa28ae5e4f701b80d9297c910b975e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194225"
---
# <a name="measurepaulis-operation"></a>Операция Меасурепаулис

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Учитывая массив операторов кубит Паули, измеряет каждый с помощью указанного мини-приложения измерения, а затем возвращает массив результатов.

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []

Массив кубит Паули операторов для измерения.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация для измерения заданных операторов.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Мини-приложение: ([Паули](xref:microsoft.quantum.lang-ref.pauli)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) __= <Result> Недопустимый__> 

Операция, которая выполняет измерение заданного кубит оператора.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__[]

Массив результатов, полученных из измерения каждого элемента `paulis` в `target` .