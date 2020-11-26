---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Функция Пурифиедмикседстатерекуирементс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229993"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="032d8-102">Функция Пурифиедмикседстатерекуирементс</span><span class="sxs-lookup"><span data-stu-id="032d8-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="032d8-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="032d8-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="032d8-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="032d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="032d8-105">Возвращает общее число Кубитс, которые должны быть выделены для применения операции, возвращенной @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="032d8-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="032d8-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="032d8-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="032d8-107">Таржетеррор: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="032d8-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="032d8-108">Целевая ошибка $ \епсилон $.</span><span class="sxs-lookup"><span data-stu-id="032d8-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="032d8-109">НкоеффиЦиентс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="032d8-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="032d8-110">Число коэффициентов, которые должны быть указаны при подготовке смешанного состояния.</span><span class="sxs-lookup"><span data-stu-id="032d8-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="032d8-111">Выходные данные: [микседстатепрепаратионрекуирементс](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="032d8-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="032d8-112">Описание того, сколько Кубитс требуется в целом, и для каждого индекса и регистров мусора, используемых @"microsoft.quantum.preparation.purifiedmixedstate" функцией.</span><span class="sxs-lookup"><span data-stu-id="032d8-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="032d8-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="032d8-113">See Also</span></span>

- [<span data-ttu-id="032d8-114">Microsoft. тактов. подготовка. Пурифиедмикседстате</span><span class="sxs-lookup"><span data-stu-id="032d8-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)