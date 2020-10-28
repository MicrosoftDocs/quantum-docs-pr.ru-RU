---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Функция Трустаблесфромпермутатионфолдер
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 6b00c9e880ed7b7b3bf446dcb17dab3bab7a83a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92733480"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="96814-102">Функция Трустаблесфромпермутатионфолдер</span><span class="sxs-lookup"><span data-stu-id="96814-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="96814-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="96814-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="96814-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="96814-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="96814-105">Логика декомпозиции для одного индекса переменной</span><span class="sxs-lookup"><span data-stu-id="96814-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="96814-106">Описание</span><span class="sxs-lookup"><span data-stu-id="96814-106">Description</span></span>

<span data-ttu-id="96814-107">Это принимает текущее состояние и создает обновленную перестановку и, возможно, добавляет новые функции для контролируемых шлюзов.</span><span class="sxs-lookup"><span data-stu-id="96814-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="96814-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="96814-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="96814-109">Нумварс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="96814-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="96814-110">состояние: [декомпоситионстате](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="96814-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="96814-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="96814-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="96814-112">Выходные данные: [декомпоситионстате](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="96814-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>

