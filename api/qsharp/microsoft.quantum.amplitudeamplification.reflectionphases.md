---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Определяемый пользователем тип Рефлектионфасес
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: fc3642b76c6e01f0709e78ea42c9ea7237389afa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847180"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="ab709-102">Определяемый пользователем тип Рефлектионфасес</span><span class="sxs-lookup"><span data-stu-id="ab709-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="ab709-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="ab709-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="ab709-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ab709-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ab709-105">Этапы последовательности частичных отражений в усилении амплитуды.</span><span class="sxs-lookup"><span data-stu-id="ab709-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="ab709-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="ab709-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="ab709-107">Абаутстарт: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ab709-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ab709-108">Массив этапов для отражения состояния запуска.</span><span class="sxs-lookup"><span data-stu-id="ab709-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="ab709-109">Абауттаржет: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ab709-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ab709-110">Массив этапов для отражения состояния целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="ab709-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab709-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="ab709-111">Remarks</span></span>

<span data-ttu-id="ab709-112">Оба массива должны иметь одинаковую длину.</span><span class="sxs-lookup"><span data-stu-id="ab709-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="ab709-113">Обратите внимание, что во многих случаях первый этап о начальном состоянии и последнем этапе о целевом состоянии представляет собой смену глобального этапа и может иметь значение $0 $.</span><span class="sxs-lookup"><span data-stu-id="ab709-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>