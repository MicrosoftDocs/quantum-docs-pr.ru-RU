---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Функция выборки
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: ddff72bbed6f20e8e0ceb3bfe3fc50a3da0bd2a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211633"
---
# <a name="sampled-function"></a>Функция выборки

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Производит выборку заданного массива с использованием заданного расписания.

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a>Входные данные

### <a name="schedule--samplingschedule"></a>Расписание: [самплингсчедуле](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Расписание, используемое в значениях выборки.


### <a name="values--t"></a>значения: 'T []

Массив значений для выборки.



## <a name="output--t"></a>Выходные данные: 'T []

Массив элементов из значений, следующих за заданным расписанием.

## <a name="type-parameters"></a>Параметры типа

### <a name="t"></a>Е

