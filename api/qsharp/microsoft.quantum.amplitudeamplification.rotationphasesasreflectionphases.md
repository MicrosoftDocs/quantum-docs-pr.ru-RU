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
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="90596-102">Функция Ротатионфасесасрефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="90596-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="90596-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="90596-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="90596-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90596-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90596-105">Преобразует этапы, указанные в виде однокубитных поворотов, на фазы, указанные как частичные отражения.</span><span class="sxs-lookup"><span data-stu-id="90596-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="90596-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="90596-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="90596-107">Ротфасес: [ротатионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="90596-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="90596-108">Массив однокубитных поворотов для преобразования в частичные отражения.</span><span class="sxs-lookup"><span data-stu-id="90596-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="90596-109">Выходные данные: [рефлектионфасес](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="90596-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="90596-110">Операция, реализующая этапы, указанные как частичные отражения.</span><span class="sxs-lookup"><span data-stu-id="90596-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="90596-111">Ссылки</span><span class="sxs-lookup"><span data-stu-id="90596-111">References</span></span>

<span data-ttu-id="90596-112">Мы используем соглашение в</span><span class="sxs-lookup"><span data-stu-id="90596-112">We use the convention in</span></span>

- <span data-ttu-id="90596-113">[ *Г.х. низкий, I. L. Чжуанский*](https://arxiv.org/abs/1707.05391) для связывания фаз вращения одного кубит с этапами оператора отражения.</span><span class="sxs-lookup"><span data-stu-id="90596-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>