---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Функция выборки
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 5dd599246847718f4f0411715585cb416595db9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854947"
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

