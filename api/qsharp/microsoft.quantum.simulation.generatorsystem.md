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
# <a name="generatorsystem-user-defined-type"></a>Определяемый пользователем тип Женераторсистем

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакеты [](https://nuget.org/packages/)


Представляет коллекцию `GeneratorIndex` ES.

Мы перебираем эту коллекцию с помощью целого числа с одним индексом, и размер коллекции считается известным.

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a>Remarks

Экземпляры `GeneratorSystem` можно легко определить с помощью <xref:microsoft.quantum.arrays.lookupfunction> функции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Лукупфунктион](xref:Microsoft.Quantum.Arrays.LookupFunction)