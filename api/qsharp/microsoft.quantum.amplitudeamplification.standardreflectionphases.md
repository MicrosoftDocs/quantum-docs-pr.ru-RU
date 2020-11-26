---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Функция Стандардрефлектионфасес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 316c8f22a16859ebb439824eda9a5aa02c750b5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191131"
---
# <a name="standardreflectionphases-function"></a>Функция Стандардрефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Вычисление этапов частичного отражения для стандартного усиления амплитуды.

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Входные данные

### <a name="niterations--int"></a>Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)

Число итераций усиления амплитуды для создания фаз частичного отражения для.



## <a name="output--reflectionphases"></a>Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Операция, реализующая этапы, указанные как частичные отражения

## <a name="remarks"></a>Комментарии

Все фазы являются $ \пи $, за исключением первого отражения о начальном состоянии и последнего отражения состояния целевого объекта, которое равно $0 $.