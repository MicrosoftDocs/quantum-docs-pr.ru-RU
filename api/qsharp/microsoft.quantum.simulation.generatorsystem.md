---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Определяемый пользователем тип Женераторсистем
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 20092a8deca50c90f46f4d79c6b40b805f135754
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225233"
---
# <a name="generatorsystem-user-defined-type"></a>Определяемый пользователем тип Женераторсистем

Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет коллекцию `GeneratorIndex` ES.

Мы перебираем эту коллекцию с помощью целого числа с одним индексом, и размер коллекции считается известным.

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a>Комментарии

Экземпляры `GeneratorSystem` можно легко определить с помощью <xref:microsoft.quantum.arrays.lookupfunction> функции.

## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Arrays. Лукупфунктион](xref:Microsoft.Quantum.Arrays.LookupFunction)