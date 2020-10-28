---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Функция Нмисклассификатионс
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 9e356d68233519978e007e5a2999ca1be8cb7f83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709741"
---
# <a name="nmisclassifications-function"></a><span data-ttu-id="34657-102">Функция Нмисклассификатионс</span><span class="sxs-lookup"><span data-stu-id="34657-102">NMisclassifications function</span></span>

<span data-ttu-id="34657-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="34657-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="34657-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34657-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34657-105">При наличии набора выводимых меток и набора правильных меток возвращает количество индексов, в которых каждый набор меток различается.</span><span class="sxs-lookup"><span data-stu-id="34657-105">Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.</span></span>

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a><span data-ttu-id="34657-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="34657-106">Input</span></span>

### <a name="proposed--int"></a><span data-ttu-id="34657-107">предложено: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="34657-107">proposed : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="actual--int"></a><span data-ttu-id="34657-108">фактическое: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="34657-108">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--int"></a><span data-ttu-id="34657-109">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="34657-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="34657-110">Количество индексов `idx` таким, что `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="34657-110">The number of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>