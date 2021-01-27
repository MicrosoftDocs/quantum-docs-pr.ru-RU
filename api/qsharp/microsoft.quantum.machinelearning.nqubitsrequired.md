---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: Функция Нкубитсрекуиред
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: 8f6c1bf3dfef3152a6ba8eada0980d6940724259
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854966"
---
# <a name="nqubitsrequired-function"></a><span data-ttu-id="459a9-102">Функция Нкубитсрекуиред</span><span class="sxs-lookup"><span data-stu-id="459a9-102">NQubitsRequired function</span></span>

<span data-ttu-id="459a9-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="459a9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="459a9-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="459a9-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="459a9-105">Возвращает число Кубитс, необходимое для применения заданного последовательного классификатора.</span><span class="sxs-lookup"><span data-stu-id="459a9-105">Returns the number of qubits required to apply a given sequential classifier.</span></span>

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a><span data-ttu-id="459a9-106">Входные данные</span><span class="sxs-lookup"><span data-stu-id="459a9-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="459a9-107">модель: [секуентиалмодел](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="459a9-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--int"></a><span data-ttu-id="459a9-108">Выходные данные: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="459a9-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="459a9-109">Минимальный размер регистра, на который может быть применен последовательный классификатор.</span><span class="sxs-lookup"><span data-stu-id="459a9-109">The minimum size of a register on which the sequential classifier may be applied.</span></span>