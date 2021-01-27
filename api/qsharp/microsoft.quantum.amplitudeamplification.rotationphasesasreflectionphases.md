---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: Функция Ротатионфасесасрефлектионфасес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 5d50b3fdc2b0f948e93cb11b5c69403d97574ccd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843952"
---
# <a name="rotationphasesasreflectionphases-function"></a>Функция Ротатионфасесасрефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Преобразует этапы, указанные в виде однокубитных поворотов, на фазы, указанные как частичные отражения.

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Входные данные

### <a name="rotphases--rotationphases"></a>Ротфасес: [ротатионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)

Массив однокубитных поворотов для преобразования в частичные отражения.



## <a name="output--reflectionphases"></a>Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Операция, реализующая этапы, указанные как частичные отражения.

## <a name="references"></a>Ссылки

Мы используем соглашение в

- [ *Г.х. низкий, I. L. Чжуанский*](https://arxiv.org/abs/1707.05391) для связывания фаз вращения одного кубит с этапами оператора отражения.