---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Функция Фикседпоинтрефлектионфасес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191454"
---
# <a name="fixedpointreflectionphases-function"></a>Функция Фикседпоинтрефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вычисление этапов частичного отражения для усиления амплитуды с фиксированной точкой.

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Входные данные

### <a name="nqueries--int"></a>Нкуериес: [int](xref:microsoft.quantum.lang-ref.int)

Число запросов к состоянию Oracle для подготовки. Должно быть нечетным целым числом.


### <a name="successmin--double"></a>Сукцессмин: [Double](xref:microsoft.quantum.lang-ref.double)

Минимальная вероятность успеха для целевого объекта.



## <a name="output--reflectionphases"></a>Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Массив фаз, который может использоваться в реализации алгоритма для усиления амплитуды с фиксированной точкой.

## <a name="references"></a>Ссылки

Мы используем этапы в «усилении амплитуды с фиксированной точкой с оптимальным количеством запросов».

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) См. также «методология составного тактового шлюза»
- [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) для этапов в `RotationPhases` формате.