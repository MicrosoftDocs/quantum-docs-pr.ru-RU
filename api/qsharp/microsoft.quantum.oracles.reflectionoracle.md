---
uid: Microsoft.Quantum.Oracles.ReflectionOracle
title: Определяемый пользователем тип Рефлектионоракле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracle
qsharp.summary: >-
  Represents a reflection oracle.

  A reflection oracle, $O$, has inputs:

  - The phase $\phi$ by which to rotate the reflected subspace. - The qubit register on which to perform the given reflection.
ms.openlocfilehash: 7bb0626e7cca9ae0b640699ea57f2e114bda2d06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226661"
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



## <a name="remarks"></a>Комментарии

Эта $O Oracle = \болдоне-(1-e ^ {i \фи}) \кет{\пси}\бра{\пси} $ выполняет частичное отражение на фазе $ \фи $ о одном чистом состоянии $ \кет{\пси} $.