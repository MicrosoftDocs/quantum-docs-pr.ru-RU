---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Функция Троттерстепсизе
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: fabfbff74572b3c96c701de5443e4265a0468d78
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92715229"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="faed4-102">Функция Троттерстепсизе</span><span class="sxs-lookup"><span data-stu-id="faed4-102">TrotterStepSize function</span></span>

<span data-ttu-id="faed4-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="faed4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="faed4-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="faed4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="faed4-105">Вычисление размера шага Троттер в рекурсивной реализации алгоритма моделирования Троттер.</span><span class="sxs-lookup"><span data-stu-id="faed4-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="faed4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="faed4-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="faed4-107">порядок: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="faed4-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="faed4-108">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="faed4-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="faed4-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="faed4-109">Remarks</span></span>

<span data-ttu-id="faed4-110">В этой операции используется другое соглашение об индексировании, чем в [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="faed4-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="faed4-111">В частности, `DecomposedIntoTimeStepsCA(_, 4)` соответствует скалярному $p _2 (\ламбда) $ в Куант-pH/0508139.</span><span class="sxs-lookup"><span data-stu-id="faed4-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>