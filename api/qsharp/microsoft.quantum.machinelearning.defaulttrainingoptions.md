---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: Функция Дефаулттраинингоптионс
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855993"
---
# <a name="defaulttrainingoptions-function"></a><span data-ttu-id="a496f-102">Функция Дефаулттраинингоптионс</span><span class="sxs-lookup"><span data-stu-id="a496f-102">DefaultTrainingOptions function</span></span>

<span data-ttu-id="a496f-103">Пространство имен: [Microsoft. тактов. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a496f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a496f-104">Пакет: [Microsoft. тактов. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a496f-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="a496f-105">Возвращает набор параметров по умолчанию для учебных классификаторов.</span><span class="sxs-lookup"><span data-stu-id="a496f-105">Returns a default set of options for training classifiers.</span></span>

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a><span data-ttu-id="a496f-106">Выходные данные: [траинингоптионс](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="a496f-106">Output : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="a496f-107">Разумный набор параметров обучения по умолчанию для использования при обучении классификаторов.</span><span class="sxs-lookup"><span data-stu-id="a496f-107">A reasonable set of default training options for use when training classifiers.</span></span>

## <a name="example"></a><span data-ttu-id="a496f-108">Пример</span><span class="sxs-lookup"><span data-stu-id="a496f-108">Example</span></span>

<span data-ttu-id="a496f-109">Чтобы использовать параметры по умолчанию, но с дополнительными измерениями, используйте `w/` оператор:</span><span class="sxs-lookup"><span data-stu-id="a496f-109">To use the default options, but with additional measurements, use the `w/` operator:</span></span>

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```