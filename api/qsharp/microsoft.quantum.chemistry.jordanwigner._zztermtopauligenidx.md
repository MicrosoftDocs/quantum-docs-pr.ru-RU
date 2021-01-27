---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZZTermToPauliGenIdx
title: Функция _ZZTermToPauliGenIdx
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 0bbb0325406767f9d27e317ccc306f1fe77d00f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839063"
---
# <a name="_zztermtopauligenidx-function"></a><span data-ttu-id="ec52a-102">Функция _ZZTermToPauliGenIdx</span><span class="sxs-lookup"><span data-stu-id="ec52a-102">_ZZTermToPauliGenIdx function</span></span>

<span data-ttu-id="ec52a-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="ec52a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="ec52a-104">Пакет: [Microsoft. тактов. Химия](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ec52a-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="ec52a-105">Преобразует Женераториндекс, описывающий терм ZZ, в выражение "Женераториндекс []" с точки зрения пол.</span><span class="sxs-lookup"><span data-stu-id="ec52a-105">Converts a GeneratorIndex describing a ZZ term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="ec52a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="ec52a-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="ec52a-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ec52a-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ec52a-108">`GeneratorIndex` представление Терма ZZ.</span><span class="sxs-lookup"><span data-stu-id="ec52a-108">`GeneratorIndex` representing a ZZ term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="ec52a-109">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="ec52a-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="ec52a-110">"Женераториндекс []" выражение ZZ в качестве Паулиных терминов.</span><span class="sxs-lookup"><span data-stu-id="ec52a-110">'GeneratorIndex[]' expressing ZZ term as Pauli terms.</span></span>