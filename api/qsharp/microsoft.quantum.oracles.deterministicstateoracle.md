---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Определяемый пользователем тип Детерминистикстатеоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 10ae9e52f298cdfb92dd6a9e5cf85960bece6800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842592"
---
# <a name="deterministicstateoracle-user-defined-type"></a>Определяемый пользователем тип Детерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Представляет Oracle для подготовки детерминированного состояния.

Входные данные для Oracle $O $:

- Регистр, в котором будет храниться требуемое состояние такта $ \кет{\пси} \_ s $.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Remarks

Эта база данных Oracle, определенная $O \кет {0} = \кет{\пси} $, действует в состоянии вычислительного основания $ \кет {0} $ для создания состояния $ \кет{\пси} $.
Первый параметр — это кубит регистр $ \кет{\пси} $.