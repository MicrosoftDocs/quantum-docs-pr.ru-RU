---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliGenIdx
title: Функция _ZTermToPauliGenIdx
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 1569ec742778549b8754cdca8b2d9872310e8976
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92714179"
---
# <a name="_ztermtopauligenidx-function"></a><span data-ttu-id="17b23-102">Функция _ZTermToPauliGenIdx</span><span class="sxs-lookup"><span data-stu-id="17b23-102">_ZTermToPauliGenIdx function</span></span>

<span data-ttu-id="17b23-103">Пространство имен: [Microsoft. тактов. химия. жорданвигнер](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="17b23-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="17b23-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17b23-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="17b23-105">Преобразует Женераториндекс, описывающий термин Z, в выражение "Женераториндекс []" с точки зрения пол.</span><span class="sxs-lookup"><span data-stu-id="17b23-105">Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="17b23-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="17b23-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="17b23-107">термин: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="17b23-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="17b23-108">`GeneratorIndex` представление термина Z.</span><span class="sxs-lookup"><span data-stu-id="17b23-108">`GeneratorIndex` representing a Z term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="17b23-109">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="17b23-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="17b23-110">"Женераториндекс []" выражение Z в качестве термина Паули.</span><span class="sxs-lookup"><span data-stu-id="17b23-110">'GeneratorIndex[]' expressing Z term as Pauli terms.</span></span>