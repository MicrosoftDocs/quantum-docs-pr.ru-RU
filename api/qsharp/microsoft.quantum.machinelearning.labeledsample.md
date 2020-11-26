---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Определяемый пользователем тип Лабеледсампле
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: a7c7dae5cd9e82d66bb98313f4200838006ca291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196333"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="849a8-102">Определяемый пользователем тип Лабеледсампле</span><span class="sxs-lookup"><span data-stu-id="849a8-102">LabeledSample user defined type</span></span>

<span data-ttu-id="849a8-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="849a8-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="849a8-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="849a8-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="849a8-105">Пример с именем класса, к которому принадлежит образец.</span><span class="sxs-lookup"><span data-stu-id="849a8-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="849a8-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="849a8-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="849a8-107">Функции: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="849a8-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="849a8-108">Вектор функций для данного примера.</span><span class="sxs-lookup"><span data-stu-id="849a8-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="849a8-109">Метка: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="849a8-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="849a8-110">Целочисленная метка для класса, к которому принадлежит этот образец.</span><span class="sxs-lookup"><span data-stu-id="849a8-110">An integer label for the class to which this sample belongs.</span></span>