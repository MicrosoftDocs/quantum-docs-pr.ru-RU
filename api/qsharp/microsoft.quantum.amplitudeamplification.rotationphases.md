---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Определяемый пользователем тип Ротатионфасес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 2f955ce3bfb9ea057c26c79547895df39ed322ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843963"
---
# <a name="rotationphases-user-defined-type"></a>Определяемый пользователем тип Ротатионфасес

Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Фазы для последовательности однокубитных поворотов в усилении амплитуды.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Remarks

Первый параметр — это массив фаз для отражения, выраженный в виде произведения однокубитных поворотов.
[Г.Х. Низкая, I. L. Чжуанский, https://arxiv.org/abs/1707.05391 ].