---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Определяемый пользователем тип Обливиаусоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 7c5b35984f3c8828a5ba9bdae8f9effbc1d378f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710988"
---
# <a name="obliviousoracle-user-defined-type"></a><span data-ttu-id="76fb2-102">Определяемый пользователем тип Обливиаусоракле</span><span class="sxs-lookup"><span data-stu-id="76fb2-102">ObliviousOracle user defined type</span></span>

<span data-ttu-id="76fb2-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="76fb2-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="76fb2-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="76fb2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="76fb2-105">Представляет Oracle для усиления амплитуды очевидным.</span><span class="sxs-lookup"><span data-stu-id="76fb2-105">Represents an oracle for oblivious amplitude amplification.</span></span>

<span data-ttu-id="76fb2-106">Входные данные для Oracle $O $:</span><span class="sxs-lookup"><span data-stu-id="76fb2-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="76fb2-107">АнЦилла Register $a $, с которым $O $ работает.</span><span class="sxs-lookup"><span data-stu-id="76fb2-107">The ancilla register $a$ that $O$ acts on.</span></span>
- <span data-ttu-id="76fb2-108">Системная регистрация $s $, к которой применяется требуемая единая $U $, после выбора зарегистрировать $a $ в состоянии $ \кет{т} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="76fb2-108">The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.</span></span>

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="76fb2-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="76fb2-109">Remarks</span></span>

<span data-ttu-id="76fb2-110">Эта база данных Oracle, определенная $ $ О\кет {s} \_ а\кет {\ PSI} \_ s = \Ламбда\кет{т} \_ a U \кет{\пси} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет{т ^ \перп} \_ а\кдотс $ $, действует в анЦилла состоянии $ \кет{с} \_ a $ для реализации единой $U $ в любом состоянии системы $ \кет{\пси} \_ s $ с амплитудой $ \lambda $ в основе, помеченной $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="76fb2-110">This oracle defined by $$ O\ket{s}\_a\ket{\psi}\_s= \lambda\ket{t}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{t^\perp}\_a\cdots $$ acts on the ancilla state $\ket{s}\_a$ to implement the unitary $U$ on any system state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{t}\_a$.</span></span>
<span data-ttu-id="76fb2-111">Первый параметр — кубит регистр $ \кет{с} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="76fb2-111">The first parameter is the qubit register of $\ket{s}\_a$.</span></span> <span data-ttu-id="76fb2-112">Вторым параметром является кубит регистр $ \кет{\пси} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="76fb2-112">The second parameter is the qubit register of $\ket{\psi}\_s$.</span></span>