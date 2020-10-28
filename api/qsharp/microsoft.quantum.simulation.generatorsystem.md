---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Определяемый пользователем тип Женераторсистем
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: c03caf99b197410c7fa15021c8acaaf55a728781
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733537"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="d1d61-102">Определяемый пользователем тип Женераторсистем</span><span class="sxs-lookup"><span data-stu-id="d1d61-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="d1d61-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d1d61-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d1d61-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d1d61-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d1d61-105">Представляет коллекцию `GeneratorIndex` ES.</span><span class="sxs-lookup"><span data-stu-id="d1d61-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="d1d61-106">Мы перебираем эту коллекцию с помощью целого числа с одним индексом, и размер коллекции считается известным.</span><span class="sxs-lookup"><span data-stu-id="d1d61-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="d1d61-107">Remarks</span><span class="sxs-lookup"><span data-stu-id="d1d61-107">Remarks</span></span>

<span data-ttu-id="d1d61-108">Экземпляры `GeneratorSystem` можно легко определить с помощью <xref:microsoft.quantum.arrays.lookupfunction> функции.</span><span class="sxs-lookup"><span data-stu-id="d1d61-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1d61-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="d1d61-109">See Also</span></span>

- [<span data-ttu-id="d1d61-110">Microsoft. тактов. Arrays. Лукупфунктион</span><span class="sxs-lookup"><span data-stu-id="d1d61-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)