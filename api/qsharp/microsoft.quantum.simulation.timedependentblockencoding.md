---
uid: Microsoft.Quantum.Simulation.TimeDependentBlockEncoding
title: Определяемый пользователем тип Тимедепендентблоккенкодинг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentBlockEncoding
qsharp.summary: >-
  Represents a `BlockEncoding` that is controlled by a clock register.

  That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k. \end{align} $$.
ms.openlocfilehash: e2b191a4fc44f99c88f25da9b1ee6460d936740b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814260"
---
# <a name="timedependentblockencoding-user-defined-type"></a><span data-ttu-id="d74ee-102">Определяемый пользователем тип Тимедепендентблоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="d74ee-102">TimeDependentBlockEncoding user defined type</span></span>

<span data-ttu-id="d74ee-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d74ee-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d74ee-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d74ee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d74ee-105">Представляет объект `BlockEncoding` , который управляется регистром часов.</span><span class="sxs-lookup"><span data-stu-id="d74ee-105">Represents a `BlockEncoding` that is controlled by a clock register.</span></span>

<span data-ttu-id="d74ee-106">То есть, `TimeDependentBlockEncoding` представляет собой единое $U $, управляемое состоянием $ \кет{к} _d $ в регистре часов `d` таким образом, что произвольный оператор $H _k $, который действует на системный регистр, `s` кодируется в верхнем левом блоке, соответствующем вспомогательному состоянию $ \кет {0} _A $.</span><span class="sxs-lookup"><span data-stu-id="d74ee-106">That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="d74ee-107">Это означает следующее:</span><span class="sxs-lookup"><span data-stu-id="d74ee-107">That is,</span></span>

<span data-ttu-id="d74ee-108">$ $ \бегин{алигн} (\бра {0} \_ а\отимес I_ {DS}) U (\кет {0} \_ а\отимес I_ {DS}) = \ sum_ {k} \кет{к}\бра{к} \_ д\отимес H_k.</span><span class="sxs-lookup"><span data-stu-id="d74ee-108">$$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k.</span></span>
<span data-ttu-id="d74ee-109">\енд{алигн} $ $.</span><span class="sxs-lookup"><span data-stu-id="d74ee-109">\end{align} $$.</span></span>

```qsharp

newtype TimeDependentBlockEncoding = (((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

