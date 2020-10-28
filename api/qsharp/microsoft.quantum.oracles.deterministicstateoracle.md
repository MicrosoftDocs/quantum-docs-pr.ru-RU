---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Определяемый пользователем тип Детерминистикстатеоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: f02267d48cf42fb5b02782dc6b667ac7b60a05dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733385"
---
# <a name="deterministicstateoracle-user-defined-type"></a>Определяемый пользователем тип Детерминистикстатеоракле

Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)

Пакеты [](https://nuget.org/packages/)


Представляет Oracle для подготовки детерминированного состояния.

Входные данные для Oracle $O $:

- Регистр, в котором будет храниться требуемое состояние такта $ \кет{\пси} \_ s $.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Remarks

Эта база данных Oracle, определенная $O \кет {0} = \кет{\пси} $, действует в состоянии вычислительного основания $ \кет {0} $ для создания состояния $ \кет{\пси} $.
Первый параметр — это кубит регистр $ \кет{\пси} $.