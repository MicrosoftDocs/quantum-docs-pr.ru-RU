---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Определяемый пользователем тип Рефлектионфасес
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: e0c7db6cd1aad636a34684958be117de1b9888f8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92731969"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="f4ccb-102">Определяемый пользователем тип Рефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="f4ccb-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="f4ccb-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="f4ccb-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="f4ccb-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f4ccb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f4ccb-105">Этапы последовательности частичных отражений в усилении амплитуды.</span><span class="sxs-lookup"><span data-stu-id="f4ccb-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="f4ccb-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="f4ccb-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="f4ccb-107">Абаутстарт: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f4ccb-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f4ccb-108">Массив этапов для отражения состояния запуска.</span><span class="sxs-lookup"><span data-stu-id="f4ccb-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="f4ccb-109">Абауттаржет: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f4ccb-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f4ccb-110">Массив этапов для отражения состояния целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="f4ccb-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4ccb-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="f4ccb-111">Remarks</span></span>

<span data-ttu-id="f4ccb-112">Оба массива должны иметь одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="f4ccb-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="f4ccb-113">Обратите внимание, что во многих случаях первый этап о начальном состоянии и последнем этапе о целевом состоянии представляет собой смену глобального этапа и может иметь значение $0 $.</span><span class="sxs-lookup"><span data-stu-id="f4ccb-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>