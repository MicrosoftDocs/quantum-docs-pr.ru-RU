---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Операция Меасурепаулис
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 7348ab3941af391c451d5c66f888cf3b6662cf20
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731000"
---
# <a name="measurepaulis-operation"></a>Операция Меасурепаулис

Пространство имен: [Microsoft. тактов. Измерение](xref:Microsoft.Quantum.Measurement)

Пакеты [](https://nuget.org/packages/)


Учитывая массив операторов кубит Паули, измеряет каждый с помощью указанного мини-приложения измерения, а затем возвращает массив результатов.

```qsharp
operation MeasurePaulis (paulis : Pauli[][], target : Qubit[], gadget : ((Pauli[], Qubit[]) => Result)) : Result[]
```


## <a name="input"></a>Входные данные

### <a name="paulis--pauli"></a>Пол: [Паули](xref:microsoft.quantum.lang-ref.pauli)[] []

Массив кубит Паули операторов для измерения.


### <a name="target--qubit"></a>Целевой объект: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]

Регистрация для измерения заданных операторов.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Мини-приложение: ( [Паули](xref:microsoft.quantum.lang-ref.pauli)[], [кубит](xref:microsoft.quantum.lang-ref.qubit)[]) __= <Result> Недопустимый__ > 

Операция, которая выполняет измерение заданного кубит оператора.



## <a name="output--__invalidresult__"></a>Выходные данные __: <Result> Недопустимый__ []

Массив результатов, полученных из измерения каждого элемента `paulis` в `target` .