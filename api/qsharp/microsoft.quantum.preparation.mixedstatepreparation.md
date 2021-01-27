---
uid: Microsoft.Quantum.Preparation.MixedStatePreparation
title: Определяемый пользователем тип Микседстатепрепаратион
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparation
qsharp.summary: Represents a particular mixed state that can be prepared on an index and a garbage register.
ms.openlocfilehash: 7e5b6ca755aac19a31b7e27e32e934bb823b128e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842406"
---
# <a name="mixedstatepreparation-user-defined-type"></a>Определяемый пользователем тип Микседстатепрепаратион

Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет конкретное смешанное состояние, которое может быть подготовлено для индекса и для регистрации мусора.

```qsharp

newtype MixedStatePreparation = (Requirements : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements, Norm : Double, Prepare : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Именованные элементы

### <a name="requirements--mixedstatepreparationrequirements"></a>Требования: [микседстатепрепаратионрекуирементс](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)


### <a name="norm--double"></a>Норма: [Double](xref:microsoft.quantum.lang-ref.double)


### <a name="prepare--littleendianqubitqubit--unit--is-adj--ctl"></a>Подготовка: ([литтлиндиан](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[кубит](xref:microsoft.quantum.lang-ref.qubit)[],[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"



## <a name="see-also"></a>См. также:

- [Microsoft. тактов. Пурифиедмикседстате](xref:Microsoft.Quantum.PurifiedMixedState)