---
uid: Microsoft.Quantum.Simulation.TimeDependentBlockEncoding
title: Определяемый пользователем тип Тимедепендентблоккенкодинг
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentBlockEncoding
qsharp.summary: >-
  Represents a `BlockEncoding` that is controlled by a clock register.

  That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k. \end{align} $$.
ms.openlocfilehash: 1cb3a3cf1e16b194eebd1574da6f9934fc34e5f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92734224"
---
# <a name="timedependentblockencoding-user-defined-type"></a><span data-ttu-id="d9370-102">Определяемый пользователем тип Тимедепендентблоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="d9370-102">TimeDependentBlockEncoding user defined type</span></span>

<span data-ttu-id="d9370-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d9370-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d9370-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d9370-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d9370-105">Представляет объект `BlockEncoding` , который управляется регистром часов.</span><span class="sxs-lookup"><span data-stu-id="d9370-105">Represents a `BlockEncoding` that is controlled by a clock register.</span></span>

<span data-ttu-id="d9370-106">То есть, `TimeDependentBlockEncoding` представляет собой единое $U $, управляемое состоянием $ \кет{к} _d $ в регистре часов `d` таким образом, что произвольный оператор $H _k $, который действует на системный регистр, `s` кодируется в верхнем левом блоке, соответствующем вспомогательному состоянию $ \кет {0} _A $.</span><span class="sxs-lookup"><span data-stu-id="d9370-106">That is, a `TimeDependentBlockEncoding` is a unitary $U$ controlled by a state $\ket{k}_d$ in clock register `d` such that an arbitrary operator $H_k$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="d9370-107">Это означает следующее:</span><span class="sxs-lookup"><span data-stu-id="d9370-107">That is,</span></span>

<span data-ttu-id="d9370-108">$ $ \бегин{алигн} (\бра {0} \_ а\отимес I_ {DS}) U (\кет {0} \_ а\отимес I_ {DS}) = \ sum_ {k} \кет{к}\бра{к} \_ д\отимес H_k.</span><span class="sxs-lookup"><span data-stu-id="d9370-108">$$ \begin{align} (\bra{0}\_a\otimes I_{ds})U(\ket{0}\_a\otimes I_{ds}) = \sum_{k}\ket{k}\bra{k}\_d\otimes H_k.</span></span>
<span data-ttu-id="d9370-109">\енд{алигн} $ $.</span><span class="sxs-lookup"><span data-stu-id="d9370-109">\end{align} $$.</span></span>

```qsharp

newtype TimeDependentBlockEncoding = (((Qubit[], Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

