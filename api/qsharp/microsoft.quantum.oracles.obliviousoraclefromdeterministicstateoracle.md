---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Функция Обливиаусораклефромдетерминистикстатеоракле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 9e18776ad4d6adf0068213117c6d1d8ed5c5f126
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732201"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="fd3ec-102">Функция Обливиаусораклефромдетерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="fd3ec-102">ObliviousOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="fd3ec-103">Пространство имен: [Microsoft. такт. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="fd3ec-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="fd3ec-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fd3ec-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fd3ec-105">Объединяет Oracle `DeterministicStateOracle` и `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="fd3ec-105">Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.</span></span>

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a><span data-ttu-id="fd3ec-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="fd3ec-106">Input</span></span>

### <a name="ancillaoracle--deterministicstateoracle"></a><span data-ttu-id="fd3ec-107">АнЦиллаоракле: [детерминистикстатеоракле](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="fd3ec-107">ancillaOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="fd3ec-108">Подготовка состояния Oracle $A $ типа, `DeterministicStateOracle` действующего на register $a $.</span><span class="sxs-lookup"><span data-stu-id="fd3ec-108">A state preparation oracle $A$ of type `DeterministicStateOracle` acting on register $a$.</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="fd3ec-109">Сигналоракле: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="fd3ec-109">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="fd3ec-110">Тип Oracle $U $ of `ObliviousOracle` , который взаимодействует с register $a, s $.</span><span class="sxs-lookup"><span data-stu-id="fd3ec-110">A oracle $U$ of type `ObliviousOracle` acting jointly on register $a,s$.</span></span>



## <a name="output--obliviousoracle"></a><span data-ttu-id="fd3ec-111">Выходные данные: [обливиаусоракле](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="fd3ec-111">Output : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="fd3ec-112">Oracle $O = UA $ of Type `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="fd3ec-112">An oracle $O=UA$ of type `ObliviousOracle`.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd3ec-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="fd3ec-113">See Also</span></span>

- [<span data-ttu-id="fd3ec-114">Microsoft. тактов. Oracle. Детерминистикстатеоракле</span><span class="sxs-lookup"><span data-stu-id="fd3ec-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="fd3ec-115">Microsoft. тактов. Oracle. Обливиаусоракле</span><span class="sxs-lookup"><span data-stu-id="fd3ec-115">Microsoft.Quantum.Oracles.ObliviousOracle</span></span>](xref:Microsoft.Quantum.Oracles.ObliviousOracle)