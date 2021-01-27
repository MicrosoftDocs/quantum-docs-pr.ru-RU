---
uid: Microsoft.Quantum.Oracles.ReflectionOracleFromDeterministicStateOracle
title: Функция Рефлектионораклефромдетерминистикстатеоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ReflectionOracleFromDeterministicStateOracle
qsharp.summary: Constructs reflection about a given state from an oracle.
ms.openlocfilehash: c260bdbcdb2ce53ad602bf84e0d31ef4fec24a79
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842525"
---
# <a name="reflectionoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="a4112-102">Функция Рефлектионораклефромдетерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="a4112-102">ReflectionOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="a4112-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="a4112-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="a4112-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4112-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4112-105">Конструирует отражение о заданном состоянии из Oracle.</span><span class="sxs-lookup"><span data-stu-id="a4112-105">Constructs reflection about a given state from an oracle.</span></span>

```qsharp
function ReflectionOracleFromDeterministicStateOracle (oracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.ReflectionOracle
```


## <a name="description"></a><span data-ttu-id="a4112-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a4112-106">Description</span></span>

<span data-ttu-id="a4112-107">Учитывая детерминированное состояние подготовка Oracle, представленная единой матрицей $O $, результатом этой функции является Oracle, который применяет отражение состояния $ \кет{\пси} $, подготовленного Oracle $O $; то есть, состояние $ \кет{\пси} $, например, $O \кет {0} = \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="a4112-107">Given a deterministic state preparation oracle represented by a unitary matrix $O$, the result of this function is an oracle that applies a reflection around the state $\ket{\psi}$ prepared by the oracle $O$; that is, the state $\ket{\psi}$ such that $O\ket{0} = \ket{\psi}$.</span></span>

## <a name="input"></a><span data-ttu-id="a4112-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a4112-108">Input</span></span>

### <a name="oracle--deterministicstateoracle"></a><span data-ttu-id="a4112-109">Oracle: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="a4112-109">oracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="a4112-110">Объект Oracle, подготавливающий копии состояния $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="a4112-110">An oracle that prepares copies of the state $\ket{\psi}$.</span></span>



## <a name="output--reflectionoracle"></a><span data-ttu-id="a4112-111">Выходные данные: [рефлектионоракле](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="a4112-111">Output : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="a4112-112">База данных Oracle, отражающая состояние $ \кет{\пси} $.</span><span class="sxs-lookup"><span data-stu-id="a4112-112">An oracle that reflects about the state $\ket{\psi}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4112-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="a4112-113">See Also</span></span>

- [<span data-ttu-id="a4112-114">Microsoft. тактов. Oracle. Детерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="a4112-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="a4112-115">Microsoft. тактов. Oracle. Рефлектионоракле</span><span class="sxs-lookup"><span data-stu-id="a4112-115">Microsoft.Quantum.Oracles.ReflectionOracle</span></span>](xref:Microsoft.Quantum.Oracles.ReflectionOracle)