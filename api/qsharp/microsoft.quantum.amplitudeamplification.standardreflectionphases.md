---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Функция Стандардрефлектионфасес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: c189b34b641989ab458986fb3f2872759b949be5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731921"
---
# <a name="standardreflectionphases-function"></a>Функция Стандардрефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


Вычисление этапов частичного отражения для стандартного усиления амплитуды.

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Входные данные

### <a name="niterations--int"></a>Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)

Число итераций усиления амплитуды для создания фаз частичного отражения для.



## <a name="output--reflectionphases"></a>Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Операция, реализующая этапы, указанные как частичные отражения

## <a name="remarks"></a>Remarks

Все фазы являются $ \пи $, за исключением первого отражения о начальном состоянии и последнего отражения состояния целевого объекта, которое равно $0 $.