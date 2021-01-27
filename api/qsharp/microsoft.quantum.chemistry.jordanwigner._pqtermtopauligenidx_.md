---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliGenIdx_
title: Функция _пктермтопаулиженидкс_
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliGenIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 046b3b7b78cee7f046607277896100e20c33a32d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839312"
---
# <a name="_pqtermtopauligenidx_-function"></a><span data-ttu-id="bec34-102">Функция _пктермтопаулиженидкс_</span><span class="sxs-lookup"><span data-stu-id="bec34-102">_PQTermToPauliGenIdx_ function</span></span>

<span data-ttu-id="bec34-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="bec34-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="bec34-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="bec34-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="bec34-105">Преобразует Женераториндекс, описывающий термин PQ, в выражение "Женераториндекс []" с точки зрения пол.</span><span class="sxs-lookup"><span data-stu-id="bec34-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliGenIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="bec34-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="bec34-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="bec34-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="bec34-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="bec34-108">`GeneratorIndex` представляет термин PQ.</span><span class="sxs-lookup"><span data-stu-id="bec34-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="bec34-109">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="bec34-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="bec34-110">"Женераториндекс []" выражает PQ термин в качестве Паулиных терминов.</span><span class="sxs-lookup"><span data-stu-id="bec34-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>