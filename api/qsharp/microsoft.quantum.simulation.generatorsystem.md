---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Определяемый пользователем тип Женераторсистем
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 3748d3fb79597fb526c86a91bc28290155189014
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858406"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="11b4f-102">Определяемый пользователем тип Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="11b4f-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="11b4f-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="11b4f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="11b4f-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11b4f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11b4f-105">Представляет коллекцию `GeneratorIndex` ES.</span><span class="sxs-lookup"><span data-stu-id="11b4f-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="11b4f-106">Мы перебираем эту коллекцию с помощью целого числа с одним индексом, и размер коллекции считается известным.</span><span class="sxs-lookup"><span data-stu-id="11b4f-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="11b4f-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="11b4f-107">Remarks</span></span>

<span data-ttu-id="11b4f-108">Экземпляры `GeneratorSystem` можно легко определить с помощью <xref:microsoft.quantum.arrays.lookupfunction> функции.</span><span class="sxs-lookup"><span data-stu-id="11b4f-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="11b4f-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="11b4f-109">See Also</span></span>

- [<span data-ttu-id="11b4f-110">Microsoft. тактов. Arrays. Лукупфунктион</span><span class="sxs-lookup"><span data-stu-id="11b4f-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)