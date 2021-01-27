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
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="e3610-102">Определяемый пользователем тип Рефлектионоракле</span><span class="sxs-lookup"><span data-stu-id="e3610-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="e3610-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="e3610-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="e3610-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e3610-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e3610-105">Представляет Oracle отражения.</span><span class="sxs-lookup"><span data-stu-id="e3610-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="e3610-106">Отражение Oracle, $O $, имеет входные данные:</span><span class="sxs-lookup"><span data-stu-id="e3610-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="e3610-107">Этап $ \фи $, на который нужно повернуть отраженное подпространство.</span><span class="sxs-lookup"><span data-stu-id="e3610-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="e3610-108">Регистр кубит, в котором выполняется данное отражение.</span><span class="sxs-lookup"><span data-stu-id="e3610-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="e3610-109">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="e3610-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="e3610-110">Апплирефлектион: ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="e3610-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="e3610-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="e3610-111">Remarks</span></span>

<span data-ttu-id="e3610-112">Эта $O Oracle = \болдоне-(1-e ^ {i \фи}) \кет{\пси}\бра{\пси} $ выполняет частичное отражение на фазе $ \фи $ о одном чистом состоянии $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="e3610-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>