---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Определяемый пользователем тип Обливиаусоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 793e72af56e288f9b437302f9958665e92e5e763
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842552"
---
# <a name="obliviousoracle-user-defined-type"></a><span data-ttu-id="1d392-102">Определяемый пользователем тип Обливиаусоракле</span><span class="sxs-lookup"><span data-stu-id="1d392-102">ObliviousOracle user defined type</span></span>

<span data-ttu-id="1d392-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="1d392-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="1d392-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d392-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d392-105">Представляет Oracle для усиления амплитуды очевидным.</span><span class="sxs-lookup"><span data-stu-id="1d392-105">Represents an oracle for oblivious amplitude amplification.</span></span>

<span data-ttu-id="1d392-106">Входные данные для Oracle $O $:</span><span class="sxs-lookup"><span data-stu-id="1d392-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="1d392-107">АнЦилла Register $a $, с которым $O $ работает.</span><span class="sxs-lookup"><span data-stu-id="1d392-107">The ancilla register $a$ that $O$ acts on.</span></span>
- <span data-ttu-id="1d392-108">Системная регистрация $s $, к которой применяется требуемая единая $U $, после выбора зарегистрировать $a $ в состоянии $ \кет{т} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="1d392-108">The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.</span></span>

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="1d392-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="1d392-109">Remarks</span></span>

<span data-ttu-id="1d392-110">Эта база данных Oracle, определенная $ $ О\кет {s} \_ а\кет {\ PSI} \_ s = \Ламбда\кет{т} \_ a U \кет{\пси} \_ s + \sqrt{1-| \ламбда | ^ 2} \кет{т ^ \перп} \_ а\кдотс $ $, действует в анЦилла состоянии $ \кет{с} \_ a $ для реализации единой $U $ в любом состоянии системы $ \кет{\пси} \_ s $ с амплитудой $ \lambda $ в основе, помеченной $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="1d392-110">This oracle defined by $$ O\ket{s}\_a\ket{\psi}\_s= \lambda\ket{t}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{t^\perp}\_a\cdots $$ acts on the ancilla state $\ket{s}\_a$ to implement the unitary $U$ on any system state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{t}\_a$.</span></span>
<span data-ttu-id="1d392-111">Первый параметр — кубит регистр $ \кет{с} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="1d392-111">The first parameter is the qubit register of $\ket{s}\_a$.</span></span> <span data-ttu-id="1d392-112">Вторым параметром является кубит регистр $ \кет{\пси} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="1d392-112">The second parameter is the qubit register of $\ket{\psi}\_s$.</span></span>