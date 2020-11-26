---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Функция Троттерстепсизе
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: aa5b63e058e1ea726b0d4c6eca73078831daaf3b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204697"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="a7066-102">Функция Троттерстепсизе</span><span class="sxs-lookup"><span data-stu-id="a7066-102">TrotterStepSize function</span></span>

<span data-ttu-id="a7066-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a7066-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a7066-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a7066-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a7066-105">Вычисление размера шага Троттер в рекурсивной реализации алгоритма моделирования Троттер.</span><span class="sxs-lookup"><span data-stu-id="a7066-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="a7066-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="a7066-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="a7066-107">порядок: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a7066-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="a7066-108">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a7066-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="a7066-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7066-109">Remarks</span></span>

<span data-ttu-id="a7066-110">В этой операции используется другое соглашение об индексировании, чем в [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="a7066-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="a7066-111">В частности, `DecomposedIntoTimeStepsCA(_, 4)` соответствует скалярному $p _2 (\ламбда) $ в Куант-pH/0508139.</span><span class="sxs-lookup"><span data-stu-id="a7066-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>