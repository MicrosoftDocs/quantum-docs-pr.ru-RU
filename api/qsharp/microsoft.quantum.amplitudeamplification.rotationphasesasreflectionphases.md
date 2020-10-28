---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: Функция Ротатионфасесасрефлектионфасес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: d62a7584324c9467ccc759e4bed81acbceee719c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731936"
---
# <a name="rotationphasesasreflectionphases-function"></a>Функция Ротатионфасесасрефлектионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


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