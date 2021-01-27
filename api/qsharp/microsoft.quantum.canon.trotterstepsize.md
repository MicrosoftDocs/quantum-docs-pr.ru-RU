---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Функция Троттерстепсизе
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: c7b6432645dcad2bd47c62b91e04e0b42cd04ca9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840070"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="aed7a-102">Функция Троттерстепсизе</span><span class="sxs-lookup"><span data-stu-id="aed7a-102">TrotterStepSize function</span></span>

<span data-ttu-id="aed7a-103">Пространство имен: [Microsoft. тактов. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aed7a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aed7a-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aed7a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aed7a-105">Вычисление размера шага Троттер в рекурсивной реализации алгоритма моделирования Троттер.</span><span class="sxs-lookup"><span data-stu-id="aed7a-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="aed7a-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="aed7a-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="aed7a-107">порядок: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aed7a-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="aed7a-108">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="aed7a-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="aed7a-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="aed7a-109">Remarks</span></span>

<span data-ttu-id="aed7a-110">В этой операции используется другое соглашение об индексировании, чем в [Куант-pH/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="aed7a-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="aed7a-111">В частности, `DecomposedIntoTimeStepsCA(_, 4)` соответствует скалярному $p _2 (\ламбда) $ в Куант-pH/0508139.</span><span class="sxs-lookup"><span data-stu-id="aed7a-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>