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
# <a name="mixedstatepreparationrequirements-user-defined-type"></a>Определяемый пользователем тип Микседстатепрепаратионрекуирементс

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет число Кубитс, необходимых для подготовки заданного смешанного состояния.

```qsharp

newtype MixedStatePreparationRequirements = (NTotalQubits : Int, (NIndexQubits : Int, NGarbageQubits : Int));
```



## <a name="named-items"></a>Именованные элементы

### <a name="ntotalqubits--int"></a>Нтоталкубитс: [int](xref:microsoft.quantum.lang-ref.int)


### <a name="nindexqubits--int"></a>Ниндекскубитс: [int](xref:microsoft.quantum.lang-ref.int)


### <a name="ngarbagequbits--int"></a>Нгарбажекубитс: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Пурифиедмикседстате](xref:Microsoft.Quantum.PurifiedMixedState)