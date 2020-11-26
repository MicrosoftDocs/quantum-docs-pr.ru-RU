---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Определяемый пользователем тип Декомпоситионстате
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: cd2a55013f1232d4158dd6c33143b7cf6c0aafbc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203201"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="bc60b-102">Определяемый пользователем тип Декомпоситионстате</span><span class="sxs-lookup"><span data-stu-id="bc60b-102">DecompositionState user defined type</span></span>

<span data-ttu-id="bc60b-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="bc60b-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="bc60b-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bc60b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bc60b-105">Состояние во время декомпозиции на основе индексов переменных</span><span class="sxs-lookup"><span data-stu-id="bc60b-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="bc60b-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="bc60b-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="bc60b-107">Разрешение: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="bc60b-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="bc60b-108">Лфунктионс: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="bc60b-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="bc60b-109">Рфунктионс: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="bc60b-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="bc60b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bc60b-110">Description</span></span>

<span data-ttu-id="bc60b-111">Состояние содержит текущую перестановку и созданные в настоящее время функции для контролируемых шлюзов слева, а также контролируемые шлюзы справа.</span><span class="sxs-lookup"><span data-stu-id="bc60b-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>