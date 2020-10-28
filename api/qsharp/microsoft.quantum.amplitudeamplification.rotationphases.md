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
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="b6e3c-102">Определяемый пользователем тип Ротатионфасес</span><span class="sxs-lookup"><span data-stu-id="b6e3c-102">RotationPhases user defined type</span></span>

<span data-ttu-id="b6e3c-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="b6e3c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="b6e3c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b6e3c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b6e3c-105">Фазы для последовательности однокубитных поворотов в усилении амплитуды.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="b6e3c-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="b6e3c-106">Remarks</span></span>

<span data-ttu-id="b6e3c-107">Первый параметр — это массив фаз для отражения, выраженный в виде произведения однокубитных поворотов.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="b6e3c-108">[Г.Х.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-108">[ G.H.</span></span> <span data-ttu-id="b6e3c-109">Низкая, I. L.</span><span class="sxs-lookup"><span data-stu-id="b6e3c-109">Low, I. L.</span></span> <span data-ttu-id="b6e3c-110">Чжуанский, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="b6e3c-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>