---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Определяемый пользователем тип Ротатионфасес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: b0373f964b77f8ea561c6e96b11e476b42e7fc55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731944"
---
# <a name="rotationphases-user-defined-type"></a>Определяемый пользователем тип Ротатионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакеты [](https://nuget.org/packages/)


Фазы для последовательности однокубитных поворотов в усилении амплитуды.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Remarks

Первый параметр — это массив фаз для отражения, выраженный в виде произведения однокубитных поворотов.
[Г.Х. Низкая, I. L. Чжуанский, https://arxiv.org/abs/1707.05391 ].