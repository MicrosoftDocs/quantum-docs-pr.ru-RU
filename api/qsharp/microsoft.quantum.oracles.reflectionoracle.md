---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Определяемый пользователем тип Рефлектионоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 8e35e7e508ea7e0c30ea2a70633f71a6c87d4be1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733337"
---
# <a name="reflectionoracle-user-defined-type"></a>Определяемый пользователем тип Рефлектионоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


Представляет Oracle отражения.

Отражение Oracle, $O $, имеет входные данные:

- Этап $ \фи $, на который нужно повернуть отраженное подпространство.
- Регистр кубит, в котором выполняется данное отражение.

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Именованные элементы

### <a name="applyreflection--doublequbit--unit-adj--ctl"></a>Апплирефлектион: ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная начисление [единиц](xref:microsoft.quantum.lang-ref.unit) + CTL



## <a name="remarks"></a>Remarks

Эта $O Oracle = \болдоне-(1-e ^ {i \фи}) \кет{\пси}\бра{\пси} $ выполняет частичное отражение на фазе $ \фи $ о одном чистом состоянии $ \кет{\пси} $.