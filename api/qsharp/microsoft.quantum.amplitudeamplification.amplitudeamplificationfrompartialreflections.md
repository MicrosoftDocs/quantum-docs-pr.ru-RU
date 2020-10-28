---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Функция Амплитудеамплификатионфромпартиалрефлектионс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: fc7c2c0d05ea626f7f7e5d8ebf3ce5ecea61390b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732048"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a>Функция Амплитудеамплификатионфромпартиалрефлектионс

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


Усиление амплитуды путем частичной отражения.

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Входные данные

### <a name="phases--reflectionphases"></a>этапы: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Фазы частичной отражения


### <a name="startstatereflection--reflectionoracle"></a>Стартстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Оператор отражения о начальном состоянии


### <a name="targetstatereflection--reflectionoracle"></a>Таржетстатерефлектион: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Оператор отражения о целевом состоянии



## <a name="output--qubit--unit-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [единицы измерения](xref:microsoft.quantum.lang-ref.unit) + CTL

Операция, реализующая усиление амплитуды путем частичной отражения.

## <a name="remarks"></a>Remarks

Усиление амплитуды — это особый случай усиления амплитуды очевидным, когда нет Кубитс системы, а очевидным Oracle имеет значение Identity.
В большинстве случаев `startQubits` инициализируется в состоянии $ \кет{\текст{старт}} \_ $1, которое является $-$1 еиженстате `startStateReflection` .