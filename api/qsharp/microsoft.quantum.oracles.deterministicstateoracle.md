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
# <a name="deterministicstateoracle-user-defined-type"></a><span data-ttu-id="d401f-102">Определяемый пользователем тип Детерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="d401f-102">DeterministicStateOracle user defined type</span></span>

<span data-ttu-id="d401f-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="d401f-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="d401f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d401f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d401f-105">Представляет Oracle для подготовки детерминированного состояния.</span><span class="sxs-lookup"><span data-stu-id="d401f-105">Represents an oracle for deterministic state preparation.</span></span>

<span data-ttu-id="d401f-106">Входные данные для Oracle $O $:</span><span class="sxs-lookup"><span data-stu-id="d401f-106">The input to the oracle $O$ is:</span></span>

- <span data-ttu-id="d401f-107">Регистр, в котором будет храниться требуемое состояние такта $ \кет{\пси} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="d401f-107">The register that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="d401f-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="d401f-108">Remarks</span></span>

<span data-ttu-id="d401f-109">Эта база данных Oracle, определенная $O \кет {0} = \кет{\пси} $, действует в состоянии вычислительного основания $ \кет {0} $ для создания состояния $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="d401f-109">This oracle defined by $O\ket{0}=\ket{\psi}$ acts on the on computational basis state $\ket{0}$ to create the state $\ket{\psi}$.</span></span>
<span data-ttu-id="d401f-110">Первый параметр — это кубит регистр $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="d401f-110">The first parameter is the qubit register of $\ket{\psi}$.</span></span>