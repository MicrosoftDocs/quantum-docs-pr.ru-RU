---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Определяемый пользователем тип Блоккенкодинг
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 1b769c58fd23b4ebc9d779cec3c47d8275822e5a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732472"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="a128e-102">Определяемый пользователем тип Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="a128e-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="a128e-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a128e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a128e-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a128e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a128e-105">Представляет собой единое место кодирования произвольного оператора в верхнем левом блоке.</span><span class="sxs-lookup"><span data-stu-id="a128e-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="a128e-106">То есть, `BlockEncoding` представляет собой единое $U $, где произвольный оператор $H $, который действует на системный регистр, `s` кодируется в верхнем левом блоке, соответствующем вспомогательному состоянию $ \кет {0} _A $.</span><span class="sxs-lookup"><span data-stu-id="a128e-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="a128e-107">Это означает следующее:</span><span class="sxs-lookup"><span data-stu-id="a128e-107">That is,</span></span>

<span data-ttu-id="a128e-108">$ $ \бегин{алигн} (\бра {0} _A \отимес I_s) U (\кет {0} _a \отимес I_s) = H \енд{алигн} $ $.</span><span class="sxs-lookup"><span data-stu-id="a128e-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

