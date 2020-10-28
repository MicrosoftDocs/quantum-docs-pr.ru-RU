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
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="3e43f-102">Определяемый пользователем тип Рефлектионоракле</span><span class="sxs-lookup"><span data-stu-id="3e43f-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="3e43f-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="3e43f-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="3e43f-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3e43f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3e43f-105">Представляет Oracle отражения.</span><span class="sxs-lookup"><span data-stu-id="3e43f-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="3e43f-106">Отражение Oracle, $O $, имеет входные данные:</span><span class="sxs-lookup"><span data-stu-id="3e43f-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="3e43f-107">Этап $ \фи $, на который нужно повернуть отраженное подпространство.</span><span class="sxs-lookup"><span data-stu-id="3e43f-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="3e43f-108">Регистр кубит, в котором выполняется данное отражение.</span><span class="sxs-lookup"><span data-stu-id="3e43f-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="3e43f-109">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="3e43f-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit-adj--ctl"></a><span data-ttu-id="3e43f-110">Апплирефлектион: ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная начисление [единиц](xref:microsoft.quantum.lang-ref.unit) + CTL</span><span class="sxs-lookup"><span data-stu-id="3e43f-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="3e43f-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="3e43f-111">Remarks</span></span>

<span data-ttu-id="3e43f-112">Эта $O Oracle = \болдоне-(1-e ^ {i \фи}) \кет{\пси}\бра{\пси} $ выполняет частичное отражение на фазе $ \фи $ о одном чистом состоянии $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="3e43f-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>