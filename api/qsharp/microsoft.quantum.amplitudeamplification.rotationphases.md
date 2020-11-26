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
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="942c7-102">Определяемый пользователем тип Ротатионфасес</span><span class="sxs-lookup"><span data-stu-id="942c7-102">RotationPhases user defined type</span></span>

<span data-ttu-id="942c7-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="942c7-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="942c7-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="942c7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="942c7-105">Фазы для последовательности однокубитных поворотов в усилении амплитуды.</span><span class="sxs-lookup"><span data-stu-id="942c7-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="942c7-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="942c7-106">Remarks</span></span>

<span data-ttu-id="942c7-107">Первый параметр — это массив фаз для отражения, выраженный в виде произведения однокубитных поворотов.</span><span class="sxs-lookup"><span data-stu-id="942c7-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="942c7-108">[Г.Х.</span><span class="sxs-lookup"><span data-stu-id="942c7-108">[ G.H.</span></span> <span data-ttu-id="942c7-109">Низкая, I. L.</span><span class="sxs-lookup"><span data-stu-id="942c7-109">Low, I. L.</span></span> <span data-ttu-id="942c7-110">Чжуанский, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="942c7-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>