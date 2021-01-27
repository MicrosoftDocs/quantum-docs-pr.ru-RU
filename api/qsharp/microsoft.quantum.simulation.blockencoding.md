---
uid: Microsoft.Quantum.Simulation.BlockEncoding
title: Определяемый пользователем тип Блоккенкодинг
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: BlockEncoding
qsharp.summary: >-
  Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.

  That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$. That is,

  $$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.
ms.openlocfilehash: 70cd18f04cbd449f4818ba3b40580303137f84db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857633"
---
# <a name="blockencoding-user-defined-type"></a><span data-ttu-id="1562e-102">Определяемый пользователем тип Блоккенкодинг</span><span class="sxs-lookup"><span data-stu-id="1562e-102">BlockEncoding user defined type</span></span>

<span data-ttu-id="1562e-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1562e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1562e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1562e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1562e-105">Представляет собой единое место кодирования произвольного оператора в верхнем левом блоке.</span><span class="sxs-lookup"><span data-stu-id="1562e-105">Represents a unitary where an arbitrary operator of interest is encoded in the top-left block.</span></span>

<span data-ttu-id="1562e-106">То есть, `BlockEncoding` представляет собой единое $U $, где произвольный оператор $H $, который действует на системный регистр, `s` кодируется в верхнем левом блоке, соответствующем вспомогательному состоянию $ \кет {0} _A $.</span><span class="sxs-lookup"><span data-stu-id="1562e-106">That is, a `BlockEncoding` is a unitary $U$ where an arbitrary operator $H$ of interest that acts on the system register `s` is encoded in the top- left block corresponding to auxiliary state $\ket{0}_a$.</span></span> <span data-ttu-id="1562e-107">Это означает следующее:</span><span class="sxs-lookup"><span data-stu-id="1562e-107">That is,</span></span>

<span data-ttu-id="1562e-108">$ $ \бегин{алигн} (\бра {0} _A \отимес I_s) U (\кет {0} _a \отимес I_s) = H \енд{алигн} $ $.</span><span class="sxs-lookup"><span data-stu-id="1562e-108">$$ \begin{align} (\bra{0}_a\otimes I_s)U(\ket{0}_a\otimes I_s) = H \end{align} $$.</span></span>

```qsharp

newtype BlockEncoding = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```

