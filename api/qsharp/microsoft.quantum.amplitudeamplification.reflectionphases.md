---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Определяемый пользователем тип Рефлектионфасес
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: 743ece778239c223573a3a8536ae8059cea09d5f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191352"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="f151c-102">Определяемый пользователем тип Рефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="f151c-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="f151c-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="f151c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="f151c-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f151c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f151c-105">Этапы последовательности частичных отражений в усилении амплитуды.</span><span class="sxs-lookup"><span data-stu-id="f151c-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="f151c-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="f151c-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="f151c-107">Абаутстарт: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f151c-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f151c-108">Массив этапов для отражения состояния запуска.</span><span class="sxs-lookup"><span data-stu-id="f151c-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="f151c-109">Абауттаржет: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f151c-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f151c-110">Массив этапов для отражения состояния целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f151c-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="f151c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f151c-111">Remarks</span></span>

<span data-ttu-id="f151c-112">Оба массива должны иметь одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="f151c-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="f151c-113">Обратите внимание, что во многих случаях первый этап о начальном состоянии и последнем этапе о целевом состоянии представляет собой смену глобального этапа и может иметь значение $0 $.</span><span class="sxs-lookup"><span data-stu-id="f151c-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>