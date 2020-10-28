---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Функция выборки
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732320"
---
# <a name="sampled-function"></a>Функция выборки

Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Пакеты [](https://nuget.org/packages/)


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

