---
uid: Microsoft.Quantum.AmplitudeAmplification.TargetStateReflectionOracle
title: Функция Таржетстатерефлектионоракле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: TargetStateReflectionOracle
qsharp.summary: >-
  Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.

  The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.
ms.openlocfilehash: 65ad316a6ac986ebd0dc28b25859026a60aa3239
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191114"
---
# <a name="targetstatereflectionoracle-function"></a><span data-ttu-id="e9f13-102">Функция Таржетстатерефлектионоракле</span><span class="sxs-lookup"><span data-stu-id="e9f13-102">TargetStateReflectionOracle function</span></span>

<span data-ttu-id="e9f13-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="e9f13-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="e9f13-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e9f13-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e9f13-105">Конструирует `ReflectionOracle` о целевом состоянии, уникально помеченном флагом кубит.</span><span class="sxs-lookup"><span data-stu-id="e9f13-105">Constructs a `ReflectionOracle` about the target state uniquely marked by the flag qubit.</span></span>

<span data-ttu-id="e9f13-106">Целевое состояние имеет одно значение кубит, равное 1, и все остальные 0: $ \кет {1} _f $.</span><span class="sxs-lookup"><span data-stu-id="e9f13-106">The target state has a single qubit set to 1, and all others 0: $\ket{1}_f$.</span></span>

```qsharp
function TargetStateReflectionOracle (idxFlagQubit : Int) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="input"></a><span data-ttu-id="e9f13-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="e9f13-107">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="e9f13-108">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e9f13-108">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e9f13-109">Индекс, помечающий кубит $f $ of Oracle.</span><span class="sxs-lookup"><span data-stu-id="e9f13-109">Index to flag qubit $f$ of oracle.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="e9f13-110">Выходные данные: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="e9f13-110">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="e9f13-111">Значение типа `ReflectionOracle` , которое отражает состояние, отмеченное параметром $ \кет {1} _f $.</span><span class="sxs-lookup"><span data-stu-id="e9f13-111">A `ReflectionOracle` that reflects about the state marked by $\ket{1}_f$.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9f13-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="e9f13-112">See Also</span></span>

- [<span data-ttu-id="e9f13-113">Microsoft. тактов. Canon. Рефлектионоракле</span><span class="sxs-lookup"><span data-stu-id="e9f13-113">Microsoft.Quantum.Canon.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Canon.ReflectionOracle)