---
uid: Microsoft.Quantum.Chemistry.JordanWigner._V0123TermToPauliMajIdx_
title: Функция _V0123TermToPauliMajIdx_
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _V0123TermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis
ms.openlocfilehash: 0c30e75714760fe50f876cfbc5bd1f9609226242
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839121"
---
# <a name="_v0123termtopaulimajidx_-function"></a><span data-ttu-id="2fc40-102">Функция _V0123TermToPauliMajIdx_</span><span class="sxs-lookup"><span data-stu-id="2fc40-102">_V0123TermToPauliMajIdx_ function</span></span>

<span data-ttu-id="2fc40-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="2fc40-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="2fc40-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="2fc40-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="2fc40-105">Преобразует Женераториндекс, описывающий термин ПКРС, в выражение "Женераториндекс []" с точки зрения пол.</span><span class="sxs-lookup"><span data-stu-id="2fc40-105">Converts a GeneratorIndex describing a PQRS term to an expression 'GeneratorIndex[]' in terms of Paulis</span></span>

```qsharp
function _V0123TermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex[]
```


## <a name="input"></a><span data-ttu-id="2fc40-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2fc40-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="2fc40-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="2fc40-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="2fc40-108">`GeneratorIndex` представляет термин ПКРС.</span><span class="sxs-lookup"><span data-stu-id="2fc40-108">`GeneratorIndex` representing a PQRS term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="2fc40-109">Выходные данные: [оптимизедбетерминдекс](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)[]</span><span class="sxs-lookup"><span data-stu-id="2fc40-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)[]</span></span>

<span data-ttu-id="2fc40-110">"Женераториндекс []" выражает ПКРС термин в качестве Паулиных терминов.</span><span class="sxs-lookup"><span data-stu-id="2fc40-110">'GeneratorIndex[]' expressing PQRS term as Pauli terms.</span></span>