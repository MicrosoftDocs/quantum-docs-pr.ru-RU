---
uid: Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
title: Определяемый пользователем тип Микседстатепрепаратионрекуирементс
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparationRequirements
qsharp.summary: Represents the number of qubits required in order to prepare a given mixed state.
ms.openlocfilehash: 3ea4757f6aa5125418b1e81db9f32e7b668eb359
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228701"
---
# <a name="mixedstatepreparationrequirements-user-defined-type"></a><span data-ttu-id="2f34f-102">Определяемый пользователем тип Микседстатепрепаратионрекуирементс</span><span class="sxs-lookup"><span data-stu-id="2f34f-102">MixedStatePreparationRequirements user defined type</span></span>

<span data-ttu-id="2f34f-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2f34f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2f34f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2f34f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2f34f-105">Представляет число Кубитс, необходимых для подготовки заданного смешанного состояния.</span><span class="sxs-lookup"><span data-stu-id="2f34f-105">Represents the number of qubits required in order to prepare a given mixed state.</span></span>

```qsharp

newtype MixedStatePreparationRequirements = (NTotalQubits : Int, (NIndexQubits : Int, NGarbageQubits : Int));
```



## <a name="named-items"></a><span data-ttu-id="2f34f-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="2f34f-106">Named Items</span></span>

### <a name="ntotalqubits--int"></a><span data-ttu-id="2f34f-107">Нтоталкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2f34f-107">NTotalQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="nindexqubits--int"></a><span data-ttu-id="2f34f-108">Ниндекскубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2f34f-108">NIndexQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="ngarbagequbits--int"></a><span data-ttu-id="2f34f-109">Нгарбажекубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2f34f-109">NGarbageQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="see-also"></a><span data-ttu-id="2f34f-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="2f34f-110">See Also</span></span>

- [<span data-ttu-id="2f34f-111">Microsoft. тактов. Пурифиедмикседстате</span><span class="sxs-lookup"><span data-stu-id="2f34f-111">Microsoft.Quantum.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.PurifiedMixedState)