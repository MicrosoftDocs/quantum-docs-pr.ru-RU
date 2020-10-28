---
uid: Microsoft.Quantum.Preparation._ApproximatelyUnprepareArbitraryStatePlan
title: Функция _ApproximatelyUnprepareArbitraryStatePlan
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: _ApproximatelyUnprepareArbitraryStatePlan
qsharp.summary: Implementation step of arbitrary state preparation procedure.
ms.openlocfilehash: 4050a65b0830da4c3d73e84942780aa7c2643c76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733336"
---
# <a name="_approximatelyunpreparearbitrarystateplan-function"></a><span data-ttu-id="b46d5-102">Функция _ApproximatelyUnprepareArbitraryStatePlan</span><span class="sxs-lookup"><span data-stu-id="b46d5-102">_ApproximatelyUnprepareArbitraryStatePlan function</span></span>

<span data-ttu-id="b46d5-103">Пространство имен: [Microsoft. тактов. Подготовка](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="b46d5-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="b46d5-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b46d5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b46d5-105">Этап реализации процедуры подготовки произвольного состояния.</span><span class="sxs-lookup"><span data-stu-id="b46d5-105">Implementation step of arbitrary state preparation procedure.</span></span>

```qsharp
function _ApproximatelyUnprepareArbitraryStatePlan (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], (rngControl : Range, idxTarget : Int)) : (Qubit[] => Unit is Adj + Ctl)[]
```


## <a name="input"></a><span data-ttu-id="b46d5-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b46d5-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="b46d5-107">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b46d5-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="coefficients--complexpolar"></a><span data-ttu-id="b46d5-108">коэффициенты: [комплексполар](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="b46d5-108">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>




### <a name="rngcontrol--range"></a><span data-ttu-id="b46d5-109">Рнгконтрол: [диапазон](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="b46d5-109">rngControl : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>




### <a name="idxtarget--int"></a><span data-ttu-id="b46d5-110">Идкстаржет: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b46d5-110">idxTarget : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="b46d5-111">Выходные данные: [кубит](xref:microsoft.quantum.lang-ref.qubit)[] => [модульные](xref:microsoft.quantum.lang-ref.unit) года + CTL []</span><span class="sxs-lookup"><span data-stu-id="b46d5-111">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>



## <a name="see-also"></a><span data-ttu-id="b46d5-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="b46d5-112">See Also</span></span>

- [<span data-ttu-id="b46d5-113">Microsoft. тактов. подготовка. Препареарбитраристате</span><span class="sxs-lookup"><span data-stu-id="b46d5-113">Microsoft.Quantum.Preparation.PrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.PrepareArbitraryState)
- [<span data-ttu-id="b46d5-114">Microsoft. тактов. Canon. Мултиплекспаули</span><span class="sxs-lookup"><span data-stu-id="b46d5-114">Microsoft.Quantum.Canon.MultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.MultiplexPauli)