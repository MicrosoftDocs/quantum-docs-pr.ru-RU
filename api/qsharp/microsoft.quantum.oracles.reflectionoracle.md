---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Определяемый пользователем тип Рефлектионоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 1ef07126596b70d2c5574430656009116c34d2bc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854488"
---
# <a name="reflectionoracle-user-defined-type"></a>Определяемый пользователем тип Рефлектионоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет Oracle отражения.

Отражение Oracle, $O $, имеет входные данные:

- Этап $ \фи $, на который нужно повернуть отраженное подпространство.
- Регистр кубит, в котором выполняется данное отражение.

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a>Именованные элементы

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a>Апплирефлектион: ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"



## <a name="remarks"></a>Remarks

Эта $O Oracle = \болдоне-(1-e ^ {i \фи}) \кет{\пси}\бра{\пси} $ выполняет частичное отражение на фазе $ \фи $ о одном чистом состоянии $ \кет{\пси} $.