---
uid: Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
title: Определяемый пользователем тип Микседстатепрепаратионрекуирементс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparationRequirements
qsharp.summary: Represents the number of qubits required in order to prepare a given mixed state.
ms.openlocfilehash: df57b7b43fc84f7ddf68392f6a2b7013225da730
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856934"
---
# <a name="mixedstatepreparationrequirements-user-defined-type"></a><span data-ttu-id="c3191-102">Определяемый пользователем тип Микседстатепрепаратионрекуирементс</span><span class="sxs-lookup"><span data-stu-id="c3191-102">MixedStatePreparationRequirements user defined type</span></span>

<span data-ttu-id="c3191-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="c3191-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="c3191-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c3191-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c3191-105">Представляет число Кубитс, необходимых для подготовки заданного смешанного состояния.</span><span class="sxs-lookup"><span data-stu-id="c3191-105">Represents the number of qubits required in order to prepare a given mixed state.</span></span>

```qsharp

newtype MixedStatePreparationRequirements = (NTotalQubits : Int, (NIndexQubits : Int, NGarbageQubits : Int));
```



## <a name="named-items"></a><span data-ttu-id="c3191-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="c3191-106">Named Items</span></span>

### <a name="ntotalqubits--int"></a><span data-ttu-id="c3191-107">Нтоталкубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3191-107">NTotalQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="nindexqubits--int"></a><span data-ttu-id="c3191-108">Ниндекскубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3191-108">NIndexQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


### <a name="ngarbagequbits--int"></a><span data-ttu-id="c3191-109">Нгарбажекубитс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3191-109">NGarbageQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="see-also"></a><span data-ttu-id="c3191-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="c3191-110">See Also</span></span>

- [<span data-ttu-id="c3191-111">Microsoft. тактов. Пурифиедмикседстате</span><span class="sxs-lookup"><span data-stu-id="c3191-111">Microsoft.Quantum.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.PurifiedMixedState)