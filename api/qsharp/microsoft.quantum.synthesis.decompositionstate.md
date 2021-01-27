---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Определяемый пользователем тип Декомпоситионстате
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: eb2aed53b4116a4ea72ee732ff46c4a10eb3d67b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855505"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="6cbe9-102">Определяемый пользователем тип Декомпоситионстате</span><span class="sxs-lookup"><span data-stu-id="6cbe9-102">DecompositionState user defined type</span></span>

<span data-ttu-id="6cbe9-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6cbe9-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6cbe9-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6cbe9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6cbe9-105">Состояние во время декомпозиции на основе индексов переменных</span><span class="sxs-lookup"><span data-stu-id="6cbe9-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="6cbe9-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="6cbe9-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="6cbe9-107">Разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6cbe9-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="6cbe9-108">Лфунктионс: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="6cbe9-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="6cbe9-109">Рфунктионс: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="6cbe9-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="6cbe9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6cbe9-110">Description</span></span>

<span data-ttu-id="6cbe9-111">Состояние содержит текущую перестановку и созданные в настоящее время функции для контролируемых шлюзов слева, а также контролируемые шлюзы справа.</span><span class="sxs-lookup"><span data-stu-id="6cbe9-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>