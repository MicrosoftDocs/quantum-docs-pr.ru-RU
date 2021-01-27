---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Функция Трустаблесфромпермутатионфолдер
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 881bb8e29d3d7761cc521837502ea79b0714b381
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855254"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="601f6-102">Функция Трустаблесфромпермутатионфолдер</span><span class="sxs-lookup"><span data-stu-id="601f6-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="601f6-103">Пространство имен: [Microsoft. тактов. синтез](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="601f6-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="601f6-104">Пакет: [Microsoft. такт. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="601f6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="601f6-105">Логика декомпозиции для одного индекса переменной</span><span class="sxs-lookup"><span data-stu-id="601f6-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="601f6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="601f6-106">Description</span></span>

<span data-ttu-id="601f6-107">Это принимает текущее состояние и создает обновленную перестановку и, возможно, добавляет новые функции для контролируемых шлюзов.</span><span class="sxs-lookup"><span data-stu-id="601f6-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="601f6-108">Входные данные</span><span class="sxs-lookup"><span data-stu-id="601f6-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="601f6-109">Нумварс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="601f6-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="601f6-110">состояние: [декомпоситионстате](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="601f6-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="601f6-111">Индекс: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="601f6-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="601f6-112">Выходные данные: [декомпоситионстате](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="601f6-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>

