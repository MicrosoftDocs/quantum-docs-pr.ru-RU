---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Функция Пурифиедмикседстатерекуирементс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 6ddb48ba66eea87a07d515ff791bfb34f2d98b76
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856833"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="cf4a8-102">Функция Пурифиедмикседстатерекуирементс</span><span class="sxs-lookup"><span data-stu-id="cf4a8-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="cf4a8-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="cf4a8-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="cf4a8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cf4a8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cf4a8-105">Возвращает общее число Кубитс, которые должны быть выделены для применения операции, возвращенной @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="cf4a8-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="cf4a8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cf4a8-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="cf4a8-107">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cf4a8-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cf4a8-108">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="cf4a8-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="cf4a8-109">НкоеффиЦиентс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cf4a8-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cf4a8-110">Число коэффициентов, которые должны быть указаны при подготовке смешанного состояния.</span><span class="sxs-lookup"><span data-stu-id="cf4a8-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="cf4a8-111">Выходные данные: [микседстатепрепаратионрекуирементс](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="cf4a8-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="cf4a8-112">Описание того, сколько Кубитс требуется в целом, и для каждого индекса и регистров мусора, используемых @"microsoft.quantum.preparation.purifiedmixedstate" функцией.</span><span class="sxs-lookup"><span data-stu-id="cf4a8-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf4a8-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="cf4a8-113">See Also</span></span>

- [<span data-ttu-id="cf4a8-114">Microsoft. тактов. подготовка. Пурифиедмикседстате</span><span class="sxs-lookup"><span data-stu-id="cf4a8-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)