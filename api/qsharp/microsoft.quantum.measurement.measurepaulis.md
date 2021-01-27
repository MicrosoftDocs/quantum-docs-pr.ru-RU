---
uid: Microsoft.Quantum.Measurement.MeasurePaulis
title: Операция Меасурепаулис
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasurePaulis
qsharp.summary: Given an array of multi-qubit Pauli operators, measures each using a specified measurement gadget, then returns the array of results.
ms.openlocfilehash: 1bc14ec8e7c608d1195a03a354c71e870594f86d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853768"
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