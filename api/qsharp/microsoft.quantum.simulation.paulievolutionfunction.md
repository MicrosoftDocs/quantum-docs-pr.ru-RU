---
uid: Microsoft.Quantum.Simulation.PauliEvolutionFunction
title: Функция Паулиеволутионфунктион
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 060f4e4f23bb8b47518a3a22bbca8ab0be6e13b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92730904"
---
# <a name="paulievolutionfunction-function"></a><span data-ttu-id="58cbb-102">Функция Паулиеволутионфунктион</span><span class="sxs-lookup"><span data-stu-id="58cbb-102">PauliEvolutionFunction function</span></span>

<span data-ttu-id="58cbb-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="58cbb-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="58cbb-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58cbb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58cbb-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Паули.</span><span class="sxs-lookup"><span data-stu-id="58cbb-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="58cbb-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="58cbb-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="58cbb-107">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="58cbb-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="58cbb-108">Индекс генератора, который должен быть представлен как единое развитие на основе Паули.</span><span class="sxs-lookup"><span data-stu-id="58cbb-108">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="58cbb-109">Выходные данные: [еволутионунитари](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="58cbb-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="58cbb-110">`EvolutionUnitary`Представление, представляющее время развития термина, на который ссылается "женераториндекс.</span><span class="sxs-lookup"><span data-stu-id="58cbb-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>