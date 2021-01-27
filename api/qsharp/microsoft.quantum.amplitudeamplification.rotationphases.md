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
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="4b12d-102">Определяемый пользователем тип Ротатионфасес</span><span class="sxs-lookup"><span data-stu-id="4b12d-102">RotationPhases user defined type</span></span>

<span data-ttu-id="4b12d-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="4b12d-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="4b12d-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4b12d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4b12d-105">Фазы для последовательности однокубитных поворотов в усилении амплитуды.</span><span class="sxs-lookup"><span data-stu-id="4b12d-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="4b12d-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="4b12d-106">Remarks</span></span>

<span data-ttu-id="4b12d-107">Первый параметр — это массив фаз для отражения, выраженный в виде произведения однокубитных поворотов.</span><span class="sxs-lookup"><span data-stu-id="4b12d-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="4b12d-108">[Г.Х.</span><span class="sxs-lookup"><span data-stu-id="4b12d-108">[ G.H.</span></span> <span data-ttu-id="4b12d-109">Низкая, I. L.</span><span class="sxs-lookup"><span data-stu-id="4b12d-109">Low, I. L.</span></span> <span data-ttu-id="4b12d-110">Чжуанский, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="4b12d-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>