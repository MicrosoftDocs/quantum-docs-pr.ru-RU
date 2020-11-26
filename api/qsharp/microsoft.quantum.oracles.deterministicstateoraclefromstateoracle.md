---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Функция Детерминистикстатеораклефромстатеоракле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 183b1108ead6239e26bb0b38144cb9374e7bf285
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226763"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="4e9ae-102">Функция Детерминистикстатеораклефромстатеоракле</span><span class="sxs-lookup"><span data-stu-id="4e9ae-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="4e9ae-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="4e9ae-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="4e9ae-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4e9ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4e9ae-105">Преобразует Oracle типа `StateOracle` в `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="4e9ae-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="4e9ae-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="4e9ae-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="4e9ae-107">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4e9ae-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4e9ae-108">Индекс для флага `stateOracle` $A кубит $, который явно работает с двумя регистрами: флаг $f $ и system $s $, например $A \кет {0} \_ ф\кет {\ PSI} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="4e9ae-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="4e9ae-109">Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="4e9ae-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="4e9ae-110">Подготовка состояния Oracle $A $ типа `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="4e9ae-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="4e9ae-111">Выходные данные: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="4e9ae-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="4e9ae-112">Одно и то же состояние подготовленная база данных Oracle $A $, но теперь `DeterministicStateOracle` имеет тип, поэтому он работает с регистром, где $a, s $ больше не разделяются явным образом, например  $A \ket{0\psi} \_ {as} $.</span><span class="sxs-lookup"><span data-stu-id="4e9ae-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e9ae-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="4e9ae-113">See Also</span></span>

- [<span data-ttu-id="4e9ae-114">Microsoft. тактов. Oracle. Статеоракле</span><span class="sxs-lookup"><span data-stu-id="4e9ae-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="4e9ae-115">Microsoft. тактов. Oracle. Детерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="4e9ae-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)