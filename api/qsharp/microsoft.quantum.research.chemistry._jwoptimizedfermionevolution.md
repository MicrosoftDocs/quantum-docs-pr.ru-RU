---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedFermionEvolution
title: _JWOptimizedFermionEvolution операция
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedFermionEvolution
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 5976b65d44c0e8597088dbaa6b85ffde634edcdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92732529"
---
# <a name="_jwoptimizedfermionevolution-operation"></a><span data-ttu-id="392c8-102">_JWOptimizedFermionEvolution операция</span><span class="sxs-lookup"><span data-stu-id="392c8-102">_JWOptimizedFermionEvolution operation</span></span>

<span data-ttu-id="392c8-103">Пространство имен: [Microsoft. тактов. Research. Химия](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="392c8-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="392c8-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="392c8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="392c8-105">Представляет динамический генератор как набор моделирующих шлюзов и расширение на основе Жвоптимизед.</span><span class="sxs-lookup"><span data-stu-id="392c8-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

<span data-ttu-id="392c8-106">Дополнительные сведения см. в разделе [динамическое моделирование генератора](../libraries/data-structures#dynamical-generator-modeling) .</span><span class="sxs-lookup"><span data-stu-id="392c8-106">See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation _JWOptimizedFermionEvolution (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="392c8-107">Входные данные</span><span class="sxs-lookup"><span data-stu-id="392c8-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="392c8-108">Женераториндекс: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="392c8-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="392c8-109">Индекс генератора, который должен быть представлен как единое развитие на основе Жвоптимизед.</span><span class="sxs-lookup"><span data-stu-id="392c8-109">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="392c8-110">Степсизе: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="392c8-110">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="392c8-111">Множитель на протяжении времени — развитие термина, на который ссылается `generatorIndex` .</span><span class="sxs-lookup"><span data-stu-id="392c8-111">A multiplier on the duration of time-evolution by the term referenced in `generatorIndex`.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="392c8-112">Паритикубит: [кубит](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="392c8-112">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="392c8-113">Кубит, определяющий знак времени — развитие.</span><span class="sxs-lookup"><span data-stu-id="392c8-113">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="392c8-114">Кубитс: [кубит](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="392c8-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="392c8-115">Зарегистрируйте обоснованный оператор по времени.</span><span class="sxs-lookup"><span data-stu-id="392c8-115">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="392c8-116">Выходные данные: [единица измерения](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="392c8-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

