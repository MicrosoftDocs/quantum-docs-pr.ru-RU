---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Определяемый пользователем тип Статеоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 65f4edcf2101190da0c6d00eb4dd21881143ceb0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733345"
---
# <a name="stateoracle-user-defined-type"></a><span data-ttu-id="33f4c-102">Определяемый пользователем тип Статеоракле</span><span class="sxs-lookup"><span data-stu-id="33f4c-102">StateOracle user defined type</span></span>

<span data-ttu-id="33f4c-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="33f4c-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="33f4c-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33f4c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33f4c-105">Представляет Oracle для подготовки состояния.</span><span class="sxs-lookup"><span data-stu-id="33f4c-105">Represents an oracle for state preparation.</span></span>

<span data-ttu-id="33f4c-106">Входные данные для Oracle $O $:</span><span class="sxs-lookup"><span data-stu-id="33f4c-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="33f4c-107">Целочисленное индексирование флага кубит $f $.</span><span class="sxs-lookup"><span data-stu-id="33f4c-107">An integer indexing the flag qubit $f$.</span></span>
- <span data-ttu-id="33f4c-108">Система регистрирует $s $, которая будет хранить требуемое состояние такта $ \кет{\пси} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="33f4c-108">The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="33f4c-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="33f4c-109">Remarks</span></span>

<span data-ttu-id="33f4c-110">Эта база данных Oracle, определяемая $ $ О\кет {0} \_ {f} \кет {0} \_ s = \ламбда\кет {1} \_ ф\кет {\ PSI} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет {0} \_ ф\кдотс, $ $ действует на основе вычислительного состояния $ \кет {0} \_ {f} \кет {0} \_ s $ для создания целевого состояния $ \кет{\пси} \_ s $ с амплитудой $ \ламбда $ в базе, помеченной $ \кет {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="33f4c-110">This oracle defined by $$ O\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, $$ acts on the on computational basis state $\ket{0}\_{f}\ket{0}\_s$ to create the target state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{1}\_f$.</span></span>
<span data-ttu-id="33f4c-111">Первый параметр является индексом кубит регистра $ \кет {0} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="33f4c-111">The first parameter is an index to the qubit register of $\ket{0}\_f$.</span></span> <span data-ttu-id="33f4c-112">Второй параметр охватывает оба регистра.</span><span class="sxs-lookup"><span data-stu-id="33f4c-112">The second parameter encompassed both registers.</span></span>