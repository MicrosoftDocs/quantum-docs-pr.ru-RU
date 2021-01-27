---
uid: Microsoft.Quantum.Chemistry.JordanWigner._PQTermToPauliMajIdx_
title: Функция _пктермтопаулимажидкс_
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _PQTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: edb9302e04de2abc6dfa9da0da27504f776e721f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839284"
---
# <a name="_pqtermtopaulimajidx_-function"></a><span data-ttu-id="7ba4b-102">Функция _пктермтопаулимажидкс_</span><span class="sxs-lookup"><span data-stu-id="7ba4b-102">_PQTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="7ba4b-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="7ba4b-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="7ba4b-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="7ba4b-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="7ba4b-105">Преобразует Женераториндекс, описывающий термин PQ, в выражение "Женераториндекс []" с точки зрения пол.</span><span class="sxs-lookup"><span data-stu-id="7ba4b-105">Converts a GeneratorIndex describing a PQ term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _PQTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="7ba4b-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="7ba4b-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="7ba4b-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="7ba4b-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="7ba4b-108">`GeneratorIndex` представляет термин PQ.</span><span class="sxs-lookup"><span data-stu-id="7ba4b-108">`GeneratorIndex` representing a PQ term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="7ba4b-109">Выходные данные: [оптимизедбетерминдекс](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="7ba4b-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="7ba4b-110">"Женераториндекс []" выражает PQ термин в качестве Паулиных терминов.</span><span class="sxs-lookup"><span data-stu-id="7ba4b-110">'GeneratorIndex[]' expressing PQ term as Pauli terms.</span></span>