---
uid: Microsoft.Quantum.AmplitudeAmplification.AmpAmpByOracle
title: Функция Ампампбйоракле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmpAmpByOracle
qsharp.summary: >-
  > [!WARNING]

  > AmpAmpByOracle has been deprecated. Please use <xref:Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification> instead.

  >

  > Please use @"microsoft.quantum.amplitudeamplification.standardamplitudeamplification".
ms.openlocfilehash: 27775b35523522298cbca5d6d1e3c36ea24acf97
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844017"
---
# <a name="ampampbyoracle-function"></a><span data-ttu-id="d9bdd-102">Функция Ампампбйоракле</span><span class="sxs-lookup"><span data-stu-id="d9bdd-102">AmpAmpByOracle function</span></span>

<span data-ttu-id="d9bdd-103">Пространство имен: [Microsoft. тактов. амплитудеамплификатион](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="d9bdd-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="d9bdd-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d9bdd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="d9bdd-105">Ампампбйоракле является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-105">AmpAmpByOracle has been deprecated.</span></span> <span data-ttu-id="d9bdd-106">Взамен рекомендуется использовать <xref:Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification>.</span><span class="sxs-lookup"><span data-stu-id="d9bdd-106">Please use <xref:Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification> instead.</span></span>
>
> <span data-ttu-id="d9bdd-107">Используйте @"microsoft.quantum.amplitudeamplification.standardamplitudeamplification".</span><span class="sxs-lookup"><span data-stu-id="d9bdd-107">Please use @"microsoft.quantum.amplitudeamplification.standardamplitudeamplification".</span></span>



```qsharp
function AmpAmpByOracle (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="d9bdd-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d9bdd-108">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="d9bdd-109">Нитератионс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d9bdd-109">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="stateoracle--stateoracle"></a><span data-ttu-id="d9bdd-110">Статеоракле: [статеоракле](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="d9bdd-110">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>




### <a name="idxflagqubit--int"></a><span data-ttu-id="d9bdd-111">Идксфлагкубит: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d9bdd-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="d9bdd-112">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] = [единица измерения](xref:microsoft.quantum.lang-ref.unit)  ">" + CTL</span><span class="sxs-lookup"><span data-stu-id="d9bdd-112">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

