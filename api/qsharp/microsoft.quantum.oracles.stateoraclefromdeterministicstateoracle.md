---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Функция Статеораклефромдетерминистикстатеоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733344"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="c2d31-102">Функция Статеораклефромдетерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="c2d31-102">StateOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="c2d31-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="c2d31-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="c2d31-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c2d31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c2d31-105">Преобразует Oracle типа `DeterministicStateOracle` в `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="c2d31-105">Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.</span></span>

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a><span data-ttu-id="c2d31-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="c2d31-106">Input</span></span>

### <a name="deterministicstateoracle--deterministicstateoracle"></a><span data-ttu-id="c2d31-107">Детерминистикстатеоракле: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="c2d31-107">deterministicStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="c2d31-108">Подготовка состояния Oracle $A $ типа `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="c2d31-108">A state preparation oracle $A$ of type `DeterministicStateOracle`.</span></span>



## <a name="output--stateoracle"></a><span data-ttu-id="c2d31-109">Выходные данные: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="c2d31-109">Output : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="c2d31-110">То же состояние подготовки Oracle $A $, но теперь типа `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="c2d31-110">The same state preparation oracle $A$, but now of type `StateOracle`.</span></span> <span data-ttu-id="c2d31-111">Обратите внимание, что индекс флага в этом `StateOracle` случае является фиктивной переменной и не имеет результата.</span><span class="sxs-lookup"><span data-stu-id="c2d31-111">Note that the flag index in this `StateOracle` is a dummy variable and has no effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2d31-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="c2d31-112">See Also</span></span>

- [<span data-ttu-id="c2d31-113">Microsoft. тактов. Oracle. Детерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="c2d31-113">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="c2d31-114">Microsoft. тактов. Oracle. Статеоракле</span><span class="sxs-lookup"><span data-stu-id="c2d31-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)