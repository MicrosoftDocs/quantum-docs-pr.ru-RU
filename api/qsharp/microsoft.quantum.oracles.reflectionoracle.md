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
# <a name="reflectionoracle-user-defined-type"></a><span data-ttu-id="effd6-102">Определяемый пользователем тип Рефлектионоракле</span><span class="sxs-lookup"><span data-stu-id="effd6-102">ReflectionOracle user defined type</span></span>

<span data-ttu-id="effd6-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="effd6-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="effd6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="effd6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="effd6-105">Представляет Oracle отражения.</span><span class="sxs-lookup"><span data-stu-id="effd6-105">Represents a reflection oracle.</span></span>

<span data-ttu-id="effd6-106">Отражение Oracle, $O $, имеет входные данные:</span><span class="sxs-lookup"><span data-stu-id="effd6-106">A reflection oracle, $O$, has inputs:</span></span>

- <span data-ttu-id="effd6-107">Этап $ \фи $, на который нужно повернуть отраженное подпространство.</span><span class="sxs-lookup"><span data-stu-id="effd6-107">The phase $\phi$ by which to rotate the reflected subspace.</span></span>
- <span data-ttu-id="effd6-108">Регистр кубит, в котором выполняется данное отражение.</span><span class="sxs-lookup"><span data-stu-id="effd6-108">The qubit register on which to perform the given reflection.</span></span>

```qsharp

newtype ReflectionOracle = (ApplyReflection : ((Double, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="effd6-109">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="effd6-109">Named Items</span></span>

### <a name="applyreflection--doublequbit--unit--is-adj--ctl"></a><span data-ttu-id="effd6-110">Апплирефлектион: ([Double](xref:microsoft.quantum.lang-ref.double),[кубит](xref:microsoft.quantum.lang-ref.qubit)[]) =>ная [единица](xref:microsoft.quantum.lang-ref.unit)  — "года + CTL"</span><span class="sxs-lookup"><span data-stu-id="effd6-110">ApplyReflection : ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="effd6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="effd6-111">Remarks</span></span>

<span data-ttu-id="effd6-112">Эта $O Oracle = \болдоне-(1-e ^ {i \фи}) \кет{\пси}\бра{\пси} $ выполняет частичное отражение на фазе $ \фи $ о одном чистом состоянии $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="effd6-112">This oracle $O = \boldone - (1 - e^{i \phi}) \ket{\psi}\bra{\psi}$ performs a partial reflection by a phase $\phi$ about a single pure state $\ket{\psi}$.</span></span>