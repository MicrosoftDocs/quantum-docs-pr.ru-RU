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
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="244e2-102">Определяемый пользователем тип Детерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="244e2-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="244e2-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="244e2-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="244e2-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="244e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="244e2-105">Представляет Oracle для подготовки детерминированного состояния.</span><span class="sxs-lookup"><span data-stu-id="244e2-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="244e2-106">Входные данные для Oracle $O $:</span><span class="sxs-lookup"><span data-stu-id="244e2-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="244e2-107">Регистр, в котором будет храниться требуемое состояние такта $ \кет{\пси} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="244e2-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="244e2-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="244e2-108">Remarks</span></span>

<span data-ttu-id="244e2-109">Эта база данных Oracle, определенная $O \кет {0} = \кет{\пси} $, действует в состоянии вычислительного основания $ \кет {0} $ для создания состояния $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="244e2-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="244e2-110">Первый параметр — это кубит регистр $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="244e2-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>