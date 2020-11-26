---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Определяемый пользователем тип Детерминистикстатеоракле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 6f8f80aacd3386ba61675101acb87e09fff5afff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193936"
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



## <a name="remarks"></a>Комментарии

Эта база данных Oracle, определенная $O \кет {0} = \кет{\пси} $, действует в состоянии вычислительного основания $ \кет {0} $ для создания состояния $ \кет{\пси} $.
Первый параметр — это кубит регистр $ \кет{\пси} $.