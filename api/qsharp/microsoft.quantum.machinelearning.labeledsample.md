---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Определяемый пользователем тип Лабеледсампле
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92711337"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="e1035-102">Определяемый пользователем тип Лабеледсампле</span><span class="sxs-lookup"><span data-stu-id="e1035-102">LabeledSample user defined type</span></span>

<span data-ttu-id="e1035-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e1035-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e1035-104">Пакеты [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e1035-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e1035-105">Пример с именем класса, к которому принадлежит образец.</span><span class="sxs-lookup"><span data-stu-id="e1035-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="e1035-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="e1035-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="e1035-107">Функции: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e1035-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e1035-108">Вектор функций для данного примера.</span><span class="sxs-lookup"><span data-stu-id="e1035-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="e1035-109">Метка: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e1035-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e1035-110">Целочисленная метка для класса, к которому принадлежит этот образец.</span><span class="sxs-lookup"><span data-stu-id="e1035-110">An integer label for the class to which this sample belongs.</span></span>