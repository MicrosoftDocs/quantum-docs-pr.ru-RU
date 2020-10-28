---
uid: Microsoft.Quantum.Simulation._MultiplyGeneratorSystem
title: Функция _MultiplyGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: e59700917d45f1613bbc7983bda262d3b956e2f5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92710666"
---
# <a name="_multiplygeneratorsystem-function"></a><span data-ttu-id="2b8f5-102">Функция _MultiplyGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="2b8f5-102">_MultiplyGeneratorSystem function</span></span>

<span data-ttu-id="2b8f5-103">Пространство имен: [Microsoft. тактов. Моделирование](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="2b8f5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="2b8f5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2b8f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2b8f5-105">Умножает коэффициент всех терминов в `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="2b8f5-105">Multiplies the coefficient of all terms in a `GeneratorSystem`.</span></span>

```qsharp
function _MultiplyGeneratorSystem (multiplier : Double, idxTerm : Int, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="2b8f5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2b8f5-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="2b8f5-107">множитель: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2b8f5-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="idxterm--int"></a><span data-ttu-id="2b8f5-108">Идкстерм: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2b8f5-108">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="2b8f5-109">Женераторсистем: [женераторсистем](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="2b8f5-109">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>





## <a name="output--generatorindex"></a><span data-ttu-id="2b8f5-110">Выходные данные: [женераториндекс](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="2b8f5-110">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>



## <a name="remarks"></a><span data-ttu-id="2b8f5-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="2b8f5-111">Remarks</span></span>

<span data-ttu-id="2b8f5-112">Это промежуточный шаг, и его не следует вызывать.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-112">This is an intermediate step and should not be called.</span></span>