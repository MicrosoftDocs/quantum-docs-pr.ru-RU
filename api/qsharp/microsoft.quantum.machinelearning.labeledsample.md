---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Определяемый пользователем тип Лабеледсампле
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846980"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="18306-102">Определяемый пользователем тип Лабеледсампле</span><span class="sxs-lookup"><span data-stu-id="18306-102">LabeledSample user defined type</span></span>

<span data-ttu-id="18306-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="18306-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="18306-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="18306-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="18306-105">Пример с именем класса, к которому принадлежит образец.</span><span class="sxs-lookup"><span data-stu-id="18306-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="18306-106">Именованные элементы</span><span class="sxs-lookup"><span data-stu-id="18306-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="18306-107">Функции: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="18306-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="18306-108">Вектор функций для данного примера.</span><span class="sxs-lookup"><span data-stu-id="18306-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="18306-109">Метка: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="18306-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="18306-110">Целочисленная метка для класса, к которому принадлежит этот образец.</span><span class="sxs-lookup"><span data-stu-id="18306-110">An integer label for the class to which this sample belongs.</span></span>