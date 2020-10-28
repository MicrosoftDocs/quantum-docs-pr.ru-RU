---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Определяемый пользователем тип Декомпоситионстате
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: 0547c04828a80b4f696cc17e13c8cc57d0379f96
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733912"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="7b08a-102">Определяемый пользователем тип Декомпоситионстате</span><span class="sxs-lookup"><span data-stu-id="7b08a-102">DecompositionState user defined type</span></span>

<span data-ttu-id="7b08a-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="7b08a-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="7b08a-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7b08a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7b08a-105">Состояние во время декомпозиции на основе индексов переменных</span><span class="sxs-lookup"><span data-stu-id="7b08a-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="7b08a-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="7b08a-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="7b08a-107">Разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7b08a-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="7b08a-108">Лфунктионс: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="7b08a-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="7b08a-109">Рфунктионс: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="7b08a-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="7b08a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7b08a-110">Description</span></span>

<span data-ttu-id="7b08a-111">Состояние содержит текущую перестановку и созданные в настоящее время функции для контролируемых шлюзов слева, а также контролируемые шлюзы справа.</span><span class="sxs-lookup"><span data-stu-id="7b08a-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>