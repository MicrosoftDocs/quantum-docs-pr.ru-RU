---
uid: Microsoft.Quantum.MachineLearning._UpdatedBias
title: Функция _UpdatedBias
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _UpdatedBias
qsharp.summary: Returns a bias value that leads to near-minimum misclassification score.
ms.openlocfilehash: 41a51d8a6a8af299ce3e84b727336b098a3d1160
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844448"
---
# <a name="_updatedbias-function"></a><span data-ttu-id="2cbd4-102">Функция _UpdatedBias</span><span class="sxs-lookup"><span data-stu-id="2cbd4-102">_UpdatedBias function</span></span>

<span data-ttu-id="2cbd4-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2cbd4-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2cbd4-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2cbd4-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="2cbd4-105">Возвращает значение смещения, которое приводит к оценке почти минимальных ошибок классификации.</span><span class="sxs-lookup"><span data-stu-id="2cbd4-105">Returns a bias value that leads to near-minimum misclassification score.</span></span>

```qsharp
function _UpdatedBias (labeledProbabilities : (Double, Int)[], bias : Double, tolerance : Double) : Double
```


## <a name="input"></a><span data-ttu-id="2cbd4-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2cbd4-106">Input</span></span>

### <a name="labeledprobabilities--doubleint"></a><span data-ttu-id="2cbd4-107">Лабеледпробабилитиес: ([Double](xref:microsoft.quantum.lang-ref.double),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="2cbd4-107">labeledProbabilities : ([Double](xref:microsoft.quantum.lang-ref.double),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>




### <a name="bias--double"></a><span data-ttu-id="2cbd4-108">уровень смещения: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2cbd4-108">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="tolerance--double"></a><span data-ttu-id="2cbd4-109">Допуск: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2cbd4-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--double"></a><span data-ttu-id="2cbd4-110">Выходные данные: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2cbd4-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

