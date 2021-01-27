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