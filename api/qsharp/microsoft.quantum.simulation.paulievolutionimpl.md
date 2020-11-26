---
uid: Microsoft.Quantum.Simulation.PauliEvolutionImpl
title: Операция Паулиеволутионимпл
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.

  See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 868f3eef187e8e993127cfcab21e1574583ac845
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229143"
---
# <a name="paulievolutionimpl-operation"></a><span data-ttu-id="cad5e-102">Операция Паулиеволутионимпл</span><span class="sxs-lookup"><span data-stu-id="cad5e-102">PauliEvolutionImpl operation</span></span>

<span data-ttu-id="cad5e-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="cad5e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="cad5e-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cad5e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cad5e-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Паули.</span><span class="sxs-lookup"><span data-stu-id="cad5e-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

<span data-ttu-id="cad5e-106">Дополнительные сведения см. в разделе [динамическое моделирование генератора](/quantum/libraries/data-structures#dynamical-generator-modeling) .</span><span class="sxs-lookup"><span data-stu-id="cad5e-106">See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation PauliEvolutionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, delta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cad5e-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="cad5e-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="cad5e-108">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="cad5e-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="cad5e-109">Индекс генератора, который должен быть представлен как единое развитие на основе Паули.</span><span class="sxs-lookup"><span data-stu-id="cad5e-109">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>


### <a name="delta--double"></a><span data-ttu-id="cad5e-110">Дельта: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cad5e-110">delta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cad5e-111">Множитель на протяжении времени — развитие термина, на который ссылается `generatorIndex` .</span><span class="sxs-lookup"><span data-stu-id="cad5e-111">A multiplier on the duration of time-evolution by the term referenced in `generatorIndex`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="cad5e-112">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cad5e-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cad5e-113">Зарегистрируйте обоснованный оператор по времени.</span><span class="sxs-lookup"><span data-stu-id="cad5e-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cad5e-114">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cad5e-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

