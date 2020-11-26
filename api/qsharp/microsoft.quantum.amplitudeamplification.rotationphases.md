---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Определяемый пользователем тип Ротатионфасес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191369"
---
# <a name="rotationphases-user-defined-type"></a>Определяемый пользователем тип Ротатионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Фазы для последовательности однокубитных поворотов в усилении амплитуды.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Комментарии

Первый параметр — это массив фаз для отражения, выраженный в виде произведения однокубитных поворотов.
[Г.Х. Низкая, I. L. Чжуанский, https://arxiv.org/abs/1707.05391 ].