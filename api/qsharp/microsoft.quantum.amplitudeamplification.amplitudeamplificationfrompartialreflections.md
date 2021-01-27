---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Функция Амплитудеамплификатионфромпартиалрефлектионс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: e4030aabcab55db35bcb8199e37bee837ead6ad0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845898"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a>Функция Амплитудеамплификатионфромпартиалрефлектионс

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="output--qubit--unit--is-adj--ctl"></a>Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL

Операция, реализующая усиление амплитуды путем частичной отражения.

## <a name="remarks"></a>Remarks

Усиление амплитуды — это особый случай усиления амплитуды очевидным, когда нет Кубитс системы, а очевидным Oracle имеет значение Identity.
В большинстве случаев `startQubits` инициализируется в состоянии $ \кет{\текст{старт}} \_ $1, которое является $-$1 еиженстате `startStateReflection` .