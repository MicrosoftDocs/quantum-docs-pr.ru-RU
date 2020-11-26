---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Функция Трустаблесфромпермутатионфолдер
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 86e112782825303805029b2f9f6cfd9d6ce9e8b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231030"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="66dd1-102">Функция Трустаблесфромпермутатионфолдер</span><span class="sxs-lookup"><span data-stu-id="66dd1-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="66dd1-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="66dd1-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="66dd1-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66dd1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66dd1-105">Логика декомпозиции для одного индекса переменной</span><span class="sxs-lookup"><span data-stu-id="66dd1-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="66dd1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="66dd1-106">Description</span></span>

<span data-ttu-id="66dd1-107">Это принимает текущее состояние и создает обновленную перестановку и, возможно, добавляет новые функции для контролируемых шлюзов.</span><span class="sxs-lookup"><span data-stu-id="66dd1-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="66dd1-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="66dd1-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="66dd1-109">Нумварс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="66dd1-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="66dd1-110">состояние: [декомпоситионстате](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="66dd1-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="66dd1-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="66dd1-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="66dd1-112">Выходные данные: [декомпоситионстате](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="66dd1-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>

